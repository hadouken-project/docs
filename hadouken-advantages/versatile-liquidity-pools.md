# Versatile Liquidity Pools

## Overview

Built on top of Balancer's versatile architecture, Hadouken allows users to create a wide variety of liquidity pools of any composition and underlying math.

## ​Weighted Pools​ <a href="#weighted-pools" id="weighted-pools"></a>

Designed for general cases, Weighted Pool supports up to 8 assets that don't necessarily have price correlation (e.g. CKB/USDC) in a single pool. The creator of Weighted Pools can assign individual weight for each asset, and they're traded with the constant product bonding curve first popularized by Uniswap.

## ​Composable Stable Pools​ <a href="#metastable-pools" id="metastable-pools"></a>

Composable Stable Pools (CSPs) are for assets that are either closely pegged (such as stable coins), or highly correlated (for example, the LP token of a stable pool and another stable coin).  CSPs can hold up to 3 assets in a single pool, and use the StableSwap bonding curve first popularized by Curve to trade assets in the same pool.

When CSPs are used for pegged assets (such as USDC and USDT), they become Stable Pools characterized by slippage tolerance optimization around the pegging price; When CSPs are used to compose with other Weighted Pools (for example, [CKB, [USDC, USDT]]) or Stable Pools (for example, [[USDC, USDT], DAI], they could consolidate liquidity and increase capital efficiency.

## ​Liquidity Bootstrapping Pools​ <a href="#liquidity-bootstrapping-pools" id="liquidity-bootstrapping-pools"></a>

Liquidity Bootstrapping Pools (LBPs) allow pool creators to specify token weighting that slowly changes over time. For example, an LBP can be initiated with 10% of CKBs and 90% of NewToken, and move towards a 50/50 split over time. LBPs give teams the ability to perform an IDO (Initial DEX Offering) that disincentivizes early "ape-ins", to allow the market to slowly settles on a fair price.

## Boosted Pools

Hadouken Boosted Pools bring benefits to both liquidity providers (LPs) and token swappers. LPs get their liquidity positions sent to Hadouken's lending product, such that they receive yield not only from trading fees but also from lending. Swappers get access to deep liquidity with low slippage. Boosted Pools are designed for high capital efficiency, giving LPs the benefits of lending out their coins as well as trading fees.

_For more information about any of these pools - visit the_ [_Balancer Docs_](https://docs.balancer.fi/products/balancer-pools)_._
