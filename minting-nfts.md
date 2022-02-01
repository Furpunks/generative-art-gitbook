# Minting NFTs

Now that we have our newly created NFT images and their associated JSON files uploaded to cloud storage we are ready to create our smart contract which will mint them.

To do this we are going to use Remix IDE. Remix allows us to deploy and administer smart contracts on Ethereum, Binance and other similar blockchains.



You can access Remix IDE directly by going to [remix.etherum.org](https://remix.ethereum.org)

And if you're interested in learning more about Remix and the community you can do so here:

{% embed url="https://remix-project.org" %}

## Creating Our Smart Contract

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

In a later update to the guide I will walk through what each line of code is doing so that you can follow along with what the contract does. For now though there are a few important settings to be aware of.

`uint256 public maxSupply = 10000;`

`uint256 public maxMintAmount = 20;`



maxSupply is telling the smart contract that we are going to ever have a total number of 10000 NFTs. You will need to set this to what is suitable for your project.

maxMintAmount tells the smart contract to mint the first 20 NFTs and assign them to the wallet owner. That will be your Metamask wallet that you have connected.



For our guide I will leave these all set to default even though we only uploaded five NFTs to IPFS earlier.&#x20;



With our smart contract in Remix we now need to compile it so that Remix can execute it in a later step. To do so click on the Solidity complier icon, the first yellow circle in the image below.

![](<.gitbook/assets/Screenshot 2022-02-01 142353.png>)

For other projects you will need to ensure that your compiler matches or is compatible with the version of your smart contract code. Our smart contract is expecting 0.7.0 <0.9.0 which you can see on line 16 of the code.

The complier version 0.8.7 selected in the screen shot above falls within our expected range so we are good to go.

Be sure to select the box next to Enable optimization and leave the value at 200.

Now click Compile.

Once Remix has compiled the Contract you will see it displayed on the left like so:

![](<.gitbook/assets/Screenshot 2022-02-01 142908.png>)

## Deploying the Smart Contract

To get ready to deploy our smart contract we need to click on the Deploy & run transactions icon circled in yellow below. This will bring up a few options which we will need to configure.

![](<.gitbook/assets/Screenshot 2022-02-01 150156.png>)

First we need to change the Environment to work with Metamask. To do that click the drop down list under Environment and select Injected Web3. A Metamask pop up with be displayed asking you to connect. Click Next.

![](<.gitbook/assets/Screenshot 2022-02-01 150539.png>)

After clicking Next you will be prompted to allow Remix to see address, account balance, activity and initiate transactions. Click Connect.

![](<.gitbook/assets/Screenshot 2022-02-01 150625.png>)

Remix will now show your Environment as Injected Web3 and you will see the following Environment.

![](<.gitbook/assets/Screenshot 2022-02-01 150831.png>)

We now need to tell Remix which Contract we want to Deploy. We can do this by selecting the contract name that we created during Creating our Smart Contract section from the Contract drop down list. The contract in this guide is called NFT.sol so I will select that.

![](<.gitbook/assets/Screenshot 2022-02-01 151146.png>)

With our contract selected we can now pass in a few parameters that will be used when deploying the contract to the blockchain. Click on the arrow circled in yellow below:

![](<.gitbook/assets/Screenshot 2022-02-01 151627.png>)

This will expand the options that we can provide parameters for.

![](<.gitbook/assets/Screenshot 2022-02-01 151659.png>)

We can see that the smart contract allows us to supply the Name, Symbol, Base URI and a not revealed URI.

### Smart Contract Parameters

**NAME**

This is the name of our set of NFTs. In this example we will set Name to Furpunks.

**SYMBOL**

The symbol is the short three or four character representation of our NFTs similar to ETH for Ethereum or KTY for Krypto Kitty :)&#x20;

We will be using FUR as our symbol for this guide.

**INITBASEURI**

The base URI is the IPFS URI to our JSON files. So if you have been following along from the beginning you will need to provide your base URI that you have created. For this guide we will be using: [https://ipfs.io/ipfs/](https://ipfs.io/ipfs/)QmXYnfnw5wdyJuTwYqBqty9jboxvNFjZYu7A1HAiHueqvi/

Be sure to replace the CID with the one you have from Pinata otherwise your NFT images will not load. Also do not forget to put a trailing / at the end!

**INITNOTREVEAKEDURI**

This is the base URI to display for NFTs that have not been revealed yet. This is good for when you don't want to show what the NFT is that someone is buying unit they have already purchased it. We won't be using this setting for our example so will just leave it blank.



Lets take a look at what all those settings look like when configured.

Once we have selected our Environment, Contract and added in our values for the contract parameters your screen should look like this:

![](<.gitbook/assets/Screenshot 2022-02-01 172616.png>)

_Side note: All the steps above are the same for the Binance Smart Chain as well if you're project is on BSC. In order for the contract to be deployed to BSC you will need to make sure you have selected a BSC Testnet in Metamask._

Now we're ready to execute our Remix code and deploy our smart contract to the Ethereum blockchain. Click transact. __&#x20;

Once we click transact Metamask will pop up a confirmation window. From here we can see the expected gas fees in ETH. Click Confirm to proceed with the transaction.

![](<.gitbook/assets/Screenshot 2022-02-01 173512.png>)

The deployment of the contract could take anywhere between a few seconds or a few mins if you're deploying to Mainnet depending on how congested the network is. Be patient and wait for Metamask to display a confirmation in the bottom of the screen like so:

![](<.gitbook/assets/Screenshot 2022-02-01 173533.png>)

Great, now that our transaction has gone through we can open Metamask and see that our ETH has been deducted the gas fees for the contract deployment. If you click on Contract Deployment under Activity we can see a few more details.

![](<.gitbook/assets/Screenshot 2022-02-01 173555.png>)

From this pop up we can see the total cost of ETH it took us to deploy our contract. We also have a link where we can see it on the blockchain. Click on the View on block explorer link.

![](<.gitbook/assets/Screenshot 2022-02-01 173609.png>)

This will take us to etherscan (or bscscan if using BSC Testnet) where we can see the transaction that occurred in order to deploy our smart contract.

![](<.gitbook/assets/Screenshot 2022-02-01 173625.png>)

Great! We are now ready to mint our NFTs.

If we head back over to our Remix window we can see the newly deployed contract.

![](<.gitbook/assets/Screenshot 2022-02-01 175513.png>)

&#x20;Lets expand it to see what options we have available to us. There's quite a lot so I have split the images into two. They both include the same withdraw button to provide context on where the settings are in relation to one another.

![](<.gitbook/assets/Screenshot 2022-02-01 175747.png>) ![](<.gitbook/assets/Screenshot 2022-02-01 175823.png>)

As you can see there are a LOT of different ways we can interact with our newly created smart contract.

Lets start out by click Name. It should return the Name of your smart contract which in this example is Furpunks.

Owner - This should display your wallet address which signifies you are the owner of the contract.

