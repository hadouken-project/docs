# Risk Framework

Initial tokens enabled as collateral that users can borrow against will be stablecoins (USDC and DAI, to start), WBTC, ETH, BNB, ADA, CKB, and HDK (for HDK, only much later after launch, when the token has reached a maturity point with less volatility). The market will decide the deposit (and borrow) APRs based on market dynamics, including the amount of tokens being deposited vs. borrowed in a collateralised debt position (CDP).

For loans, each asset used as collateral will have a different risk scale. Intuitively, less volatile assets like stablecoins will have the lowest / “best” risk scale, followed by assets like ETH, WBTC, and the like with a slightly higher risk scale, followed by lower cap coins like CKB and HDK with the highest risk scale. In this case, this means the loan-to-value ratios for these latter types of loans will be lower (i.e. more collateral must be posted).

Risk scale is based on several factors, including smart contract risk, counterparty risk, and of course market risk. Market risk is the easiest to quantify, and perhaps the most important. Market risk comprises several factors, including liquidity risk, volatility risk, and overall market cap of the asset. For ease, it makes sense to use the same risk scales used by Aave for specific assets.

The amount a user can borrow depends on the amount deposited, and which asset they’ve deposited. Logically, the loan-to-value ratio (LTV) a user experiences will be higher if the risk scale of the deposited asset is more favorable. For stablecoins, the LTV is 75% for DAI and 80% for USDC, with liquidation thresholds 5% above those figures. The LTV for ETH is 82.5% with an 85% liquidation threshold, and 70% for WBTC with a 75% liquidation threshold. (Initial spreads between LTV and LT can be inflated to 10-20%, to ensure a lower risk of liquidation for early users of the platform). Note that USDT is not accepted as collateral by Aave due to the perceived counterparty risk of the backing entity, and therefore the same goes for Hadouken.

A sample LTV for CKB and eventually HDK would be around 30-40%, with liquidation thresholds 20-30% above that. Of course, risk parameters change over time, as will risk scales and the corresponding LTV ratios. The LTV ratio determines the maximum amount a user can borrow for a given basket of collateral, which can comprise several different currencies.

The liquidation threshold (LT) is the value where a position becomes undercollateralised, and could be liquidated. There’s a small safety cushion between LTV and LT, such that loans shouldn’t be liquidated shortly after receipt due to small market movements.

There’s another concept called a liquidation bonus (LB), which is a bonus on the price of assets of the collateral when liquidators purchase it as part of the liquidation of a loan that has passed the LT. In general, the LB is 5-10%.

Two final concepts vital for a lending product are health factor and reserve factor. Health factor is a value that can when below 1 result in liquidation to maintain solvency, and is calculated using the formula below. The reserve factor allocates a share of the protocol’s interests to a collector contract as reserve for the ecosystem.

Below is a table of the various LTV, liquidation threshold, and liquidation bonus values for each supported asset. Liquidation bonuses can be slightly higher to start, to bootstrap various liquidation initiatives (i.e. B Protocol’s liquidation bot).

![](<../.gitbook/assets/image (9).png>)

_For more information on asset risk, please refer to_ [_Aave's documentation_](https://docs.aave.com/risk/asset-risk/risks-per-asset)_._
