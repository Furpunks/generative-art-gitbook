# Assets

Assets are probably one of, if not _the_, most important part of creating NFTs. Without good assets your final image will not look very good. I'm terrible at artistic endeavours so don't judge my Krypto Kitty NFTs too harshly!

The Furpunks repo has four pre loaded assets for you to play with. You can view them under the 'input' folder in Explorer. You will see Background, Body Colour, Colar and Face.

![](<.gitbook/assets/Screenshot 2022-01-12 181137.png>)

Each asset folder has three sub folder, Common, Rare and Super Rare. The sub folders are refered to classifications. Additional classifications can be added and will be covered in a follow up guide.

To view one of the assets click on the folder and classification next to the corresponding one. Below you will see I have selected Brown.png from the Common classification folder under the Body Colour asset.

![](<.gitbook/assets/Screenshot 2022-01-12 181441.png>)

### Configuration Settings

Now that we have a set of assets we would like to create our NFTs from, let's have a look at modifying our config file.

Branch out the input folder and click on config.js in Explorer. We will now see our first bit of code on the right side similar to the image below.

![](<.gitbook/assets/Screenshot 2022-01-12 182110.png>)

We want to scroll down to the section that begins with:

/\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

BEGIN CONFIG

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*/

Here we will find all the main configuration values that we can adjust to fit our NFTs.



I will explain what each line does in a follow up.



### NFT Metadata

Our NFTs need metadata so that an NFT marketplace is able to understand what traits each NFT has had applied.

During the process of creating our NFTs two main types of JSON files will be created.

A main .json file called \_metadata.json and a .json file for each NFT.png file created. This allows us to cater for multiple types of NFT marketplace platforms.

The first .json file \_metadata.json contains a complete list of all the attributes applied to each individual NFT.

The additional .json files contain metadata specific only to their corresponding NFTs.

### Generate NFTs Already!

Welcome to the fun part. Lets generate some NFTs with our assets.

To do so, open Terminal and type in the following:

`node index.js`

This command is used to tell nodejs to execute our program using index.js which in turn calls config.js. You should see similar output in the Terminal window below and if you open the output folder in Explorer you will see the NFTs that have been created.

![](<.gitbook/assets/Screenshot 2022-01-12 182743.png>)

If we click on one of the .png files in Explorer we can see what was created. In my run I had the following NFT generated, yours will probably look different as they are created randomly from the assets we have specified.

![](<.gitbook/assets/Screenshot 2022-01-12 183429.png>)

We can also view the metadata by clicking on the associated .json file. This is what mine looks like for the example above.

![](<.gitbook/assets/Screenshot 2022-01-12 183730.png>)

If your json is appearing all on a single line you can have VS Code format it correctly for you by hitting 'shift+alt+f'

