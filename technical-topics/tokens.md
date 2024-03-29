# Tokens

Hadouken supports all Godwoken-enabled assets including [pCKB](https://docs.godwoken.io/integration#pckb) and Force Bridge enabled assets from Ethereum and Binance Smart Chain, such as ETH, WBTC, USDT, USDC, and BNB. pCKB is to Godwoken what ETH is to the Ethereum blockchain. To use Hadouken on Godwoken, users must have enough pCKBs (often displayed as just CKBs) in their wallets.

## Bridged Tokens

Ethereum-native assets on Godwoken are brought over by a Hadouken-customised implementation of [Force Bridge](https://forcebridge.com/bridge/Ethereum/Nervos). Force Bridge supports many ERC-20 (from Ethereum) and BEP-20 (from Binance Smart Chain) tokens, but Hadouken only supports a subset of those tokens to start. There are both ERC-20 and BEP-20 versions of USDC and USDT available on Hadouken, as well as liquidity pools to swap between the two. Hadouken also supports tokens bridged using the Celer bridge and Multichain bridge.

Here is a comprehensive list of bridged tokens currently supported by Hadouken:

| Token Name | Token Description                      | Contract Address                           |
| ---------- | -------------------------------------- | ------------------------------------------ |
| CKB        | pCKB (via Godwoken Bridge from CKB)    | 0x7538C85caE4E4673253fFd2568c1F1b48A71558a |
| ETH        | ETH (via Force Bridge from Etherem)    | 0x9E858A7aAEDf9FDB1026Ab1f77f627be2791e98A |
| BTC        | WBTC (via Force Bridge from Ethereum)  | 0x82455018F2c32943b3f12F4e59D0DA2FAf2257Ef |
| USDC       | USDC (via Force Bridge from Ethereum)  | 0x186181e225dc1Ad85a4A94164232bD261e351C33 |
| USDT       | USDT (via Force Bridge from Ethereum)  | 0x8E019acb11C7d17c26D334901fA2ac41C1f44d50 |
| BUSD       | BUSD (via Force Bridge from Ethereum)  | 0x9dC5014998b6A7351d75D731263199D31feb4474 |
| BNB        | BNB (via Force Bridge from BNB Chain)  | 0xBAdb9b25150Ee75bb794198658A4D0448e43E528 |
| BUSD\|bsc  | BUSD (via Force Bridge from BNB Chain) | 0xD07920d57F400D89d62535D50eb9D1200ed7821B |
| USDC\|bsc  | USDC (via Force Bridge from BNB Chain) | 0xfA307CfdEA89DC197A346c338a98aC85d517af6e |
| USDT\|bsc  | USDT (via Force Bridge from BNB Chain) | 0xDFF2faCdFe47C1D5b51f18231f900949F1d5988f |
| ceUSDC     | Celer USDC (via Celer Bridge)          | 0x53bB26dc8C5EFC6c95C37155aCa487d1D043436a |
| ceUSDT     | Celer USDT (via Celer Bridge)          | 0x3c790b38f466514ffCB4230e7B2334e52B64c942 |
| ceETH      | Celer ETH (via Celer Bridge)           | 0xB66954619363145a05eF835547449EB9050d82f6 |
| ceWBTC     | Celer WBTC (via Celer Bridge)          | 0x1C428a6539A40eC5Bb481631266a51cd19b233B1 |

## hTokens

Similar to Aave's aTokens, Hadouken has hTokens, which are minted and burned upon the supply and withdrawal of assets to one of Hadouken's lending pools. hTokens are pegged 1:1 to the value of the underlying asset and can be stored, transferred, and traded just like normal tokens. They can also be deposited into the backstop pool for additional yields.

Here is a comprehensive list of hTokens currently supported by Hadouken:

| Token Name | Contract Address                           |
| ---------- | ------------------------------------------ |
| hCKB       | 0x734ba3e711a22a383c1A26DBE5D529CFb793C3bf |
| hETH       | 0x0A0f1D2A3ea1E0442EbC8CC3a2139a2E7B314AA5 |
| hBTC       | 0x294f250a63C10Df254233B382dB495321E23e161 |
| hBNB       | 0xBc63b48c6aA8EC2E7fB899Bcd5Cca3fD8c4b7662 |
| hUSDC      | 0x06c0c3ea4983d0141e79f78343Da48BaE6b61a09 |
| hUSDT      | 0x66206E9b054361B623046B12Aa99215541216741 |

## BPT Tokens

Hadouken's BPT (Balancer Pool Tokens) represent proportional ownership of a liquidity pool. When users add liquidity, they receive BPTs proportional to the amount of assets being added to the pool. When they exit the pool, these BPTs are burned and the user receives their pro-rata share of deposited assets.

For example, if a user adds 1,000 USDC and 1,000 CKB to a liquidity pool, and the pool has a total of 10,000 USDC and 10,000 CKB, they would receive 10% of the BPTs minted for that pool. If they later decide to exit the pool, they would receive 1,000 USDC and 1,000 CKB and their BPTs would be burned.
