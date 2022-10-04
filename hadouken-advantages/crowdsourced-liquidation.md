# Crowdsourced Liquidation

Together in collaboration with [B.Protocol](https://bprotocol.org/), Hadouken allows for crowdsourced liquidations for the lending markets. Rather than relying on bots to perform liquidations and benefit from all the profits associated with doing so, Hadouken democratises liquidations by allowing anyone to initiate a liquidation and share in the liquidation bonus.

Hadouken allows users to deposit funds into a "backstop pool". Backstop pool funds are loaned out through the lending markets to generate passive yield for depositors. When a position is eligible for liquidation, the smart contract pulls the necessary funds from the backstop temporarily to facilitate the liquidation. Next, it puts the seized collateral for sale using a combination of DEXes including Hadouken. After the sale goes through, the funds borrowed from the backstop are returned, and profits are accrued.
