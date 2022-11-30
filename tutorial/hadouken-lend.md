# Hadouken Lend

If you hover over the lending button on the navigation bar, you will see a link to assets, which will reveal a list of assets that you can borrow and lend on the platform.

<figure><img src="../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

Navigate to the dashboard using the same navigation bar and you will see your deposits, and - if applicable - any outstanding loans. In this example, we have 50 WBTC deposited already, and it's designated as collateral for a potential debt position. Let's deposit some more collateral, then open a loan. Navigate to the deposits page using the same navigation bar.

<figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

On the deposit page, choose another token, let's say ETH.

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

You will now be redirected to a page where you can specify the amount of ETH you'd like to deposit. Let's type 1000 into the field, and click deposit.

<figure><img src="../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

If you haven't already, you will now be asked to give Hadouken permission to access your ETH. After this transaction is confirmed, you will receive another prompt to confirm the deposit transaction itself. Click confirm on this as well, and wait for confirmation.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

When all of the notifications in the notification center have turned green, you're ready to open a position against your deposits (if you wish).

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

If you navigate back to the dashboard, you should see your shiny new deposits. Now, hover over lending and click borrow.

<figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

You will see a list of assets available to borrow, depending on what other users have provided on the platform. In this case, let's borrow some USDC, as we want to use it to purchase more ETH and create a synthetic leveraged position.

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

Click on ETH, and you will see a field to enter how much ETH you would like to borrow.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

Let's click use max, as we want to take on a risky position. This will result in a borrow of 527.84 ETH, with a health factor of 1.38. If the health factor reaches 1, we will be liquidated !

<figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

Next, click borrow, and confirm the transaction in MetaMask. Wait for confirmation, then head over to the dashboard to see what our new borrow has done to our overall positions.

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

With $2.13 million in deposits, and $677.9k in borrows, we've used 93.46% of our borrowing power, for a health factor of 1.38. Sometimes, the available borrow amount isn't limited by our collateral, but rather by the amount of the desired asset deposited on the platform.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

Let's say the price of ETH moves against us (i.e. it goes down) and we wish to repay part of the loan to keep our health factor in a desirable range, we would click repay on the bottom right of this screen.

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

In this case, let's repay just under half of our loan, or 250 ETH. Enter 250 into the field, and click repay. This should bring our health factor to 2.63, which makes sense as it's a little less than double our previous health factor (note that prices didn't change in this scenario, though we're imagining that they did). Confirm the prompt in MetaMask and wait for the notifications to turn green.

<figure><img src="../.gitbook/assets/image (1) (2).png" alt=""><figcaption></figcaption></figure>

If you navigate back to the dashboard, you'll see that you're now using less than half of your borrowing power.

<figure><img src="../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

Let's say you'd like to close down your open positions entirely, you'd repay the rest of your loan using the steps we just followed, then click withdraw next to each of the deposited assets (e.g. ETH and WBTC). On the withdrawal page, you can click use max, then withdraw.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Then confirm the prompt in MetaMask, and your collateral assets will be removed from Hadouken.

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>
