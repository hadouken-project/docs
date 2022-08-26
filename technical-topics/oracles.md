# Oracles

Of the utmost importance here is the price oracle. Aave uses Chainlink. Hadouken will use a combination of Band Protocol and DIA, with redundancy in place to avoid unnecessary, erroneous liquidations.

1. At pre-specified intervals, asset prices are checked using a call to Band Protocol.
2. If the price is below or equal to zero, or drastically different (e.g. >10% different) from the last price check, a call is made to the fallback price oracle (e.g. DIA).

Aave is first and foremost an ETH-denominated platform, so its oracle-integrated price calls return values in wei (1/1018 ETH). Hadouken is “denominated” in either CKB or HDK, but for simplicity assets should be priced in USD terms as allowed by the oracle(s). A list of methods follow :

* _getAssetPrice() : Returns the price of the supported \_asset._
* _getAssetsPrices() : Returns an array of prices._
* _getSourceOfAsset() : Returns the address of the price source for \_asset._
* _getFallbackOracle() : Returns the address of the fallback oracle._

How do oracles work ? Using Band as an example, their data provider platform is a decentralised oracle network (DON) that allows anyone with a data API endpoint to supply data and earn revenue on-chain in real time and at scale.

A data source on Band is an executable that describes the procedure to retrieve raw data points from a set of primary sources, and the fee associated with one data query. The execution takes place off-chain in order to reduce on-chain workloads. These primary sources can either be a traditional API or any other source that returns the desired result. Band supports both permissionless and private APIs. One of Band’s most popular use cases is of course [pulling crypto prices from CoinGecko](https://cosmoscan.io/data-source/2#code).

A data source can be registered into the system by anyone by the registrant sending a _MsgCreateDataSource_ message to the chain. In this message, they specify parameters including the per-query fee, name data of the data source, content of the executable run by validators upon receiving the request, sender / owner of the data source.

When someone wants to request data from the oracle, they don’t call the data source directly ; instead, they call the corresponding oracle script, which proceeds to then execute the necessary data sources. The oracle script behaves like other smart contracts on-chain. While the data source operates off-chain to reduce workload, the oracle script is responsible for compiling results from data sources to enable on-chain security.

The oracle script itself is an executable program that encodes two pieces of data : the set of raw data requests to the sources it needs, and the way to aggregate raw data reports into the final result. Oracle scripts themselves are Turing-complete and can be written in any programming language that supports compilation into WebAssembly.

The Oracle Script Execution Flow is as follows :

1. In the preparation phase, the script outlines the data sources that are required for its execution. It then sends a request to validators to retrieve the result from those data sources. The content of this request consists of the data sources’ execution steps and parameters required.
2. In the aggregation phase, the oracle script aggregates all of the data reports returned by the validators. Each report contains the values which the validator received from the data sources. The script then combines those values into a single, final result.

An oracle script can be registered into the system by anyone by the registrant sending a _MsgCreateOracleScript_ message to the chain. In this message, they specify parameters including the schema, name, and description of the oracle script, .wasm file (binary code saved in the WebAssembly format), sender / owner of the oracle script.

More information can be found on [Band Protocol’s GitBook](https://docs.bandchain.org/custom-script/data-source/introduction.html).
