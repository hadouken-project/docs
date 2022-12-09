# Pool Based Lending and Borrowing

Hadouken pools deposited assets together into global markets. When users borrow, they borrow from the global market of that asset. Interest rates for each market are determined dynamically by supply and demand. This design is inspired by protocols like Compound and Aave and offers high levels of capital efficiency for over-collateralized borrowing.

However, because liquidity is shared globally, risk could also spread. High-risk or high-volatility assets could introduce risk to all positions and users in the protocol. For this reason, we have made several enhancements to protect the stability of the protocol.

First, we will strictly limit markets to large-cap crypto assets with sufficient liquidity and reliable oracle price feeds to minimize risk contagion.

Second, we have introduced the concept of Backstop Pools in collaboration with [B.Protocol](https://www.bprotocol.org/). Backstop pools allow users to deposit their hTokens (deposit receipts for Hadouken's lending pools) as liquidation capital. When a debt position is marked for liquidation, funds are pulled from the backstop pool in exchange for discounted collateral and then rebalanced over time to the original assets with profits. Backstop pools provide stability and democratize liquidation, shifting profits from bots to depositors.

Third, we have added a supply cap and a borrowing cap for each asset in addition to the typical liquidation threshold parameter in pool-based lending protocols. We will adjust the supply and borrowing caps over time based on available on-chain liquidity to ensure the optimal function of the backstop pools.

With these measures, we believe Hadouken strikes a good balance between capital efficiency and risk management.
