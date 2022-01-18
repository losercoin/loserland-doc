# Tokenomics

[https://www.oklink.com/en/oec/tokenAddr/0x89c7fc93bb78ddf809e3f317501563a6323e22cd](https://www.oklink.com/en/oec/tokenAddr/0x89c7fc93bb78ddf809e3f317501563a6323e22cd)

Sunflowers are in high demand and we are recruiting more farmers to help satisfy this growing global demand. The game has a built-in supply & demand mechanism that controls the underlying tokenomics. The aim is to reward farmers who are early to the game and drive scarcity.

When rewards are earned in the game, players receive the underlying KIP20 token. As more people farm and the overall supply increases, the rewards also lessen. This means someone playing in the early days will receive a significantly higher amount of rewards for harvesting a sunflower compared to someone in the future.

{% hint style="info" %}
You can think of this similar to Bitcoin Halving and how Bitcoin have become harder to mine after each halving event
{% endhint %}

The earlier you start farming, the more you will be rewarded as the supply increases. The below table examines the rewards for harvesting sunflowers. When the supply is less than 100, 000 farmers receive **$0.01** when they harvest a sunflower. On the other hand, when supply is between 100, 000 and 500, 000 farmers will only receive **$0.002** when they harvest a sunflower.

| Tokens in supply           | SFF per Sunflower Harvested |   |
| -------------------------- | --------------------------- | - |
| Less than 100, 000         | $0.02                       |   |
| Less than 500, 000         | $0.004                      |   |
| Less than 1, 000, 000      | $0.002                      |   |
| Less than 5, 000, 000      | $0.0004                     |   |
| Less than 10, 000, 000     | $0.0002                     |   |
| Less than 50, 000, 000     | $0.00004                    |   |
| Less than 100, 000, 000    | $0.00002                    |   |
| Less than 500, 000, 000    | $0.000004                   |   |
| Less than 1, 000, 000, 000 | $0.000002                   |   |
| More than 1, 000, 000, 000 | Total Supply / 10000        |   |

{% hint style="info" %}
A sudden increase in farmers would drive the supply high and could quickly change the rewards you receive per fruit. It is advised to pay attention to the current supply and plant fruits that can be harvested before the next halving window.
{% endhint %}

### Linear Growth after 1, 000, 000, 000

The more tokens that are generated, the harder they are to farm. In decades to come, when the token supply reaches 1 Trillion there will be no more 'halvening' periods. Instead the tokenomics will become linear and extremely scarce. \
\
Essentially a soft total supply limit exists at this point.

The in game market rate would be 100000000000000000000000. This means a sunflower would earn 1/100000000000000000000000 of SFF.&#x20;

### Buy & Upgrade Price

It is not only the rewards that lessen based on the supply. The seed price and price to upgrade a farm also lessen. This will ensure that new players still have a low barrier to entry and can begin making progress on their farms.

If you own a farm before a 'halving' event, your purchasing power will increase significantly. If you had $10 SFF when supply was 50,000 you would be able to by **10 Beetroots**. If the supply grew to 150, 000, that same $10 would be able to buy **100 Beetroots**

### Smart Contract Behaviour

You can view how this market price in the smart contract [here](https://github.com/losercoin/sunflower-farmers/blob/main/src/contracts/Farm.sol#L356)

## Rewards

To encourage Sunflower Token Hodlers, the game has a unique distributed reward system. It incentivises players to build their farms and invest into the game. Whenever tokens are spent on upgrades or crafting they go into a rewards pool that is owned by the game's smart contract.

Every 3 days you will be eligible to receive your rewards. The size of the reward depends on the size of your farm.

![](<.gitbook/assets/image (7).png>)

## Rewards

## The Halvening

As all dedicated farmers know, supply and demand can be a dangerous thing. When prices are high, fortunes can be made. But when prices are low, a lifetime of potato hustling can be lost. When the supply is getting nearer to a tipping point you will want to ensure you are ready!

When a new supply point is reached all in-game prices are fractionalized. This makes all tokens farmed prior to the event much more valuable than after the supply change. The table below illustrates a range of prices before and after the first tipping point.

| **Item**               | **Price at 499,999 tokens** | Price at 500,000 tokens |
| ---------------------- | --------------------------- | ----------------------- |
| Sunflower Seeds (Buy)  | $0.002                      | $0.001                  |
| Sunflower Plant (Sell) | $0.004                      | $0.002                  |
| First Farm Upgrade     | $0.2                        | $0.1                    |

As you can see it is **all in-game** prices that are affected by the change in supply. The aim is to keep all prices relative so new-comers can still have a balanced gameplay and improve their farms.

### What could go wrong?

You will want to be careful that you don't plant anything expensive right before a supply shift otherwise you could end up selling the plant at a loss. See the example below.

1. You plant a Beetroot for $0.2 SFF (Supply is 499, 900)
2. Supply increases to 500, 100
3. You harvest the same Beetroot for $0.1 SFF

In the above case you would end up losing $0.1 as the supply has increased for Beetroots and their price has dropped accordingly.

So, keep a close eye on the supply. Do you risk it and try squeeze out more of the high rewards or play it safe?
