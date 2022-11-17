# Liquidation

Liquidation is the process of repaying another user's debt when their loan position is underwater by a certain threshold, and in turn receiving the underlying collateral. Only users below a health factor of 1.0 can be liquidated. This can happen when debt value grows relative to collateral - either when the collateral price drops or the borrowed token price goes up. Single liquidation calls can only liquidate up to 50% of total debt.

### Why is liquidation happening?&#x20;

Liquidation is necessary for the lending ecosystem to stay healthy - it protects users who deposit to the pool from losing their funds and profits. If no one participated in liquidation, the whole lending platform would become unstable. Liquidators are incentivized to participate in the liquidation ecosystem by receiving a liquidation bonus (about 5-7% depending on the asset) that comes from the liquidated user’s collateral.

### Who can participate in liquidation?

Anyone can take part in the liquidation ecosystem. For example, by writing a liquidation bot that fetches data about reserves, users, and deposit and borrows, then calculates health factor for each user, and finally performs a liquidation call for anyone below a health factor of 1.0.

### How to avoid being liquidated

You can protect yourself from being liquidated as your health factor declines by depositing more tokens as collateral or repaying some of your debt. You can also protect a deposit from liquidation by switching it to a non-collateral asset. However, it won’t increase your borrowing power ; you won’t be able to borrow tokens against non-collateral deposits.

### Example&#x20;

Alice deposits 10 USDT (as non-collateral) and 5000 CKB tokens, and borrows 10 USDC. When CKB prices go down, Alice’s health factor also goes down. If it drops below 1.0 and liquidation occurs, the liquidator can pay up to 5 USDC and receive an equal value of CKB, plus the liquidation bonus (typically 5-7%). After this operation Alice’s health factor should increase to back above 1.0.
