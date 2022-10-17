# Crowdsourced Liquidation

Together in collaboration with [B.Protocol](https://bprotocol.org/), Hadouken allows for crowdsourced liquidations for the lending markets. Rather than relying on bots to perform liquidations and benefit from all the profits associated with doing so, Hadouken democratises liquidations by allowing anyone to initiate a liquidation and share in the liquidation bonus.

Hadouken allows users to deposit funds into a backstop AMM pool ("BAMM"). Backstop pool funds are loaned out through Hadouken's lending markets to generate passive yield for depositors, resulting in higher capital efficiency. When a position is eligible for liquidation, the smart contract pulls the necessary funds from the backstop temporarily to facilitate the liquidation. Next, it puts the seized collateral for sale using a combination of DEXes including Hadouken. After the sale goes through, the funds borrowed from the backstop are returned, and profits are accrued. Hadouken currently utilises a USDC-denominated backstop, with plans to support additional backstops in the future.

The benefit of B.Protocol is that anybody can initiate a liquidation, regardless of whether they have a vested interest in the platform or not. For more information, [please visit B.Protocol's documentation](https://docs.bprotocol.org/).
