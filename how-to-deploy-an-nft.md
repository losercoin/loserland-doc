# How to deploy an NFT?

{% hint style="info" %}
This guide is how to deploy a normal craftable NFT in the game.\
\
If you want to deploy a Community Item which you earn 16%, please contact the team on telegram.
{% endhint %}

The purpose of this guide is to explore how to deploy a new NFT on Sunflower Farmers. The game is open source and we always encourage new designers and developers to introduce new features and launch NFTs in the game.

Sunflower Farmers is composable and extensible which means anybody can introduce a new crafting recipe for an NFT

#### Requirements

1. A pixel art decoration - Create a piece of pixel art you think will look good on the farm For this example we are using a scarecrow
2. OKT - You will need around $0.10 to deploy a smart contract and link it to the game
3. Sunflower Farmers project cloned - see here [https://github.com/losercoin/sunflower-farmers#how-to-run](https://github.com/losercoin/sunflower-farmers#how-to-run)
4. Basic programming skills - Most of this guide involves copy pasting code but you should have a good understanding of Javascript in case you need to debug an issue.

If you lack the programming skills or need help in this area reach out the admin on the telegram and we will help launch your creation.

{% hint style="info" %}
In the future you will be able to launch a NFT inside of the game. For now it requires a bit of knowledge around solidity and deploying contracts
{% endhint %}

## How do NFTs work?

In Sunflower Farmers all in-game items enforce the KIP20 and KIP721 (NFT) protocols. This means players have ownership of the items they collect and can swap and trade them if they want to. An NFT in Sunflower Farmers can be used for in-game features, as a decoration or even as a material that is needed in another crafted recipe.

Each decoration that gets released is an NFT deployed onto the Polygon network. Most NFT (KIP721) smart contracts allow the owner to mint new NFTs. The one key difference with Sunflower Farmer's NFTs is that ownership is handed over to the base Sunflower Farmers contract. This means that only the game has permissions to mint the NFTs and even the developer cannot sneakily create some.

![](<.gitbook/assets/image (10).png>)

## Deploying a NFT Smart Contract

In this section we will explore how to deploy a smart contract onto the OKEx Blockchain. By the end of this section you will have successfully deployed your first NFT.

For this example we will deploy a Scarecrow.sol contract. You will see the word Scarecrow used in a few places. In these parts you will want to use your own unique name for your NFT (e.g. Flowers, Trophy, etc.)

For this tutorial we will reuse the Statue.sol smart contract ([https://github.com/losercoin/sunflower-farmers/blob/main/src/contracts/Statue.sol](https://github.com/losercoin/sunflower-farmers/blob/main/src/contracts/Statue.sol)) and make a few key changes. This smart contract uses the Open Zeppelin ERC721 class which includes a range of helpers and standards that turn a contract into an NFT.

Each NFT can have unique capabilities, different supplies and other cool rules. For this guide we will use a basic contract which has a maximum supply and only allows 1 per account. In the future feel free to invent any sort of NFT with cool features.

In order to compile and deploy the contract head over to [https://remix.ethereum.org/](https://remix.ethereum.org). This is a free solidity compiler that lets us compile and deploy directly onto the OKEx blockchain. You will want to have the Statue.sol smart contract ready to copy paste.



In Remix IDE create a new file in the contracts directory named after your NFT. In this example we will call it Scarecrow.sol

![](<.gitbook/assets/image (13).png>)

Next copy paste the code from Statue.sol code into this file

Update the name and symbol you want. This will appear on NFT platforms like OpenSea.

```solidity
constructor() public ERC721("Sunflower Farmers Scarecrow", "SFC") {
        minter = msg.sender;
}
```

Update the tokenUri to point to URL hosted by [sunflower-farmers.com](http://sunflower-farmers.com). This is where platforms like OpenSea will look for the hosted image.

```jsx
function tokenURI(uint256 tokenId) public view virtual override returns (string memory) {
        require(tokenId <= 5000);

        return "<https://sunflower-farmers.com/play/nfts/scarecrow/metadata>";
    }
```

Change the total supply of your NFT. For the scarecrow we only want a supply of 5000. You will also want to update this value down in the `mint` function.

Change to the compiler tab on the left and compile the smart contract

![](<.gitbook/assets/image (1).png>)

Change to the Deploy tab on the lift. Under environment change to Injected Web3 - This allows us to connect to OEC. Switch to the Injected Provider and connect to the OKEx Blockchain

![](<.gitbook/assets/image (14).png>)

Deploy the smart contract. This will open up Metamask and ask you to confirm the transaction. It usually takes around 10-30 seconds for this to succeed.

You will see your contract appear on the left hand side. Copy the address as you will need this for later and store it somewhere.

On the left hand side drop down the contract and find the passMinterRole function. This is the stage where we pass ownership over to the game. Copy paste the Sunflower Farmer contract <> and click the passMinterRole button. This will open up a new Metamask transaction that you will need to confirm.

{% hint style="success" %}
Congratulations, your NFT has been deployed and is publicly available on the Polygon blockchain! Next up we will show you how to link it with the game.
{% endhint %}

The last step is to include the compiled code into the game's repo.

![](<.gitbook/assets/image (11).png>)

1. We will need to grab the ABI JSON file that is created when Scarecrow.sol is compiled. You can click the 'ABI' button to copy these contents. Inside of the sunflower-farmers repo you will want to create a new file in `src/abis` called `Scarecrow.json` and paste in the `Scarecrow.json` contents
2. Next you will also want to create a new file in `src/contracts` called `Scarecrow.sol` and paste in the contract you created. This is not necessary but given the open source nature of the game it is good to help future builders understand the contract

## Creating a recipe for your decoration

After all your hard work we don't want farmers to get your decoration for free! In this section we will create the crafting recipe that is required for your NFT to be crafted using a range of resources..

To create a crafting recipe we will need to interact with the Sunflower Farmers smart contract and call the `createRecipe` method. In order to do so we will import the Farm.sol contract into Remix IDE. Remix IDE has cool functionality where you can communicate with contracts already deployed on the blockchain even if you did not deploy them yourself!

So let's set up the farm contract in Remix

First up create a new file named Token.sol in Remix IDE and copy the contents of [https://github.com/losercoin/sunflower-farmers/blob/main/src/contracts/Token.sol](https://github.com/losercoin/sunflower-farmers/blob/main/src/contracts/Token.sol).

Change to the compiler tab and ensure the compiler version is set to 0.7.6 and click compile

![](<.gitbook/assets/image (5).png>)



Create a new file Farm.sol in Remix IDE and copy the contents from [https://github.com/losercoin/sunflower-farmers/blob/main/src/contracts/Farm.sol](https://github.com/losercoin/sunflower-farmers/blob/main/src/contracts/Farm.sol)

Change to the compiler tab and ensure the compiler version is set to 0.7.6 and click compile

Switch over to the deploy tab and ensure you are on the Injected Provider network and connect to the Polygon Blockchain

First change the contract to the FarmV2 -contracts/Farm.sol

![](<.gitbook/assets/image (6).png>)

Since the contract is already deployed we can use the 'At Address' feature which will connect us to the Sunflower Farmer contract. In the input next to 'At Address' input the game's smart contract address - 0x80b399335c32F0f28bd8F4bF43a044EAebdd5013. Once ready click the button 'At Address'. You will then see the contract pop up below.

![](<.gitbook/assets/image (3).png>)

Prepare the ingredients for your decoration. A decoration can be created from any KIP20 resource or other KIP721 resource in the game. You can find the list of address here [https://github.com/losercoin/sunflower-farmers/blob/main/src/dapp/types/crafting.ts](https://github.com/losercoin/sunflower-farmers/blob/main/src/dapp/types/crafting.ts).&#x20;

The Scarecrow will require 10 sunflower tokens and 50 wood. Since there are no decimals in Solidity tokens actually use very large numbers. In this case 50 tokens are actually 50000000000000000000 This is known as wei in the ethereum virtual machine. You can calculate the appropriate wei using the following calculator [https://eth-converter.com/](https://eth-converter.com).

| Name | Address                                    | Amount               |
| ---- | ------------------------------------------ | -------------------- |
| Wood | 0x37bd5138402F994c7Be9BEebE45fc5aAFf5e3c64 | 50000000000000000000 |
| SFF  | 0x89C7Fc93bb78dDF809E3F317501563a6323E22CD | 10000000000000000000 |

Expand the Farm contract and find the method called `createRecipe`For the first argument you will want to include the address of the NFT you have just deployed. The second argument includes an array of ingredients that are needed for the recipe.

\[\["0x37bd5138402F994c7Be9BEebE45fc5aAFf5e3c64", "100000000000000000000"],\[ "0x89C7Fc93bb78dDF809E3F317501563a6323E22CD", "50000000000000000000"]]

{% hint style="info" %}
Don't forget the quotation marks around these values.
{% endhint %}



Once you are ready you can click the \`createRecipe\` button and connect your NFT to the game.

{% hint style="success" %}
Congratulations, your recipe is now live on the blockchain! You can test this out by calling the `getRecipe` method with the address of the NFT you deployed.
{% endhint %}

Next up we will show you how to add your piece of art to the game and allow farmers to craft the item at the Blacksmith.

## Allowing Farmers to craft the NFT

In this section we will add the front-end piece required to allow farmers to craft your item. By the end of this step players will be able to view the recipe, craft the NFT and then view the item on their farm. Let's get started!

Before we get started we will need to set up the assets that are required to display the NFT in the game.

1. Copy your image file of your NFT into the `src/dapp/images/ui` directory. In our case we will copy across our scarecrow.png file
2. Create a new folder under `public/nfts/scarecrow` - When deployed, this is where your NFT image will be stored in a publicly accessible URL that was used as the tokenUri in your NFT smart contract - [www.sunflower-farmers.com/nfts/scarecrow/scarecrow.png](http://www.sunflower-farmers.com/nfts/scarecrow/scarecrow.png)
   1. Copy your image file into this directory - `public/nfts/scarecrow/scarecrow.png`
   2. Create a new file called `metadata` with no file extension and add the following. This file is used by OpenSea when displaying the description and the image that is shown. You will want to include a useful description, name and link to the publicly accesible URL where your image will be hosted.

```json
{
"description": "A collectable scarecroww in Sunflower Farmers.",
"external_url": "https://sunflower-farmers.com/play",
"image": "https://sunflower-farmers.com/play/nfts/scarecrow/scarecrow.png",
"name": "Scarecrow"
}
```

Next up we will update some variables in our game. In `crafting.ts` we will want to do 2 things:

1. On the `Item` interface update the name field to also accept a string of "Scarecrow" (or a similar name for your item)
2. add a new item to the `recipes` array.

```javascript
  {
    name: "Scarecrow",
    abi: Scarecrow, // Imported from "../../abis/Scarecrow.json"
    description: "Helps keep the crows away",
    image: scarecrow, // Imported from "../images/ui/scarecrow.png"
    type: "NFT",
    address: "0x143Ba32499065b5F89c518d5B75a38F3529cE324", // Your NFT address
    ingredients: [
      {
        name: "$SFF",
        amount: 10,
        image: coin,
      },
      {
        name: "Wood",
        amount: 50,
        image: wood,
      },
    ],
    supply: 5000,
  },
```

You will also need to initialise the default amount of scarecrows in `DEFAULT_INVENTORY` at the bottom of the file to 0.

{% hint style="success" %}
If you run the project with `yarn start` and go to the Blacksmith you should now see your item there and be able to craft it! This is getting exciting.
{% endhint %}

Now it is time to show the item on the farm once it has been crafted. In order to do so we head over to the NFTs file which decide when and where on the farm to display.

Inside of `NFTs.tsx` import your scarecrow png and add the following line.

```tsx
<div id="scarecrow">
    {inventory["Scarecrow"] > 0 &&
        <img src={scarecrow} alt="scarecrow" />
    }
</div>
```

Head into `NFTs.css` to add styles and decide where on the farm it should live. Your CSS will change depending on the size of your image and where you want it to live.

```css
#scarecrow {
  grid-column: 9;
  grid-row: 7;
  z-index: 99;
}

#scarecrow > img {
  width: 60%;
  position: relative;
  left: 20%;
  bottom: 30%;
}

```

{% hint style="info" %}
And that's it! Your NFT has joined the Metaverse. Congratulations!

Your next steps are to open a Pull Request that the builders can review so we can release your glorious work to the entire community!
{% endhint %}
