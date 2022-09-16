# Crowdsourced Liquidation

Together in collaboration with [B.Protocol](https://bprotocol.org/), Hadouken Lend allows for crowdsourced liquidations. Rather than relying on MEV bots to  perform liquidations and benefit from all the profits associated with doing so, B Protocol democratises liquidations by allowing anyone to initiate a liquidation and share in the liquidation bonus for doing so.

In short, this is how it works. B.Protcol pools users' funds into a "backstop pool," which generates yield when idle, generating passive income to depositors. When a position is eligible for liquidation, the smart contract pulls the necessary funds from the backstop temporarily to facilitate the liquidation. Next, it puts the seized collateral for sale using a combination of DEXes including Hadouken Swap. After the sale goes through, the funds borrowed from the backstop are returned, and profits are accrued.

\_\_\_

Liquidations are an essential part of decentralised lending platforms. When an account’s total health factor as described above is below 1, anyone can make a _liquidationCall()_ to the _LendingPool_ contract, paying back part of the debt owed, and receiving discounted collateral (based on the aforementioned liquidation bonus).

In the event that an account’s health factor is below 1 but there are no willing market participants to initiate the liquidation, the borrower lives to see another day ! Most lending protocols have automated bots built by third parties to participate in this type of profitable transaction. Of course, profitability depends on the size of the loan being liquidated, the gas costs of doing so, and the like.

To initiate a _liquidationCall()_, a user must know the account in question has a health factor below 1, know the valid debt amount and debt asset (_debtToCover_ and _debt_, respectively) to that can be paid, know the collateral asset (_collateral_) you are closing, and whether to receive _hTokens_ or the underlying asset after a successful call.

For simplicity, the user interface would display all outstanding loans and their corresponding health factors. When a loan’s health factor is below one, a button to call _liquidationCall()_ will appear.
