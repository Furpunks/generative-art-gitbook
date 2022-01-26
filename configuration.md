# Configuration

### Configuration Settings

Now that we have a set of assets we would like to create our NFTs from, let's have a look at modifying our config file.

Branch out the input folder and click on config.js in Explorer. We will now see our first bit of code on the right side similar to the image below.

![](<.gitbook/assets/Screenshot 2022-01-26 210426.png>)

For this walkthrough we will be sticking to the .eth Network as defined in the const network. I will cover Solana in a follow up guide.

There are a few areas that you will need to update for your specific project.

### Project Description

The first values to change are are namePrefix and description. The default values for Furpunks are:

```
const namePrefix = "Furpunks!";
const description = "Pixel cats with attitude.";
```



### Number of NFTs to Create

An NFT collection wouldn't be much use if you couldn't specify how many NFTs to create! Find growEditionSizeTo. In order example we have it configured to 5 which will auto generate 5 unique NFTs using our assets in the layers folder. Change 5 to however many you would like to create.

```
growEditionSizeTo: 5,
```



### Layer / Asset Order

Further down you will find a section for layersOrder like so:

```
layersOrder: [
  { name: "Background" , },
  { name: "Body Colour" },
  { name: "Eyes" },
  { name: "Colar" },
],
```

The layers order function defines two things. First, it lists all of the folders that we want our script to look in for assets in order to generate our NFTs. If you wanted to include a new layer which had additional assets you would need to include that folder name in this list. For example, if I wanted to add Hats my code would look like this:

```
layersOrder: [
  { name: "Background" , },
  { name: "Body Colour" },
  { name: "Eyes" },
  { name: "Colar" },
  { name: "Hats" },
],
```

Secondly, the layer function defines which layers are applied to our image first. This is important as if we specified Background last in the order, it would completely overwrite our NFT with just the background layer. When it comes time to make your own NFTs and they come out looking odd, this is one of the first places to look to make sure that the layer is being applied in the correct order so that it isn't being over laid or hidden by a previous layer.



### NFT Size

To set the expected size of the final NFTs be sure to change the width and height as seen here:

```
const format = {
    width: 150,
    height: 150,
    smoothing: false,
};
```



### NFT Metadata

Our NFTs need metadata so that an NFT marketplace is able to understand what traits each NFT has had applied.

During the process of creating our NFTs two main types of JSON files will be created.

A main .json file called \_metadata.json and a .json file for each NFT.png file created. This allows us to cater for multiple types of NFT marketplace platforms.

The first .json file \_metadata.json contains a complete list of all the attributes applied to each individual NFT.

The additional .json files contain metadata specific only to their corresponding NFTs.

### Generate NFTs Already!

Welcome to the fun part. Lets generate some NFTs with our assets.

To do so, open Terminal and type in the following:

`node run build`

This command is used to tell nodejs to execute our program using main.js which in turn calls config.js. You should see similar output in the Terminal window below and if you open the output folder in Explorer you will see the NFTs that have been created.

![](<.gitbook/assets/Screenshot 2022-01-26 212441.png>)

If we expand build / images and click on one of the .png files in Explorer we can see what was created. In my run I had the following NFT generated, yours will probably look different as they are created randomly from the assets we have specified.

![](<.gitbook/assets/Screenshot 2022-01-26 212559.png>)

We can also view the metadata by clicking on the associated .json file. This is what mine looks like for the example above.

![](<.gitbook/assets/Screenshot 2022-01-26 212646.png>)

We can see that my Kitty has a White background, Brown body, Green eyes and blue collar.



If your json is appearing all on a single line you can have VS Code format it correctly for you by hitting 'shift+alt+f'
