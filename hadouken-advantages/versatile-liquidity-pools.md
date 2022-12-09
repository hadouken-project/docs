# Versatile Liquidity Pools

Hadouken is built on top of Balancer's versatile architecture, and allows users to create liquidity pools of any composition and underlying math.

## ​Weighted Pools​ <a href="#weighted-pools" id="weighted-pools"></a>

Designed for general cases, the Weighted Pool supports up to 8 assets that don't necessarily have price correlation (e.g., CKB/USDC) in a single pool. The creator of Weighted Pools can assign individual weights for pool assets, and they're traded with the constant product bonding curve first popularized by Uniswap.

## ​Composable Stable Pools​ <a href="#metastable-pools" id="metastable-pools"></a>

Composable Stable Pools (CSPs) are for assets that are either closely pegged (such as stablecoins) or highly correlated (for example, the LP token of a stable pool and another stablecoin).  CSPs can hold up to 3 assets in a single pool and use the StableSwap bonding curve first popularized by Curve to trade assets against one another.

When CSPs are used for pegged assets (such as USDC and USDT), they become Stable Pools with slippage tolerance optimization around the pegging price. When they are used to compose with other Weighted Pools (for example, a [CKB, [USDC, USDT]] pool) or Stable Pools (for example, a [[USDC, USDT], DAI] pool), they could consolidate liquidity to increase capital efficiency.

## ​Liquidity Bootstrapping Pools​ <a href="#liquidity-bootstrapping-pools" id="liquidity-bootstrapping-pools"></a>

Liquidity Bootstrapping Pools (LBPs) allow pool creators to specify token weighting that slowly changes over time. For example, an LBP can start with 10% of CKBs and 90% of NewToken, and move towards a 50/50 split over time. LBPs give teams the ability to perform an IDO (Initial DEX Offering) that disincentivizes early "ape-ins", allowing the market to settle on a fair price slowly.

## Boosted Pools

Boosted Pools incentivize arbitragers to send idle liquidity to the lending platform to increase yields. They are more attractive to liquidity providers (LPs) because they receive both trading fees and lending income. Traders then benefit from improved liquidity and lower slippage.

_For more information about any of these pools - visit the_ [_Balancer Docs_](https://docs.balancer.fi/products/balancer-pools)_._
