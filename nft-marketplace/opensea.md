# OpenSea

This section will walk you through linking your NFTs to OpenSea.

Before we get started make sure you have your smart contract address to hand. If you don't, open Remix and copy it by clicking the copy icon next to your deployed contract. See yellow circle in the following screenshot.

![](<../.gitbook/assets/Screenshot 2022-02-01 193109.png>)

Next, lets head over to OpenSea's testnet app by going to [https://testnets.opensea.io/](https://testnets.opensea.io)

{% embed url="https://testnets.opensea.io" %}

![](<../.gitbook/assets/Screenshot 2022-02-01 193505 (1).png>)

You will see a similar landing page to the screenshot above with potentially different Top Collections being displayed.

If this is our first time here we need to connect our wallet. This is the same wallet that we have been using for the previous steps. To connect, click the profile icon in the top right.

![](<../.gitbook/assets/Screenshot 2022-02-01 194317.png>)

This will open up a new page where we will want to select Metamask. Once you click on Metamask you will be promoted to confirm the account you would like to connect and to connect.&#x20;

![](<../.gitbook/assets/Screenshot 2022-02-01 194041.png>)

![](<../.gitbook/assets/Screenshot 2022-02-01 194050.png>)

Once we have connected our wallet to OpenSea, we will be redirected to our OpenSea dashboard.

![](<../.gitbook/assets/Screenshot 2022-02-05 101406.png>)

If this is the first time using OpenSea and you haven't bought any previous NFTs your dashboard will look like the screenshot above with no items to display.&#x20;

Now lets add our smart contract address so that we can see the NFTs we have minted.

To do that click on your profile icon in the top right and select My Collections.

![](<../.gitbook/assets/Screenshot 2022-02-05 101637.png>)

We will now have the option to Create a collection, however, we have already done that ourselves so what we want to do is import our existing smart contract. Click on the three dots and select Import an existing smart contract.

![](<../.gitbook/assets/Screenshot 2022-02-05 101756.png>)

We will now have an option from where to import our contract from. We have been using the testnet so we are going to select Live on a testnet.

![](<../.gitbook/assets/Screenshot 2022-02-05 101957.png>)

OpenSea will now ask us for the smart contract address. We want to make sure we have Rinkeby selected and then paste in our smart contract address followed by clicking Submit.

![](<../.gitbook/assets/Screenshot 2022-02-05 102702.png>)

Once we have imported our smart contract we will now see the minted NFTs appear in our dashboard!

![](<../.gitbook/assets/Screenshot 2022-02-01 194921.png>)

And with any luck we will see the five NFTs we minted! Easy right! If yours don't immediately show up check out the Troubleshooting section or join the TG Furpunks group and ask for help.

Lets click on one to see a bit more information.

![](<../.gitbook/assets/Screenshot 2022-02-01 195419.png>)

When we view one of the NFTs we can see the Description that we gave them in the smart contract, along with the various properties that make up our NFT which are read from our json files.

After a bit of time, OpenSea will calculate the rarity percentage of each of the traits and display then automatically next to each one. You don't need to do anything for that happen, it just takes a little time for it to show up.

From this page you can put your NFT up for sale. Be sure to follow OpenSea's guide on how to do that if you run into any trouble.
