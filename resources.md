---
description: How to collect resources in Sunflower Farmers.
---

# Resources

Most farmers begin by planting and harvesting to earn Sunflower Tokens. However, there comes a time in a farmer's career when they want to move onto more lucrative ventures and start gathering wood, stone, iron ore and other valuable materials.

Sunflower Farmers is based on a composable design which allows developers and game designers to create and launch an endless range of resources that can be mined, chopped, fished, gathered and much more. Each resource requires a specific tool in order to be gathered. These tools can be crafted using a range of other resources in the game.

### KIP20 Tokens

Under the hood each resource is designed as an ERC20 contract. This means if you chop wood you can freely trade it between farms or on open exchanges. You have complete ownership of what you collect in the game! The aim is to create a game that functions like a real world economy with silver, plutonium, gas, coal, solar and all the natural market economics that come with it.

## How to gather a resource?

For this example we will explore how to chop and collect wood.&#x20;

Craft an axe - In order to chop a tree you must first craft an axe. You can do so by going to the Blacksmith and clicking 'Craft'

![](<.gitbook/assets/image (8).png>)

When crafting an item ensure that you have the required resources. Some tools require a range of different materials. An axe is the most basic item in Sunflower Farmers and requires just $1 Sunflower Token.

{% hint style="info" %}
Tip: Craft more than 1 item at a time. Whether you craft 1 or 100 the gas fee will remain the same. \~$0.003
{% endhint %}

![](<.gitbook/assets/image (12).png>)

Once you have crafted an axe you can click on the wood chopper at the top of the farm.

![](<.gitbook/assets/image (4).png>)

Choose how many axe you want to use:

* 1 axe would yield between 3-5 pieces of wood.
* 3 axe would yield between 9-15 pieces of wood.

You can refer to the resource guide below to see the return rates on resources. Once you click 'Chop' you will need to confirm a MetaMask transaction. This costs around \~$0.002 and takes around 15-20 seconds before it is validated.

![](<.gitbook/assets/image (2).png>)

{% hint style="success" %}
Congratulations! You have collected your first wood. You can view this inside of your inventory or in the Blacksmith menu. Now you explore and craft new items and NFTs!
{% endhint %}

### Tree Growth <a href="#tree-growth" id="tree-growth"></a>

Each time you use an axe it weakens the tree and you need to wait for it to grow back. If it is a stump you will need to wait some time for it to grow back before you can chop. You can refer to the different replenish rates in the resource guide below.

### Resource Guide <a href="#resource-guide" id="resource-guide"></a>

Each resource is a unique contract that has its own rules and replenishes at a different rate. Some resources yield higher returns and some resources take longer to replenish.

| Name                                                                                                                                                                                                                                                                                     | Requires                                                                                                                                                                                                                                | Output                                                                                                                                                                                                                                                                                         |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><img src="https://docs.sunflower-farmers.com/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdunBb1X4ZSri9eSiAH%2Fuploads%2Fhns6mW464n8GmCPpva2i%2Fx2VKs3J_4x.png?alt=media&#x26;token=40a57d1f-b08b-41b4-88f0-3b1d4453176d" alt="">Tree</p><p>​​Takes 1 hour to grow back.</p>  | ![](https://docs.sunflower-farmers.com/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdunBb1X4ZSri9eSiAH%2Fuploads%2FC99TT7zMpKsq8eRDKm5B%2FAwkAPuw\_11x.png?alt=media\&token=018072b4-95bb-4899-a277-61880c3421e7)Axe           | <p><img src="https://docs.sunflower-farmers.com/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdunBb1X4ZSri9eSiAH%2Fuploads%2FcIdZxhAueQiaRKLyp07r%2Fnp5wvWy_14x.png?alt=media&#x26;token=c4f41ab6-8ab7-4b89-a4b3-c987f4948b9a" alt="">3-5 pieces of wood</p><p>​Used for crafting.​</p> |
| <p><img src="https://docs.sunflower-farmers.com/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdunBb1X4ZSri9eSiAH%2Fuploads%2F9PE6dZ19TKon8fFmPKsa%2FP1bfTuY_11x.png?alt=media&#x26;token=985a5850-d7df-4c59-bf65-e70f415818c4" alt="">Quarry​</p><p>Takes 2 hour to grow back</p> | ![](https://docs.sunflower-farmers.com/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdunBb1X4ZSri9eSiAH%2Fuploads%2FD3ZbHVH4EuPTF1AMzs71%2FmCirM87\_12x.png?alt=media\&token=924576d5-0456-4258-a598-2fc1f5b85cfe)Wood pickaxe  | <p><img src="https://docs.sunflower-farmers.com/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdunBb1X4ZSri9eSiAH%2Fuploads%2FKEc9AQzDVTFnIzHsMCoU%2Fw65XqLT_12x.png?alt=media&#x26;token=700c6926-d55e-4f90-af10-e4e0d03b448d" alt="">2-4 pieces of stone​</p><p>Used for crafting​</p> |
| <p><img src="https://docs.sunflower-farmers.com/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdunBb1X4ZSri9eSiAH%2Fuploads%2FAgfibvTvhUhWbV1y6nG0%2FMineral00004.png?alt=media&#x26;token=5af7cd07-4c8a-4518-8845-bff71cb8159b" alt="">Iron Mine​</p><p>4 hours</p>               | ![](https://docs.sunflower-farmers.com/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdunBb1X4ZSri9eSiAH%2Fuploads%2FLdMqbZ4dR8m0wzia9Cjl%2FLZedx6H\_12x.png?alt=media\&token=41098d2b-c121-4915-ad90-63ff846ed048)Stone pickaxe | ![](https://docs.sunflower-farmers.com/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdunBb1X4ZSri9eSiAH%2Fuploads%2FnYqygqwAWspMq2QbarrO%2Fore.png?alt=media\&token=6c084e71-1ca0-4f68-ac38-b405f073a302)3-5 Iron ore                                                                  |
| <p><img src="https://docs.sunflower-farmers.com/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdunBb1X4ZSri9eSiAH%2Fuploads%2FvvKpGAGGVdObzS6gqT7n%2Fgold.png?alt=media&#x26;token=e75df85e-bc88-4967-a246-50a30db80817" alt="">Gold mine </p><p>12 hours</p>                      | ![](https://docs.sunflower-farmers.com/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdunBb1X4ZSri9eSiAH%2Fuploads%2FoWTcEeequdEhw8EHe6KX%2Firon\_pickaxe.png?alt=media\&token=4846c72a-f5aa-43a7-8785-cb762ffa7f24)Iron Pickaxe | ![](https://docs.sunflower-farmers.com/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdunBb1X4ZSri9eSiAH%2Fuploads%2FuIMpWBt3dyUNKKWqf5hP%2Fgold\_ore.png?alt=media\&token=6f84ca69-b018-4965-a562-b466fc7036f7)1-2 Gold ore                                                            |
| <p><img src="https://docs.sunflower-farmers.com/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdunBb1X4ZSri9eSiAH%2Fuploads%2F5yMb0PRBLe6LCki75mIE%2Fchicken.png?alt=media&#x26;token=352ac939-2cbf-46f0-bf0f-b475e68b1cb9" alt="">Chicken</p><p>24 Hours</p>                      | -                                                                                                                                                                                                                                       | ![](https://docs.sunflower-farmers.com/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MdunBb1X4ZSri9eSiAH%2Fuploads%2Fj9xy4c1VZyBYbpRrPPlw%2Fegg.png?alt=media\&token=5be12c65-c1b7-4072-ad37-5cc015064b55)1 egg per chicken                                                             |
| More coming soon...                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                |

## Addresses <a href="#addresses" id="addresses"></a>

Below is a list of addresses for the ERC20 resources & tools as well as the ERC721 (NFT) items.

| Name             | Address                                    | Link                                                                                                                                                                     |
| ---------------- | ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| $SFF             | 0x89C7Fc93bb78dDF809E3F317501563a6323E22CD | [https://www.oklink.com/en/oec/tokenAddr/0x89c7fc93bb78ddf809e3f317501563a6323e22cd](https://www.oklink.com/en/oec/tokenAddr/0x89c7fc93bb78ddf809e3f317501563a6323e22cd) |
| Axe              | 0xb891f2F11851380746C671F5E19F626436E32496 | [https://www.oklink.com/en/oec/tokenAddr/0xb891f2F11851380746C671F5E19F626436E32496](https://www.oklink.com/en/oec/tokenAddr/0xb891f2F11851380746C671F5E19F626436E32496) |
| Wood pickaxe     | 0x60Cb7e24d1fAf18206EEb89e523Bf130f15eE404 | [https://www.oklink.com/en/oec/tokenAddr/0x60Cb7e24d1fAf18206EEb89e523Bf130f15eE404](https://www.oklink.com/en/oec/tokenAddr/0x60Cb7e24d1fAf18206EEb89e523Bf130f15eE404) |
| Stone pickaxe    | 0x2B322bE31Eac05d9D8E3bae25DaB21B129d37A96 | [https://www.oklink.com/en/oec/tokenAddr/0x2B322bE31Eac05d9D8E3bae25DaB21B129d37A96](https://www.oklink.com/en/oec/tokenAddr/0x2B322bE31Eac05d9D8E3bae25DaB21B129d37A96) |
| Iron Pickaxe     | 0x9771D2d8d22BEBBc1826909F8453A54AF599d2E8 | [https://www.oklink.com/en/oec/tokenAddr/0x9771D2d8d22BEBBc1826909F8453A54AF599d2E8](https://www.oklink.com/en/oec/tokenAddr/0x9771D2d8d22BEBBc1826909F8453A54AF599d2E8) |
| Chicken          | 0x24DBC19f6c5231DA92321983d47b303CF140B6c9 | [https://www.oklink.com/en/oec/tokenAddr/0x24DBC19f6c5231DA92321983d47b303CF140B6c9](https://www.oklink.com/en/oec/tokenAddr/0x24DBC19f6c5231DA92321983d47b303CF140B6c9) |
| Egg              | 0x8f6968A43cDdFBB3307B6F23dc93ed3fF6310828 | [https://www.oklink.com/en/oec/tokenAddr/0x8f6968A43cDdFBB3307B6F23dc93ed3fF6310828](https://www.oklink.com/en/oec/tokenAddr/0x8f6968A43cDdFBB3307B6F23dc93ed3fF6310828) |
| Sunflower Statue | 0x5f38e933Ff552C6666C4810c940E20711d5274a1 | [https://opensea.io/collection/sunflower-farmers-statue](https://opensea.io/collection/sunflower-farmers-statue)                                                         |
| Scarecrow        | 0x25FA3D7fC37186bb3Cab8b8Cfb17F09eC583eC9E | [https://opensea.io/collection/sunflower-farmers-scarecrow](https://opensea.io/collection/sunflower-farmers-scarecrow)                                                   |
| Christmas Tree   | 0x128E8E0d51dC938f901f9d1FD03799E1af12aAf3 | [https://opensea.io/collection/sunflower-farmers-christmas-tree](https://opensea.io/collection/sunflower-farmers-christmas-tree)                                         |
| Chicken Coop     | 0x84F3f92E9C9f41e4aaB842Ba4665cA84273e08c3 | [https://opensea.io/collection/sunflower-farmers-chicken-coop](https://opensea.io/collection/sunflower-farmers-chicken-coop)                                             |
| Golden Egg       | 0x90658195ABeFFDDDF2a2a52e76328191a027C256 | [https://opensea.io/collection/sunflower-farmers-golden-egg](https://opensea.io/collection/sunflower-farmers-golden-egg)                                                 |
| OG Potato Statue | 0xFdd285FaC915416d577c60f3351bd527d6180334 | [https://opensea.io/collection/sunflower-farmers-og-potato-statue](https://opensea.io/collection/sunflower-farmers-og-potato-statue)                                     |
| Wood             | 0x37bd5138402F994c7Be9BEebE45fc5aAFf5e3c64 | [https://www.oklink.com/en/oec/tokenAddr/0x37bd5138402F994c7Be9BEebE45fc5aAFf5e3c64](https://www.oklink.com/en/oec/tokenAddr/0x37bd5138402F994c7Be9BEebE45fc5aAFf5e3c64) |
| Stone            | 0x85c31a63939804BC6feFDE9F752338edcCc6F872 | [https://www.oklink.com/en/oec/tokenAddr/0x85c31a63939804BC6feFDE9F752338edcCc6F872](https://www.oklink.com/en/oec/tokenAddr/0x85c31a63939804BC6feFDE9F752338edcCc6F872) |
| Iron             | 0xf9030a3a5259E3aB8A1c7f98924BAC3882dfc2e8 | [https://www.oklink.com/en/oec/tokenAddr/0xf9030a3a5259E3aB8A1c7f98924BAC3882dfc2e8](https://www.oklink.com/en/oec/tokenAddr/0xf9030a3a5259E3aB8A1c7f98924BAC3882dfc2e8) |
| Gold             | 0xCc3E026217179F29317344D7691A7f608aa9437a | [https://www.oklink.com/en/oec/tokenAddr/0xCc3E026217179F29317344D7691A7f608aa9437a](https://www.oklink.com/en/oec/tokenAddr/0xCc3E026217179F29317344D7691A7f608aa9437a) |
