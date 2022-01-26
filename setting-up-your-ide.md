# Setting up your IDE

This guide uses Microsoft's Visual Studio Code (VS Code) for its IDE. Other IDEs will be added in the future to support different operating systems.



### Install VS Code

The first thing we need to do in install VS Code. Find the executeable you downloaded and run through the installation wizard. After it has finished installed you can launch it from your Windows start menu. You should see a screen like this.

![](<.gitbook/assets/VS Code First Run.png>)

### Clone Furpunks

Now we need to clone the Furpunks github repository to a local folder on our system. To do that we need to open Terminal in VS Code. From the top menu click Terminal / New Terminal or Ctrl+Shift\_+'&#x20;

You should then see a new window appear at the bottom of the IDE which we will use to interact with the code.&#x20;

![](<.gitbook/assets/Screenshot 2022-01-12 170054.png>)

You will now need to change to a drive or directory that you want to clone the Furpunks repository to. I have mine set to E:\NFTS for this walkthrough.

![](<.gitbook/assets/Screenshot 2022-01-12 171056.png>)

To clone the repo, in the terminal prompt we want to type the following follwed by return.

``[`git clone`](https://github.com/Furpunks/hashlips\_art\_engine.git)[`https://github.com/Furpunks/furpunks_art_engine`](https://github.com/Furpunks/furpunks\_art\_engine)``

You should see the following output being displayed in your terminal window.

![](<.gitbook/assets/Screenshot 2022-01-12 170454 (2).png>)

Let's open the repo in VS Code. From the menu click File Open Folder and browse to the newly downloaded folder from github. This will be called ‘furpunks\_art\_engine’. Note: The screen shot below says generative-art. I haven't had time to recreate this walkthrough yet using the new folder name.

Select Open Folder.

&#x20;When you first open a repository in VS Code you will be prompted to trust the authors of the files in the folder.

![](<.gitbook/assets/Screenshot 2022-01-12 171905.png>)

If you are like my cat and don't trust me, then click No! Otherwise to continue with this guide you will need to tick the box ‘Trust the authors of all files in the parent folder’ and then select ‘Yes, I trust the authors button’.

You will now be presented with a screen that looks like this. Your Generative-Art repo should now appear on the left hand side in the Explorer.

![](<.gitbook/assets/Screenshot 2022-01-26 201843.png>)

### Install Node JS Modules

&#x20;Now we need to install the Node JS modules to be used with the Furpunks project. We can do this by running the following in Terminal.

`npm install`

&#x20;Once completed you will see the following output in Terminal.

![](<.gitbook/assets/Screenshot 2022-01-26 202031.png>)

We will now also have the modules added to our repo. We can verify this by looking at the Explorer and confirming that the folder node\_modules is present.

![](<.gitbook/assets/Screenshot 2022-01-26 202143.png>)



That's it, our IDE should now be all set up and ready for us to create our first NFTs.
