# Versatile Liquidity Pools

## Overview

Hadouken inherits Balancer's versatile liquidity pools. While other protocols have pools with constrained parameters, Hadouken can accommodate pools of any composition and underlying math. Hadouken's architecture allows for anyone to develop their own pool type, opening the door for customized pricing functions in trading pools.

## Pools At A Glance <a href="#pools-at-a-glance" id="pools-at-a-glance"></a>

### ​Weighted Pools​ <a href="#weighted-pools" id="weighted-pools"></a>

Designed for general cases, including tokens that don't necessarily have price correlation (e.g. DAI/WETH).

### ​Stable Pools​ <a href="#stable-pools" id="stable-pools"></a>

Ideal for soft-pegged tokens with strong correlation (e.g. DAI/USDC/USDT).

### ​MetaStable Pools​ <a href="#metastable-pools" id="metastable-pools"></a>

Built for non-pegged tokens that maintain correlation but may slowly diverge over time, such as derivatives (e.g. stETH/WETH).

### ​Liquidity Bootstrapping Pools​ <a href="#liquidity-bootstrapping-pools" id="liquidity-bootstrapping-pools"></a>

Ideal for shifting liquidity of one token into another (eg. CKB/ETH).

### ​Managed Pools​ <a href="#managed-pools" id="managed-pools"></a>

Designed to have extreme flexibility to manage a dynamic fund. Features weight shifting to rebalance, swap pausing, and management fees.

## Boosted Pools

Boosted Pools bring benefits to both liquidity providers (LPs) and token swappers. LPs get their liquidity positions sent to external protocols (in this case, Hadouken Lend), such that they receive yield not only from trading fees but also from those protocols. And swappers get access to deep liquidity with low slippage. Boosted Pools are designed for high capital efficiency, giving LPs the benefits of lending out their coins as well as trading fees.

The base components of Boosted Pools are linear pools, which use linear math to facilitate trades between two tokens at a known exchange rate and a fee mechanism to incentivise arbitrageurs to maintain a desired ratio between the tokens. Another key feature of Boosted Pools is Phantom Pool Tokens (Phantom BPT). With a normal LP, the pool mints/burns pool tokens when users join/exit the pool. However, with pools that use Phantom BPT, all pool tokens are minted at the time of pool creation and held by the pool itself. To join/exit the pool, LPs use a _swap_ or _batchSwap_.

_For more information about any of these pools - or about boosted pools - visit the_ [_Balancer GitBook_](https://docs.balancer.fi/products/balancer-pools)_._
