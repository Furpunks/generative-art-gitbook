# Minting NFTs

Now that we have our newly created NFT images and their associated JSON files uploaded to cloud storage we are ready to create our smart contract which will mint them.

To do this we are going to use Remix IDE. Remix allows us to deploy and administer smart contracts on Ethereum, Binance and other similar blockchains.



You can access Remix IDE directly by going to [remix.etherum.org](https://remix.ethereum.org)

And if you're interested in learning more about Remix and the community you can do so here:

{% embed url="https://remix-project.org" %}

When you first visit Remix you will be presented a screen that looks like this:

![](<.gitbook/assets/Screenshot 2022-02-01 131311.png>)

It has a similar look and feel to it as VS Code and is fairly straight forward to use. This section of the guide will walk you through creating a smart contract that we can use to mint our new NFTs to the blockchain.

To get started we will need to download a smart contract to work with. Hashlips has already created a smart contract that we can use so we don't need to write one ourselves. I have created a fork of the Hashlips smart contracts folder into the Furpunks GitHub. This will allow the Furpunks to update the contracts to include future feature changes.

To get the code for our smart contract go to: [https://github.com/Furpunks/hashlips\_nft\_contract/tree/main/contract](https://github.com/Furpunks/hashlips\_nft\_contract/tree/main/contract)

And click on SimpleNft.sol. You will then see a similar page below. We want to copy the contents of the SimpleNft.sol contract by clicking on the 'copy' icon circled in yellow.

![](<.gitbook/assets/Screenshot 2022-02-01 141435.png>)

With the code copied into our clipboard we can head back over to Remix. Once in Remix we need to create a new file to store the smart contract code. To do that we can click on the 'Create New File' icon in yellow.

![](<.gitbook/assets/Screenshot 2022-02-01 141822.png>)

Give your file a name, I've called mine NFT.sol, and copy in the contents of the smart contract. Your Remix should now look like the following:

![](<.gitbook/assets/Screenshot 2022-02-01 141944.png>)

