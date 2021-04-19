# Everstone NFTs
Everstones are 🟣 [PURPLE](https://wax.bloks.io/tokens/PURPLE-wax-purplepurple)-backed NFTs that send out 🔵 [BLUX](https://wax.bloks.io/tokens/BLUX-wax-bluxbluxblux) or Blu Ups daily. One Everstone is backed by between 1-64 PURPLE, and has a daily harvest between 1-432 BLUX or Blu Ups. When an Everstone is destroyed, the PURPLE is sent back to the Everstone's owner.


When you own an Everstone NFT, you get the choice to automatically Up chosen content every day or take a set reward in BLUX everyday. You may switch reward up to once per day. 

> Each Everstone level has Art and a description, revealed at a later date

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


## Everstone Rarity
Everstones are released at a slow but steady pace. How we decide to do this, we have not yet determined. Empty everstones are free, but PURPLE-backed Everstones are sold for face value at the current market sell price of PURPLE. 

## Empowering Creators 👨‍🎤🎤
Everstones are particularly useful for creators, as daily Ups on their content gives them exposure on the mapp and [Top Charts](Top-Charts.md).

## Empowering Fans 🧝‍
Fans may collect BLUX to Up their favorite artist's latest release. This can really help new artists, because local chart topping gives way to bigger charts, earning more BLUx from Sol Ups, new opportunities, and measurable exposure. 


# How it Works

Everstones are a [Simple Assets](https://wax.bloks.io/account/simpleassets) NFT that will be offered periodically from cXc already staked (backed) with PURPLE in limited amounts (Sale info TBA). Everstones can also be requested once per day by anyone (mined by cXc and send daily), though these free Everstones will contain 0 PURPLE and won't do anything useful until PURPLE is staked to them. 

Everstones store info on whether the owner wants BLUX or Blu Ups, and if Blu Ups is chosen, the owner can also specify which content to send the daily Blu Ups to. 

Once a day, we check how much PURPLE is staked on each Everstone, and if it's over 1, we distribute the owed Blu Ups or BLUX. There are no fractional Ups or BLUX, so rounding down to each level is used to calculate the rewards. For example, if you had 64 or 67 PURPLE staked to one Everstone, both would give 432 Blu Ups per day. We plan to provide a UI to help you avoid over-staking.

## Everstone Art
Each row in the "Everstone Harvest Levels + Rewards" table above has it's own art, description, and rarity that updates during the daily check (only if you stake more PURPLE). This art is TBA. 


# Staking

## Staking PURPLE to an Everstone
Staking an Everstone is done via a `transfer` of PURPLE or BLUX to [simplebacked](https://wax.bloks.io/account/simplebacked) with a memo of the Everstone's Simple Assets NFT ID (ex 100000005145313) 


## Unstaking from Everstones
Everstones will automatically return all tokens staked when burned. If an Everstone is transferred and then burned, the owner at the time of burning will receive all tokens backed on the Everstone.



# Tech + Contracts 🔌

> *Everstones emit Blu Ups* not considered in the Top 64 PURPLE rewards system, but displayed in the default Top Charts.

Everstones are Simple Assets NFT backed in Purple on a [simpleassets](https://wax.bloks.io/account/simpleassets) NFT using the [simplebacked](https://wax.bloks.io/account/simplebacked) contract to ensure all Everstones return their PURPLE to the rightful owner upon burning. ([example tx](https://wax.bloks.io/transaction/7a390ecf24f97e57482db730c2cfdc001d8bcda6a98d45fb7427d2afdcfdc052?tab=traces))



> Please note: We are still developing this feature and it probably will not be available on Beta's launch. Everstone's PURPLE-backing contract has been tested and is working as described above. Still, consider elements subject to change.
