# Automated Portfolios

## Modern Portfolio Theory

Pioneered by Nobel Prize winning economist Harry Markowitz in the mid-20th century, Modern Portfolio Theory (MPT) dictates how investors should choose investments to maximise overall return while limiting their risk. The most fundamental and basic aspect of modern portfolio theory is diversification.

MPT assumes by default that investors are fairly risk-averse - as in, they prefer less risky portfolios to riskier ones, given the same expected returns. As a result, this implies that the average investor should invest in a portfolio of multiple asset classes. In fact, Markowitz's research showed that investors can achieve the best results by choosing an optimal blend of weighting in high risk/return and low risk/return assets.

Another important aspect of MPT is automatic rebalancing. Market price fluctuation changes the weighting of portfolio assets. Reblancing is the process of having portfolio assets return to their desired allocation. Practically, it sells the assets with out-sized gains, and buys the assets that lag behind, or simply, sells high and buys low.

Hadouken allows users to set up, invest and maintain portfolios with automatic rebalancing. As an example, if a user chooses to invest in a portfolio with 1/3 of value in ETH, 1/3 in CKB and 1/3 in USDC, Hadouken incentives arbitragers to always keep the 3 assets in that desired proportion. If the price of CKB goes up relative to ETH and USDC, you will own slightly less CKB than you deposited, and more in ETH and USDC. And the best part is, as an portfolio investor you're _paid_ for these rebalances, rather than _paying_ for them !

## Risk, Return, and Impermanent Loss

The flip side of the reduced portfolio risk is the potential for [impermanent loss](https://academy.binance.com/en/articles/impermanent-loss-explained). Impermanent loss is almost unavoidable for liquidity pools, but on the aggregate, liquidity providers can expect to see a decrease in volatility of their holdings. As an example, a two-asset portfolio with a stable coin and a volatile asset provides significantly [reduced volatility](https://twitter.com/guil\_lambert/status/1412608674380632067) on both up and down sides, even before considering the income from fees and incentives.

For a quantifiable amount of IL you can expect given a particular divergence in the price of two coins, you can use this [IL calculator](https://dailydefi.org/tools/impermanent-loss-calculator/). The chart below shows how price can impact the amount of impermanent loss that a liquidity provider will experience given a certain return (_x_) in the price of a token. For example, when a token increases 500%, the liquidity provider will incur an IL of approximately 25% versus having simply held the token.

<figure><img src="../.gitbook/assets/image (3) (2).png" alt=""><figcaption></figcaption></figure>
