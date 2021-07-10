# Everstone NFTs
Everstones are 🟣 [PURPLE](https://wax.bloks.io/tokens/PURPLE-wax-purplepurple)-backed NFTs that send out 🔵 [BLUX](https://wax.bloks.io/tokens/BLUX-wax-bluxbluxblux) or Blu Ups daily. One Everstone is backed by between 1-64 PURPLE, and has a daily harvest between 1-432 BLUX or Blu Ups. When an Everstone is destroyed, the PURPLE is sent back to the Everstone's owner.

> [👁️ See an Everstone in the wild](https://wax.simplemarket.io/products/asset/100000016933308)


When you own an Everstone NFT, you get the choice to automatically Up chosen content every day or take a set reward in BLUX everyday. *Switching reward type will pause payment by 1 day.* 

> Currently, only direct BLUX payments are available. 

The more PURPLE an Everstone holds, the more efficient it becomes. 

# Everstone Harvest Levels + Rewards

| 🟣 PURPLE staked  | Daily Reward in Blu Ups or BLUX | Everstone Efficiency |
| :----:  | :-------------------: | :---------------: |
| 1         | 1                   | 100%            | 
| 2         | 3                   | 150%            | 
| 3         | 5                   | 167%            | 
| 4         | 7                   | 175%            | 
| 8         | 16                  | 200%            | 
| 12        | 30                  | 250%            | 
| 16        | 48                  | 300%            | 
| 32        | 144                 | 450%            | 
| 64        | 432                 | 675%         🧠 | 

> Each Everstone level will have unique art, revealed at a later date. We currently have a wonderful placeholder. 

## Everstone Release 
Everstone supply is limited via a trickling supply to avoid any one person/group controlling cXc.world's [Top Charts](Top-Charts.md). We will release already-staked Everstones for auction on [Simple Market](https://wax.simplemarket.io/explorer/main?skip=0&limit=20&searchString=everstone&locale=en) at regular intervals, as well as for direct sale on Simple Market and [Alcor](https://wax.alcor.exchange/nft-market). PURPLE-backed Everstones are sold for face value at the current cXc sell price of PURPLE (Currently 20 WAX/PURPLE). 

> We no longer plan to distribute non-backed Everstones, as this is harder for us to sort through.  

## Empowering Creators 👨‍🎤🎤
Everstones are particularly useful for creators, as daily Ups on their content gives them exposure on the mapp and [Top Charts](Top-Charts.md).

## Empowering Fans 🧝‍
Fans may collect BLUX to Blu Up their favorite artist's latest release. This can really help new artists, because local chart topping gives way to bigger charts, earning more BLUX from Sol Ups, new opportunities, and measurable exposure. 


# How it Works

Everstones are a [Simple Assets](https://wax.bloks.io/account/simpleassets) NFT.

Everstones store info (mdata) on whether the owner wants BLUX or Blu Ups, and if Blu Ups is chosen, the owner can also specify which content to send the daily Blu Ups to. 

Once a day, we check how much PURPLE is staked on each Everstone, and if it's over 1, we distribute the owed Blu Ups or BLUX. There are no fractional Ups or BLUX, so rounding down to each level is used to calculate the rewards. For example, if you had 64 or 67 PURPLE staked to one Everstone, both would give 432 Blu Ups per day. We plan to provide a UI to help you avoid over-staking. 

If you choose BLUX payments, weekly or monthly recharge of Solar Disk may be required to receive the full amount. This is TBD as we consider what's best for all stakeholders, currently there is no restriction. 




# Staking

## Staking PURPLE to an Everstone
Staking additional PURPLE to an Everstone is done via a `transfer` of PURPLE to [simplebacked](https://wax.bloks.io/account/simplebacked) with a memo of the Everstone's Simple Assets NFT ID (ex 100000005145313). This **will** be available through the UI of cXc.world (Beta). 


## Unstaking from Everstones
Everstones will automatically return all tokens staked when burned. If an Everstone is transferred and then burned, the owner at the time of burning will receive all tokens backed on the Everstone. Only the current owner of the Everstone can stake more PURPLE to it, so you don't need to worry about typing the wrong ID, as the `simplebacked` contract will return any PURPLE sent without an ID of an Everstone you currently own. 



# Tech + Contracts 🔌

Everstones are Simple Assets NFT backed in Purple on a [simpleassets](https://wax.bloks.io/account/simpleassets) NFT using the [simplebacked](https://wax.bloks.io/account/simplebacked) contract to ensure all Everstones return their PURPLE to the rightful owner upon burning. ([example tx](https://wax.bloks.io/transaction/7a390ecf24f97e57482db730c2cfdc001d8bcda6a98d45fb7427d2afdcfdc052?tab=traces))  


Everstones store several pieces of data we use to ensure you get paid fairly. All Everstone data is `mdata` or mutable data, so it can be updated by our `currentxchng` account.  
 
Here's all the mdata on an Everstone.  

```javascript
{
  "name":"Everstone",
  "img":"QmbYghSQZRU8vTxU9nCsiJQ8hgV2g8PkvvNhY32idz42kn",
  "level":"6",
  "staked_purple":"12",
  "daily_blux":"30",
  "lifetime_blux":"360",
  "last":"09-07-2021",
  "todays_blux":"30"
}
```

> [See it on an Everstone](https://wax.simplemarket.io/products/asset/100000016933308)

Each time an Everstone is paid, the `mdata` is updated to reflect the payment in the `lifetime_blux`, `todays_blux`, and `last` field. The `last` field hold the date of the last payment, and in the event you don't receive a payment for any reason, *you'll be paid all you are owed in the next payment.*  



> Please note: *Everstones will emit Blu Ups* not considered in the Top 64 PURPLE rewards system, but displayed in the default Top Charts. Blu Ups help content get exposure, which may lead to organic Sol Ups + PURPLE rewards.
