---
description: Back to the Furrture
---

# Configuration Part II

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
