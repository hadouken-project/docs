# Vaults & Smart Order Router

## Overview <a href="#overview" id="overview"></a>

The Smart Order Router (SOR) finds the best prices for Hadouken traders. For given input and output tokens, the SOR finds the optimal trades whether that is a direct swap in one pool, or a combination of trades hopping through multiple pools.

## Utilize All the Liquidity <a href="#utilize-all-the-liquidity" id="utilize-all-the-liquidity"></a>

As the variety of [pools ](https://docs.balancer.fi/products/smart-order-router)grows, the SOR grows too! The SOR keeps expanding as new pool types that use different math under the hood are added. This ensures that all pools in the Hadouken ecosystem can support trades. By integrating with the SOR, any custom pool built on Hadouken can benefit from all the other Hadouken liquidity. All you need to integrate a pool is first and second order differentiable `spotPriceAfterSwap` functions (differentiable either numerically or analytically).

## Taking Gas Into Account <a href="#taking-gas-into-account" id="taking-gas-into-account"></a>

In an ideal world in which gas costs are negligible, a trade between two tokens would involve each Hadouken pool that contains that pair. This would utilize all the available liquidity for the trader and maintain equal prices across all pools. Such a scenario would be an _arbitrage-free state_, in which no value could be extracted from the pools' price differences. Since there _are_ incremental gas costs for each swap added to a batch, additional pools are added to the path only when they provide enough of a price difference to make up for the gas. Since only a subset of pools are considered, this can create arbitrage opportunities across Hadouken pools.

## How It Works <a href="#how-it-works" id="how-it-works"></a>

The optimization mechanism finds the path through a set of Hadouken Pools with the greatest output (after gas costs).

![](https://2409820166-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MlH9xKbfiul3CI0OXaQ%2Fuploads%2FfsAIK6DNg5BW35L1mD71%2FSORrevised4.png?alt=media\&token=c2e566f6-2937-4214-9f5d-f737a794bae3)

### Multiple Pools, Same Spot Price <a href="#multiple-pools-same-spot-price" id="multiple-pools-same-spot-price"></a>

In order to get the best price for a trader, the SOR is designed to create an arbitrage-free state between the paths it's using. In order to achieve this, **each path the SOR routes through needs to provide the same spot price after the swap has completed.**
