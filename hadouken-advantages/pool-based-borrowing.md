# Pool Based Lending and Borrowing

Hadouken pools together deposited assets into global markets. When users borrow, they borrow from the global market of that asset. Interest rates for each market are determined dynamically by supply and demand. This design is pioneered by protocols like Compound and Aave, and enjoys the highest level of capital efficiency when it comes to over-collateralized borrowing.

On the other hand, because liquidity is shared globally, risk could also spread between positions and users. High-risk or high-volatility assets could introduce risk to all positions in the protocol. For this reason, we've made several enhancements to better protect the stability of the protocol.

First, we'll strictly limit the markets only to large-cap crypto assets with sufficient liquidity and reliable oracle price feeds to minimize risk contagion.

Second, we introduced the concepts of backstop pools in collaboration with [B.Protocol](https://www.bprotocol.org/). Backstop pools allow users to deposit their hTokens (deposit receipts of Hadouken's lending pools) to serve as liquidation capital. When a position is marked to be liquidated, its borrowed asset backstop pool is used to liquidate the position. Funds are pulled from the backstop pools in exchange for discounted collateral, then rebalanced over time to the original assets with profits. Backstop pools provide stability and democratize liquidation to shift profits from bots to depositors.

Third, we added a supply cap and a borrowing cap for each asset in addition to the typical liquidation threshold parameter in pool-based lending protocols. We'll adjust the supply and borrowing caps for each asset over time, based on available on-chain liquidity to ensure the optimal function of the backstop pools.

With the above measures, we believe Hadouken strikes a good balance between capital efficiency and risk.
