# Performing Swaps

Performing an asset swap on Hadouken will feel familiar if you've used Balancer, Curve, Uniswap, or another one of the popular decentralised exchanges available today. First, navigate to [Hadouken](https://app.hadouken.finance/), where you will be taken by default to the swap page.

If you've never used Hadouken before, you will need to initialize a Godwoken Game Plus (Nervos Layer 2) account. However, if you bridge funds to Godwoken from Etheruem, this will be done for you. And you'll even get a little bit of CKB to get started ! Once your Layer 2 account has been created, you will be able to interact with the platform.

By default, you will be taken to the swap page, which looks like this. You can choose a variety of tokens from the dropdown menus, set your slippage tolerance, and preview a trade before submitting the transaction to the blockchain.

<figure><img src="../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

Let's say you want to swap ETH for USDT. First, choose ETH from the dropdown, and type in an amount. In this example, let's swap 100 ETH. You should instantly see an amount populate in the USDT field. Note, it's only an approximate amount. You can also choose slippage tolerance, though by default it's set to 1%.

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

Upon clicking preview, you will be taken to a new page that breaks down your trade. You should see fees, amount expected after fees, and the least you should expect to receive given the stated slippage tolerance. You will also see your trade route ; in this case, your trade is 100% going through the ETH/USDC pool, then the 2pool. You can click on either of these pool icons to visit their respective pages.

<figure><img src="../.gitbook/assets/image (3) (3).png" alt=""><figcaption></figcaption></figure>

Upon clicking confirm trade, you should get a few MetaMask prompts. First, if you haven't given Hadouken permission to access the token you wish to swap out of - in this case, ETH - you need to approve that. You can click edit permission in the MetaMask prompt to increase the amount you're allowing Hadouken to access, but this isn't recommended for most users. Click confirm, and wait for the transaction to confirm.

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

Once the transaction is confirmed - as indicated by a green check mark in the notification center at the bottom of the page, you will receive another MetaMask popup to confirm the swap itself.

<figure><img src="../.gitbook/assets/image (12) (1).png" alt=""><figcaption></figcaption></figure>

Click confirm, and wait for the transaction to confirm. Once it's confirmed, you will also need to wait for the block to be finalized on Layer 1, then your desired tokens (in this case, USDT) will be available.

<figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>
