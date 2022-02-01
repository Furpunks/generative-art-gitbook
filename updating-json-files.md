---
description: Back to the Furrture
---

# Updating JSON Files

Now that we have uploaded our NFTs to IPFS we need to update our JSON files so that they point to the right location.&#x20;

In order to do that we need to go back into VS Code and open up our project if it isn't already opened. Once it has loaded open config.js by selecting it in the Explorer on the left.&#x20;

Near the top of the page you will see baseUri = "ipfs://NewUriToReplace";

Line 10 in the below screenshot:

![](<.gitbook/assets/Screenshot 2022-01-26 231912.png>)

We need to replace NewUriToReplace with our CID so that it looks **similar** to this:

`const baseUri = "ipfs://QmeRoKHKfncqvwqJAANNMP2FHhtyXENA6uVDRQeX6HhfDH";`

Be sure to paste in **your** CID. Don't use mine because your NFTs will not show up.

Once you have put in your CID we now need to update all of our JSON files. If we have a look at one of them as they currently are we can see that the ipfs URI is still pointing to the default one.

![](<.gitbook/assets/Screenshot 2022-01-26 232448.png>)

In order to update all of our JSON files without overwriting our newly created NFTs locally we can simply run the following in our Terminal window:

&#x20;`node utils/update_info.js`

You will then see the following similar text outputted displaying your CID that you have just added to config.js.

![](<.gitbook/assets/Screenshot 2022-01-28 073229.png>)

Now we can confirm that all of our JSON files have been successfully updated by taking a look at one of them. Here is an example of me looking at the JSON for the first NFT in my list. You can see inside the red circle that the ipfs string has been updated to include our CID. Great!&#x20;

![](<.gitbook/assets/Screenshot 2022-01-28 073456.png>)

### Summary

Now that we have added our CID to our JSON files we need to go back into Pinata and upload the JSON.
