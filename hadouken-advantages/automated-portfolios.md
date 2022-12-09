# Automated Portfolios

## Modern Portfolio Theory

Pioneered by Nobel Prize winning economist Harry Markowitz in the mid-20th century, Modern Portfolio Theory (MPT) dictates how investors should choose investments to maximize overall return while limiting risk. The most fundamental aspect of modern portfolio theory is diversification.

MPT assumes by default that investors are risk-averse - as in, they prefer less risky portfolios to riskier ones, given the same expected returns. As a result, this implies that the average investor should invest in a portfolio of multiple asset classes. Markowitz's research showed that investors could achieve the best results by choosing an optimal blend of weighting in high risk and low risk assets.

Another important aspect of MPT is automatic rebalancing. Market price fluctuation changes the weighting of portfolio assets. Rebalancing is the process of having portfolio assets return to their desired allocation. It sells the assets with out-sized gains and buys the assets that lag behind - sells high and buys low.

Hadouken allows users to set up, invest and maintain portfolios with automatic rebalancing. For example, if a user chooses to invest in a portfolio with 1/3 of value in ETH, 1/3 in CKB and 1/3 in USDC, Hadouken incentives arbitragers to always keep the three assets in that desired proportion. If the price of CKB goes up relative to ETH and USDC, the user will own slightly less CKB than they deposited and more in ETH and USDC. And the best part is, as a portfolio investor you're _paid_ for these rebalances rather than _paying_ for them!

## Risk, Return, and Impermanent Loss

The flip side of the reduced portfolio risk is the potential for [impermanent loss](https://academy.binance.com/en/articles/impermanent-loss-explained). Impermanent loss is almost unavoidable for liquidity pools, but on the aggregate, liquidity providers can expect to see a decrease in the volatility of their holdings. For example, a two-asset portfolio with a stablecoin and a volatile asset provides significantly [reduced volatility](https://twitter.com/guil\_lambert/status/1412608674380632067) on both up and downsides, even before considering the income from fees and incentives.

For a quantifiable amount of Impermanent Loss you can expect given a particular divergence in the price of two coins, you can use this [IL calculator](https://dailydefi.org/tools/impermanent-loss-calculator/). The chart below shows how price can impact the amount of impermanent loss that a liquidity provider will experience given a specific return (_x_) in the price of a token. For example, when a token increases 200% in relation to the other one, the liquidity provider will incur an Impermanent Loss of approximately 5.72% versus simply holding the two tokens.

It's important to put Impermanent Loss in the context of portfolio management. While it reduces the overall return, having a diversified blend of assets also reduces portfolio risk for long-term investors.

<figure><img src="../.gitbook/assets/image (3) (2).png" alt=""><figcaption></figcaption></figure>
