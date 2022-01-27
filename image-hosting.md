# Image Hosting

Now that we have our NFTs generated we need a place to store them so that people can access and view them.

There are few different ways you can go about serving your NFTs to people with Shared Hosting and IPFS being the two most popular options. Other options such as Dropbox or One Drive also exist but for the purposes of this guide we will focus on IPFS as that is the most decentralised way to store your NFTs forever online.&#x20;

If you don't know what IPFS is, it stands for InterPlanetary File System and essentially decentralised storage kind of like having a permanent hard drive in the cloud that anyone can access. That is of course an over simplification so if you fancy reading up on IPFS, which I recommend, you can do so here:

{% embed url="https://ipfs.io/#how" %}

### Pros and Cons of Different Storage Solutions

Here are a few pros and cons of the different options.

#### **Shared Hosting**

**PROS**

* Easy to set up and configure
* Can modify JSON and PNG files any time

**CONS**

* Susceptible to outages due to hosting provider, VPS downtime, missed payment, etc
* Lack of trustworthiness that files will not be altered.

#### IPFS

**PROS**

* Easy to set up and configure
* Permanent storage so NFTs always available&#x20;
* No service outages
* Trustworthy source

**CONS**

* Permanent - if you make a mistake in the JSON or NFT, it is very nearly impossible to fix.



## Setting up IPFS

Like with many of the other areas covered in this guide there are a few different ways to upload and store your NFTs on IPFS. This guide will cover using Pinata.cloud. Other methods will be added at a later time so check back to see if your preferred method has been added.

Pinata.cloud is an online service that allows you to upload and store your NFTs for Free. Their Free plan includes 1 GB of storage which should be enough for most projects.&#x20;

First we need to head over to Pinata.Cloud and register for a free account:

{% embed url="https://www.pinata.cloud" %}

Their website may have changed by the time you read this but it currently looks like this:

![](<.gitbook/assets/Screenshot 2022-01-26 223102.png>)

You will want to click Try for Free in the top right and follow the sign up process on the next page.

Once you have confirmed your email and logged in you should be presented with something similar to the following screenshot:

![](<.gitbook/assets/Screenshot 2022-01-26 224429.png>)

_Side note, for the astute among you, you will have noticed that I changed web browsers for the above screenshot and a few others below. This was due to a graphics overlay issue that Chrome was having inside my Windows 11 virtual machine running in VMWare Workstation Pro 16.2.2. So if you experience an issue where the Pinata page isn't loading, try swapping over to Mozilla Firefox. Anyway, back to the guide._

__

Once logged into Pinata we will be presented with our Files view. We will now need to create a new CID which we will use for our JSON files.

Click Upload and select Folder.

![](<.gitbook/assets/Screenshot 2022-01-26 224942.png>)

You will be presented a pop up window. Click Select.

![](<.gitbook/assets/Screenshot 2022-01-26 225118.png>)

&#x20;This will open a Windows Explorer window. We now need to browse to the parent folder containing our generated NFTs. If you have been following this guide then it should look similar to the folder in the screenshot below in the address bar.

![](<.gitbook/assets/Screenshot 2022-01-26 225333.png>)

Click Upload. Once you do a warning will pop up asking if you are sure you want to upload all files from "images". Click Upload.

![](<.gitbook/assets/Screenshot 2022-01-26 225437.png>)

You will now have a new pop up asking you to provide a name for the folder you will be uploading. You can call the folder 'images' or give it a more meaningful name if you intend to upload other projects. In my example I will call the folder Furpunks\_NFT\_Test. Click upload. Your NFTs will now upload onto IPFS!

Depending on how many NFTs, their size and your internet connection, this could take some time. Be patient and let the upload finish completely before moving to the next step.

Once they have been completely uploaded you will be taken back the the Files page and should see something similar to the following:

![](<.gitbook/assets/Screenshot 2022-01-26 230125.png>)

We can now see our new folder and the CID that has been generated for it. This is the unique identifier that we need in order to reference our NFTs from our JSON files. The following screenshot is a zoomed in version.

![](<.gitbook/assets/Screenshot 2022-01-26 230201.png>)

If we want to confirm that our NFTs have been successfully uploaded we can do so by clicking on our newly created folder. A new tab will open that will display all the NFTs that we have uploaded.&#x20;

![](<.gitbook/assets/Screenshot 2022-01-26 230714 (1).png>)

From here you can see all the NFT file names listed. Clicking on one of them will allow us to see what it is:

![](<.gitbook/assets/Screenshot 2022-01-26 230840.png>)

That's it! We are now ready for the next step. Before continuing be sure to copy your CID. A good place to store it while we work through this guide is in Notepad.

Once you've got your CID continue to the next step.
