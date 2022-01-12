# Setting up your IDE

This guide uses Microsoft's Visual Studio Code (VS Code) for its IDE. Other IDEs will be added in the future to support different operating systems.



### Install VS Code

The first thing we need to do in install VS Code. Find the executeable you downloaded and run through the installation wizard. After it has finished installed you can launch it from your Windows start menu. You should see a screen like this.

![](<.gitbook/assets/VS Code First Run.png>)

### Clone Furpunks

Now we need to clone the Furpunks github repository to our system. To do that we need to open Terminal in VS Code. Click Terminal, New Terminal or Ctrl+Shift\_+'

![](<.gitbook/assets/Screenshot 2022-01-12 170054.png>)

In the terminal prompt we want to type the following follwed by return.



```
git clone https://github.com/Furpunks/generative-art
```



Click File Open Folder and browse to the newly downloaded folder from git which will be called ‘generative-art-opensource.git’

&#x20;

Tick the box ‘Trust the authors of all files in the parent folder’ and select ‘Yes, I trust the authors button’.

&#x20;

Change branch version to 3.

&#x20;

npm install

npm install --global yarn

yarn add all

&#x20;

If you get the following error:

cannot be loaded because running scripts is disabled on this system.

You will need to open command prompt as Administrator, then type in the following and hit return:

Powershell Set-ExecutionPolicy RemoteSigned

&#x20;

&#x20;

&#x20;

Copy in layers

In terminal run: node index.js

&#x20;

Tips:

To expand the json file into a readable format press ‘shift + alt + f’
