# Trade Tokens

Hadouken Swap is first and foremost a DEX, which allows users to trade tokens without the need for a centralised exchange or other trusted third party. By connecting their MetaMask, users can access the liquidity pools on Hadouken to swap between various pairs, including stablecoins and ETH pairs.

Using Balancer's Smart Order Router (SOR), Hadouken Swap finds the best prices for traders of all assets. For given source and destination tokens, the SOR finds the optimal trades to give the token holder the best price for their desired swap. Because gas costs on Godwoken are negligible, the SOR is particularly advantageous, in that it gives users the best rate regardless of the necessary number of "hops" between different pools.

Assets bridged from Ethereum are _.e_ assets, though on the Hadouken Swap user interface the _.e_ is dropped for simplicity. For example, USDT is actually USDT.e (that is, wrapped USDT from Ethereum), USDC is USDC.e, etc. There is no BTC on Godwoken, but rather WBTC (wrapped bitcoin on Ethereum). BUSD, however, is from Binance Smart Chain. The only native asset on Godwoken is CKB.

Fees to perform swaps on Hadouken are in line with the industry average, at 0.2% for stablepools and 0.3% for weighted pools. Of these fees, 50% go to liquidity providers and 50% currently goes to the protocol.
