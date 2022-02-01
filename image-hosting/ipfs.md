# IPFS

## Setting up IPFS

Like with many of the other areas covered in this guide there are a few different ways to upload and store your NFTs on IPFS. This guide will cover using Pinata.cloud. Other methods will be added at a later time so check back to see if your preferred method has been added.

Pinata.cloud is an online service that allows you to upload and store your NFTs for Free. Their Free plan includes 1 GB of storage which should be enough for most projects.&#x20;

First we need to head over to Pinata.Cloud and register for a free account:

{% embed url="https://www.pinata.cloud" %}

Their website may have changed by the time you read this but it currently looks like this:

![](<../.gitbook/assets/Screenshot 2022-01-26 223102.png>)

You will want to click Try for Free in the top right and follow the sign up process on the next page.

Once you have confirmed your email and logged in you should be presented with something similar to the following screenshot:

![](<../.gitbook/assets/Screenshot 2022-01-26 224429.png>)

__

Once logged into Pinata we will be presented with our Files view. We will now need to create a new CID which we will use for our JSON files.

Click Upload and select Folder.

![](<../.gitbook/assets/Screenshot 2022-01-26 224942.png>)

You will be presented a pop up window. Click Select.

![](<../.gitbook/assets/Screenshot 2022-01-26 225118.png>)

&#x20;This will open a Windows Explorer window. We now need to browse to the parent folder containing our generated NFTs. If you have been following this guide then it should look similar to the folder in the screenshot below in the address bar.

![](<../.gitbook/assets/Screenshot 2022-01-26 225333.png>)

Click Upload. Once you do a warning will pop up asking if you are sure you want to upload all files from "images". Click Upload.

![](<../.gitbook/assets/Screenshot 2022-01-26 225437.png>)

You will now have a new pop up asking you to provide a name for the folder you will be uploading. You can call the folder 'images' or give it a more meaningful name if you intend to upload other projects. In my example I will call the folder Furpunks\_NFT\_Test. Click upload. Your NFTs will now upload onto IPFS!

Depending on how many NFTs, their size and your internet connection, this could take some time. Be patient and let the upload finish completely before moving to the next step.

Once they have been completely uploaded you will be taken back the the Files page and should see something similar to the following:

![](<../.gitbook/assets/Screenshot 2022-01-26 230125.png>)

We can now see our new folder and the CID that has been generated for it. This is the unique identifier that we need in order to reference our NFTs from our JSON files. The following screenshot is a zoomed in version.

![](<../.gitbook/assets/Screenshot 2022-01-26 230201.png>)

If we want to confirm that our NFTs have been successfully uploaded we can do so by clicking on our newly created folder. A new tab will open that will display all the NFTs that we have uploaded.&#x20;

![](<../.gitbook/assets/Screenshot 2022-01-26 230714 (1).png>)

From here you can see all the NFT file names listed. Clicking on one of them will allow us to see what it is:

![](<../.gitbook/assets/Screenshot 2022-01-26 230840.png>)

### Summary

We are now ready for the next step. Before continuing be sure to copy your CID. A good place to store it while we work through this guide is in Notepad.

We will now need to update our JSON files before coming back to Pinata.

Once you've got your CID continue to the next step.
