# Soldisk NFTs 

<p align="center">
  <img width="auto" height="auto" src="Images/icons/sdgencc12.png">
</p>
> Soldisk NFTs' outside triangles appear and disappear according to the level of charge, in SOL 

> This document reflects changes that were made which aren't yet reflected in the rest of the Purple Explainer

# Get to know SOL

**SOL is the spark of the cXc.world economy.** Soldisks are 🟣 [PURPLE](https://wax.bloks.io/tokens/PURPLE-wax-purplepurple)-backed NFTs that allow the holder to claim [SOL](Sol.md) based on time passed since last claim (called a recharge). One Soldisk is backed by between 1-256 PURPLE, and has a daily claimable amount up to 288 SOL. 1 SOL is used for 1 Sol Up on cXc.world (learn about [Top Charts](Top-Charts.md)). Each Sol Up pays the artist 1 BLUX, and the listener 1 BLUX.


# How it Works

Soldisks are a [Simple Assets](https://wax.bloks.io/account/simpleassets) NFT that allows users to claim daily [SOL](Sol.md), used for Sol Ups. The amount claimable is based on the level of the Soldisk (See table below.)

## Empowering Listeners + Fans 🧝‍ 
Soldisks give listeners the power (via Sol Ups) to generate exposure for undiscovered music they enjoy, and also support artists financially without spending money. This changes the dynamics of fandom, allowing a dedicated grassroots group to catapult any song to the [Top Charts](Top-Charts.md) with a little patience and organization. Not only that, these fan groups (and individual fans) will help to financially support independent musicians on their journey.

# Soldisk Grant 🌞
Soldisks require the scarce 🟣 [PURPLE](https://wax.alcor.exchange/swap?output=PURPLE-purplepurple&input=WAX-eosio.token) token to activate. To make sure the best users of cXc can get a Soldisk for free, a grant of 10,000 Soldisks (budget of 100k PURPLE) will be distributed. Disk levels 1, 2, 3 + 4 will be awarded according to a four-point verification of engagement (metrics TBA). If a user completes all 4 of these, they can claim a level 4 Soldisk. 

# How to get a free Soldisk 🤲

You can fill out [this form *not live*]() to apply for early adoption.


## New Paradigm: SOL v3.0

We had planned to make SOL a token that only our `currentxchng` account could control. We did this to try to keep our tokemonics sane + beneficial to artists and listeners alike. Now, this isn't needed as we've figured out how to do it with a normal `eosio.token` contract. 

This new SOL model allows anyone to send Ups on cXc.world even before they buy/claim a Soldisk. By using SOL on the front-end, we put full control of votes in the hands of the voter (we don't approve each Up as it happens, but later in batch).

SOL v3.0 will give charts a wider democratic effect, as people can easily buy SOL to support artists they find on cXc.world. It also gives them more options to support. BLUX will likely be cheaper to purchase and promote a song, but the artist doesn't get paid more BLUX for these UPs (though they do have a shot at PURPLE rewards.)


> [👁️  See a Soldisk in the wild]()

# Soldisk Levels 🌅

Each ascending level (1-12) unlocks 24 more SOL, and requires some amount of additional PURPLE staked. The amount of PURPLE needed for additional SOL increases as levels increase. The first 4 levels offer the most economical option at 1 PURPLE each level, while the last 3 levels each require an additional 64 PURPLE per level.

| Level  | 🟣 PURPLE staked | Max Charge (in SOL) | Efficiency |
| :----:  | :-------------------: | :---------------: | :--: | 
| 1         | 1                   | 24           | 2400% |  
| 2         | 2                   | 48           | 2400% | 
| 3         | 3                   | 72           | 2400% | 
| 4         | 4                   | 96           | 2400% | 
| 5         | 8                   | 120           | 1500% | 
| 6         | 12                   | 144           | 1200% | 
| 7         | 16                   | 168           | 1050% | 
| 8         | 32                   | 192           | 600% | 
| 9         | 64                   | 216           | 337.5% | 
| 10        | 128                   | 240           | 187.5% | 
| 11        | 192                   | 264           | 137.5% | 
| 12        | 256                   | 288           | 112.5% | 

> The first 9 levels's stake requirement are the same as [Everstones](Everstones.md)

This ramping model allows small holders to achieve 1/3 of the SOL impact (96 daily SOL) for 1/64 the maximum staked tokens (4 PURPLE for 96 SOL per day), and those who wish to get their full voice to do so by contributing more to the economy (staking more PURPLE).

# Daily Claimable SOL
Soldisks can claim every time unit, or 5 minutes. Holders will always receive an amount corresponding to the time units passed, but no more than the Max Charge (See Soldisk Levels table above). This means a Level 1 can claim their max amount (24) every 2 hours (24 x 5 minutes = 2 hours), but waiting longer won't provide any benefit. 


<p align="center">
  <img width="auto" height="auto" src="Images/[TODO claim Soldisk image].png">
</p>


## Staking PURPLE to a Soldisk 
Staking additional PURPLE to an Soldisk is done via a `transfer` of PURPLE to [simplebacked](https://wax.bloks.io/account/simplebacked) with a memo of the Soldisk's Simple Assets NFT ID (ex 100000005145313). Eventually, we'll let you stake more PURPLE right from [cXc.world](https://music.cxc.world).

Only the current owner of the Soldisk can stake more PURPLE to it, so you don't need to worry about typing the wrong ID, as the `simplebacked` contract will return any PURPLE sent without a memo of an ID of a Soldisk currently held by your account. You DO need to be sure you send to `simplebacked` account.

> ⚠️ Double check before you don't stake more than 64 PURPLE to an Soldisk, as any more than 64 PURPLE won't add additional benefits, and will be locked on `simplebacked` until the Soldisk is burnt

## Verify your PURPLE has been Staked 🟣

Visit the [`simplebacked` contract's table](https://wax.bloks.io/account/simplebacked?loadContract=true&tab=Tables&account=simplebacked&scope=simplebacked&limit=100). Ensure scope says "simplebacked". Under BOTH the `Lower Bound:` and `Upper Bound:` fields, paste your Soldisk's asset id (eg. `100000017584903`)

<p align="center">
  <img width="auto" height="auto" src="Images/Verify-PURPLE-staked.png">
</p>


## Wait for Soldisk to Automagically Evolve
Your Soldisk NFT's metadata (and title) will update when you send the PURPLE to `simplebacked` and that payment will reflect your new level. 

## Unstaking PURPLE from Soldisk
Soldisk will automatically return all tokens staked when the NFT is burned. If a Soldisk is transferred and then burned, the owner at the time of burning will receive all tokens staked to the Soldisk. Partial unstake isn't possible. *You must go supernova.* 



# Tech + Contracts 🔌

Soldisk are Simple Assets NFT backed in Purple on a [simpleassets](https://wax.bloks.io/account/simpleassets) NFT using the [simplebacked](https://wax.bloks.io/account/simplebacked) contract to ensure all Soldisk return their PURPLE to the holder upon burning. ([example tx](https://wax.bloks.io/transaction/7a390ecf24f97e57482db730c2cfdc001d8bcda6a98d45fb7427d2afdcfdc052?tab=traces))  

## Mechanics of SOL and Sol Ups

> Contract pseudocode is now published

Soldisk store several pieces of data we use to ensure you get paid fairly. All Soldisk data is `mdata` or mutable data, so it can be updated by our `currentxchng` account.  

Each time a Soldisk is paid, the `mdata` is updated to reflect the payment in the `lifetime_sol`, `todays_sol`, and `last` field. The `last` field holds the timestamp of the last payment.
 
Here's all the mdata on a Soldisk.  

```javascript
{ // needs update / will change
  "name":"Soldisk",
  "img":"", // Changes based on level
  "level":"6",
  "staked_purple":"12",
  "daily_sol":"30",
  "lifetime_blux":"360",
  "last":"164476", // Time Unit of last recharge
  "todays_sol":"30"
}

// --- Image Metadata IPFS --- \\
diskImgs = [
  "QmVoTgrAPA7a9SAoY7cBt9rdixSG6n9qvr2j7igH2AB6V2", // 0
  "QmW6XzP38csCKRPAVSK8h9acnrcrDj8J6NrTvpr1eeEFtj", // 1
  "QmaJEXuzzVJTdpUsmgeensRn4sWJ2NWs8Q1YJSEkm4FbF4", // 2
  "QmYKWVKodp3b3492yFwGrkVUx3X4yRJMFeez17GXhPEKLT", // 3
  "QmeT2vdUumCqArBksy7JxQHTPA3TAYpDSxcjJCRH4dCEcP", // 4
  "QmeoxwrTQkNvgnHWJhLLiTrcWY92MoD7tFrZkoqZyDFBLJ", // 5
  "QmXo9WkyQWixPu3vZAmtcCRZfre2ugGD7eWF1FgVKTcw7V", // 6
  "QmXxtFMWgFDMtRM6ZqdqfqFws3JLS74eagUfybYwtts3Qf", // 7
  "QmcBYSYipCTC44As2pr9nANCnDkejJwrxeELtwChDuqszh", // 8
  "QmcFQmTVQfzVaZdJ2W5cc3GtjCS7jcojscsFJgV2r1kem9", // 9
  "QmT1Wpi5cP2L3V3boMi856Za6T5QuPKZ9zoGn6C6sApJzT", // 10
  "QmcYkD2EPveKLZpgHfgar78yQ1nHeNc7ZbHjVSVoWwLLqg", // 11
  "QmfSGT2mcC6BFx76b1USbVMx37v6XWioBYwavRNTHmxTqV"  // 12    
]
```

## Ownership Requirements
To prevent gaming of the 20% participation requirement and blacklist system, only one Soldisk can be registered per account. Registering a different Soldisk will unregister the one you have registered. 

> [See it on a Soldisk](https://wax.simplemarket.io/products/asset/100000016933308)
