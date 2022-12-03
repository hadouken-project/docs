# Tokens

Hadouken supports all Godwoken-enabled assets including [pCKB](https://docs.godwoken.io/integration#pckb) and Force Bridge enabled assets from Ethereum and Binance Smart Chain including ETH, WBTC, USDT, USDC, and BNB. pCKB is to Godwoken what ETH is to the Ethereum chain. To use Hadouken on Godwoken, users have to have enough pCKBs (often displayed as just CKBs) in their wallets.

**Bridged Tokens**

Ethereum-native assets on Godwoken are brought over by a Hadouken-customised implementation of [Force Bridge](https://forcebridge.com/bridge/Ethereum/Nervos). Force Bridge supports many ERC-20 (from Ethereum) and BEP-20 (from Binance Smart Chain) tokens, but Hadouken only supports a subset of those tokens to start. There are both ERC-20 and BEP-20 versions of USDC and USDT available on Hadouken, as well as liquidity pools to swap between the two.

**hTokens**

Similar to Aave's aTokens, Hadouken has hTokens, which are minted and burned upon the supply and withdraw of assets to one of Hadouken's lending pools. hTokens are pegged 1:1 to the value of the underlying asset, and can be stored, transferred, and traded just like normal tokens, as well as deposited into the backstop pool for additional yields.

**BPT Tokens**

Like with other DEXes, Hadouken uses BPT tokens that under the hood closely resemble Balancer's BPTs (Balancer Pool Tokens). These tokens represent proportional ownership in a given pool's liquidity. When users add liquidity, they receive BPTs proportional to the amount of assets being added to the pool. When they exit the pool, these BPTs are burned and the user receives their pro-rata share of deposited assets.

**Other Bridged Tokens**

Hadouken also supports tokens bridged from other interoperability protocols. 

[Celer](https://www.celer.network/technology) is a blockchain interoperability protocol that allows for ease of use through cTokens, which are natively cross-chain interoperable tokens that represent 135 different assets across 37 different blockchains. Hadouken has plans to cTokens in some liquidity / trading pools in the near future.
