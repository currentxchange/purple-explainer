<p align="center">
  <img width="240" height="240" src="https://ipfs.pink.gg/ipfs/QmXSevesv6tanu4AuybSR3f1xHetozHYqjz1QEGbT2ghX5">
</p>


# Sol
[SOL](https://wax.simplemarket.io/trading/ft/currentxchng/SOL) is a fungible token using the [Simple Assets](https://github.com/CryptoLions/SimpleAssets) standard on the WAX blockchain.

SOL is a [time token](https://github.com/dougbutner/web-4#time-issued-cryptocurrency-time-tokens), freely given to each member of cXc.world. A SOL must be burnt to make an Up on the site. Each SOL is linked to one Time Unit.

SOL is **Non-transferable**, and **controlled** by the [currentxchng](https://wax.bloks.io/account/simpleassets) account according to the [simpleassets](https://wax.bloks.io/account/simpleassets) contract. This allows SOL to work more like an in-game currency than a real token, helping mapps prevent manipulation and Up farming with fake account.

> To learn more about the economics of cXc.world mapps, see the [Purple Paper](https://docs.google.com/document/d/1T2JH9J73WjgZ9-cULJAzrYvZzyPSXEA_fdgt21lHnDc/preview) and the [Mapps](https://docs.google.com/document/d/1YppJ2EYumRI2j0UHYdZh7NJMObMI_NfHgaFRLbjgBtw/preview) paper.

# Functionality
SOL is **burned (destroyed) for Sol Ups** 1:1.

64 can be burned at a time for a **Big Up**, which is recorded as 64 Ups (1:1), but also 1 "Big Up" tracked alongside Ups.

Sol Ups **determine most of the distribution of BLU** and also the **distribution of PURPLE** through the Top Charts.

Here you'll see the Up button (center) Big Up (left) and Blu Up (right)
<p align="center"><a href="https://music.cxc.world" target="_blank" alt="Experience cXc Music">
  <img width="auto" height="auto" src="https://github.com/currentxchange/purple-explainer/blob/master/Images/I-SE-USA.png"></a>
</p>


# Supply of SOL
SOL has a maximum supply of 2^62-1, the highest possible on EOSIO. **Circulating supply fluctuates**, as it is constantly being inflated over time, and deflated through Sol Ups.

**SOL is indivisible** (0 precision) token, matching it's functionality of being worth exactly 1 Up.

# Smart Contract
SOL is a [simpleassets](https://wax.bloks.io/account/simpleassets) token and exists on their contract. You can view SOL on Simple Assets [here](https://wax.simplemarket.io/trading/ft/currentxchng/SOL).


# SOL Distribution
Each account must first receive a **Solar Disk** (Simple Assets NFT) in order to receive SOL from the SOL faucet. Sol is held on Solar Disk via the `attachf` action.

One Solar Disk cannot hold more than **288 Sol** at one time, and Sol held outside of a Solar Disk is burned by cXc to prevent hoarding.

The amount of Sol a user has will **change the image on the Solar Disk NFT**, giving the user a visual representation of the SOL they have remaining anytime they look at their NFT wallet. This images matches the one shown on the UI on cXc.world beta.


When a user requests a faucet (called a recharge), we first check that they have a **Solar Disk**, and then see how much Sol is attached to that solar disk. If a user has less than 288 Sol, they will be given **up to 144 SOL**. A user can **recharge once every 12 hours.**

> Solar disks may be limited to invite-only if demand grows rapidly

# Advanced Functionality Description

**Sol movements are tracked by time unit, recipients and deltas.**

When a user requests a recharge, the time of the recharge (Time Unit number) is stored in the transfer memo. Also stored is a **delta value** that tells the change in time units representing how much Sol is transferred. Using the delta value, **amount**, and **Time Unit** info, we can calculate exactly which Time Unit's Sol is being burnt to Up a particular piece of content, and also ensure that a user cannot somehow recharge more than they should, as the delta would run into the last recharge, failing the transfer.
