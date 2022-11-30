# Fees & Treasury

## Overview <a href="#overview" id="overview"></a>

There are a few different types of fees on Hadouken, each collected to support a healthy ecosystem. For example, Liquidity Providers collect swap fees as users trade with pools; this acts as an incentive for them to continue providing liquidity, which is useful to facilitate trades.

## Swap Fees <a href="#swap-fees" id="swap-fees"></a>

Traders pay swap fees when they trade with a pool. The fees ultimately go to Liquidity Providers in exchange for them putting their tokens in the pool to facilitate trades. Trade fees are collected at the time of a swap, and it goes directly into the pool, growing the pool's balance. For a trade with a given inputToken and outputToken, the amount collected by the pool as a fee is Amount\_{fee} = Amount\_{inputToken} \* swapFee. As the pool collects fees, **Hadouken Pool Tokens automatically collect fees** because they represent a **proportional share of the pool.**

### Example <a href="#example" id="example"></a>

Let's say Alice, Bob, Chuck, and Diana all provide liquidity in the same pool starting out with a total value of $100. After some time, the pool has collected many trade fees and is now worth $200. The pool itself grows while the Liquidity Providers' proportional shares stay the same.

![](<../.gitbook/assets/image (16).png>)

![](https://2409820166-files.gitbook.io/\~/files/v0/b/gitbook-legacy-files/o/assets%2F-MWZrc\_wdLRZXvxl5Xwv%2F-MguL0VDuq8Ro9e3deZt%2F-MguhSCouPXUk6hvNnmO%2FScreen%20Shot%202021-08-12%20at%2010.10.06%20AM.png?alt=media\&token=df1ce268-123a-4239-b1ed-673747ce2cd8)

### Static and Dynamic Fees <a href="#static-and-dynamic-fees" id="static-and-dynamic-fees"></a>

At the time of pool creation, the pool creator defines the **fee** and the **owner**. If the owner is set to an uncontrolled address (typically the zero address) then the swap fee is **static**. If the owner sets it to a controlled address, that address can set the fee at will, therefore making the swap fee **dynamic**.There are two different ways that a pool can have **Dynamic Fees**, either the pool owner manually sets fees, or the pool creator delegates fees to a governance-approved controller by setting the pool owner to the `delegate` address.​ [Governance approved Gauntlet](https://vote.balancer.fi/#/proposal/QmZZycpDWZYAzNho6uVaWL5nFpVzauc89HC9d5QNTSn18J) to have **Delegated Fee Control** on many pool types. They have been updating fees regularly based on models designed to optimize fee volume to Liquidity Providers. To learn more about how they determine fees, check out [their Medium post](https://medium.com/gauntlet-networks/balancer-v2-pools-trading-fee-methodology-7a65df671b8c).

### Protocol Swap Fees <a href="#protocol-swap-fees" id="protocol-swap-fees"></a>

Protocol Swap Fees are a percentage of swap fees collected by pools. These go to the DAO Treasury to be used or held as the DAO sees fit. Protocol Fees for swaps are currently set to 50%. Protocol Swap Fees are a percent of the already collected swap fees; the traders would see no change in the amount collected. The Liquidity Providers, however, would see a small change. For example, if a pool has a 1% swap fee, and there was a 10% protocol swap fee, 0.9% of each trade would be collected for the LPs, and 0.1% would be collected to the protocol fee collector contract.

## **Flash Loan Fees** <a href="#flash-loan-fees" id="flash-loan-fees"></a>

Flash Loan fees are a type of Protocol Fee on Balancer. The fees collected as interest on flash loans go to the DAO Treasury. Flash loan fees are set to zero, and as of this writing they have not been activated by governance.
