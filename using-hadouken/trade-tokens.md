# Tokens

Hadouken supports all Godwoken-enabled assets including [pCKB](https://docs.godwoken.io/integration#pckb) and Force Bridge enabled assets from Ethereum and Binance Smart Chain including ETH, WBTC, USDT, USDC, and BNB. pCKB is to Godwoken what ETH is to the Ethereum chain. To use Hadouken on Godwoken, users have to have enough pCKBs (often displayed as just CKBs) in their wallets.

**Bridged Tokens**

Ethereum-native assets on Godwoken are brought over by a Hadouken-customised implementation of [Force Bridge](https://forcebridge.com/bridge/Ethereum/Nervos). Force Bridge supports many ERC-20 (from Ethereum) and BEP-20 (from Binance Smart Chain) tokens, but Hadouken only supports a subset of those tokens to start. There are both ERC-20 and BEP-20 versions of USDC and USDT available on Hadouken, as well as liquidity pools to swap between the two.

Here is a comprehensive list of bridged tokens currently supported :&#x20;

| Token Name | Token Description                         | Contract Address                           |
| ---------- | ----------------------------------------- | ------------------------------------------ |
| CKB        | pCKB (via Godwoken Bridge from CKB)       | 0x7538C85caE4E4673253fFd2568c1F1b48A71558a |
| ETH        | ETH (via Force Bridge from Etherem)       | 0x9E858A7aAEDf9FDB1026Ab1f77f627be2791e98A |
| BTC        | WBTC (via Force Bridge from Ethereum)     | 0x82455018F2c32943b3f12F4e59D0DA2FAf2257Ef |
| USDC       | USDC (via Force Bridge from Ethereum)     | 0x186181e225dc1Ad85a4A94164232bD261e351C33 |
| USDT       | USDT (via Force Bridge from Ethereum)     | 0x8E019acb11C7d17c26D334901fA2ac41C1f44d50 |
| BUSD       | BUSD (via Force Bridge from Ethereum)     | 0x9dC5014998b6A7351d75D731263199D31feb4474 |
| BNB        | BNB (via Force Bridge from BNB Chain)     | 0xBAdb9b25150Ee75bb794198658A4D0448e43E528 |
| BUSD\|bsc  | BUSD (via Force Bridge from BNB Chain)    | 0xD07920d57F400D89d62535D50eb9D1200ed7821B |
| USDC\|bsc  | USDC (via Force Bridge from BNB Chain)    | 0xfA307CfdEA89DC197A346c338a98aC85d517af6e |
| USDT\|bsc  | USDT (via Force Bridge from BNB Chain)    | 0xDFF2faCdFe47C1D5b51f18231f900949F1d5988f |

**hTokens**

Similar to Aave's aTokens, Hadouken has hTokens, which are minted and burned upon the supply and withdraw of assets to one of Hadouken's lending pools. hTokens are pegged 1:1 to the value of the underlying asset, and can be stored, transferred, and traded just like normal tokens. They can also be deposited into the backstop pool for additional yields.

Here is a comprehensive list of hTokens currently supported :&#x20;

| Token Name | Contract Address |
| ---------- | ---------------- |
| hCKB       |                  |
| hETH       |                  |
| hBTC       |                  |
| hBNB       |                  |
| hUSDC      |                  |
| hUSDT      |                  |

**BPT Tokens**

Hadouken's BPT (Balancer Pool Tokens) tokens represent proportional ownership of a liquidity pool. When users add liquidity, they receive BPTs proportional to the amount of assets being added to the pool. When they exit the pool, these BPTs are burned and the user receives their pro-rata share of deposited assets.

**Other Bridged Tokens**

Hadouken also supports tokens bridged from other interoperability protocols.

[Celer](https://www.celer.network/technology) is a blockchain interoperability protocol that allows for ease of use through cTokens, which are natively cross-chain interoperable tokens that represent 135 different assets across 37 different blockchains. Hadouken has plans to cTokens in some liquidity / trading pools in the near future.
