# Tokens

Hadouken supports all Godwoken-enabled assets including [pCKB](https://docs.godwoken.io/integration#godwoken-web3-api-compatibility) and Force Bridge enabled assets from Ethereum and Binance Smart Chain including ETH, WBTC, USDT, USDC, and BNB. pCKB is to Godwoken what ETH is to the Ethereum chain. Godwoken uses CKB as pCKB by default, the user needs not do anything for this conversion (not like converting ETH to WETH on Ethereum).

**Bridged Assets**

Ethereum-native assets on Godwoken are brought over by a Hadouken-customised implementation of [Force Bridge](https://forcebridge.com/bridge/Ethereum/Nervos), but treated on Hadouken the same as native assets. Force Bridge supports many ERC-20 and BEP-20 tokens, though Hadouken to start only supports the tokens mentioned above.

**hTokens**

Similar to Aave's aTokens, Hadouken has hTokens, which are minted and burned upon the supply and withdraw of assets to one of Hadouken's lending pools. hTokens are pegged 1:1 to the value of the underlying asset, and can be stored, transferred, and traded just like normal tokens, as well as deposited into the backstop pool for additional yields.

**LP Tokens**

Like with other DEXes, Hadouken uses LP tokens that under the hood closely resemble Balancer's BPTs (Balancer Pool Tokens). These tokens represent proportional ownership in a given pool's liquidity. When users add liquidity, they receive BPTs proportional to the amount of assets being added to the pool. When they exit the pool, these BPTs are burned and the user receives their pro-rata share of deposited assets.

**Trading Tokens**

Hadouken's DEX allows users to trade tokens without the need for a centralised exchange or other trusted third party. By connecting their MetaMask, users can access the liquidity pools on Hadouken to swap between various pairs, including stablecoins and ETH pairs.

Using Balancer's Smart Order Router (SOR), Hadouken Swap finds the best prices for traders of all assets. For given source and destination tokens, the SOR finds the optimal trades to give the token holder the best price for their desired swap. Because gas costs on Godwoken are negligible, the SOR is particularly advantageous, in that it gives users the best rate regardless of the necessary number of "hops" between different pools.

Fees to perform swaps on Hadouken are 0.2% for stablepools and 0.3% for weighted pools. Of these fees, 50% go to liquidity providers and 50% currently goes to the protocol.
