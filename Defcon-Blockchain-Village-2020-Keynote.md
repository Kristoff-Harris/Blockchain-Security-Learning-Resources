
Link: https://www.youtube.com/watch?v=ZRnXDG15nKU

## Crypto Ecosystem Components

Users

Exchanges 
- Cold/hot storage

Assets
- Nodes
- Wallets
- Smart Contracts

## Exchange Security 
### Incidents 
BlockFi - lost customer PII, Employee SIM, ported to access internal portal 
- SIM Porting == rerouting cell traffic to bypass 2FA when mobile is used. A BlockFi admin was 
  hacked in this way

Coincheck - Lost PII for 200 customers & Domain Registrar hacked 

ALTSBIT - Lost 6.929 BTC, and 23.210 ETH: Lulzsec took credit 

CASHAA - lost 336 BTC because of a personal laptop that was hacked 

### Exchange Security Insights 
Are exchanges getting more secure?
- Decrease in number of incidents since 2019 (4 in 2020, vs 11 in 2019)
- Decrease in the monetary damage ($4M in 2020 vs $175M in 2019) 

Incident causes could have been avoided
- BlockFi SIM Swapping, Cashaa unmanaged personal laptop for work

Attackers are getting creative and going after more than just a hotwallet
- PII on Sunday, SIM Swap Monday 


# Blockchain Network Incidents

Bitcoin Gold
- Two 51% attacks with 29 block reorg (7167 BTG double spend)
- Attempted 51% with a massive 1300 block reorg. Notified by NiceHash miner. Issued secret node with a checkpoint
- In the second attack, NiceHash put out a software update that had the checkpoint 

Ethereum Classic (Aug 1, 2020)
- 51% attack resulting in a massive 3500 block reorg, attacker spent 200k on NiceHash to double spend an exchange.

## Network Security Insights
- PoW coins with easily rentable GPU hashpower will continue getting 51% attacked.
- Bitcoin Gold working with miners to secretly deploy a checkpoint is a new pattern

# Blockchain Network Incidents 

## Trends 
- Overall we're seeeing a shift to a proof of stake consensus algorithm 
- Proof Of Stake is where you lock up coins (staking) to give you voting power for on-chain actions. Performing these actions, or leaving 
  coins "locked up" provides a benefit such as being awarded currency in exchange for staking.
- Delegated Proof Of Stake (DPoS) - you delegate a set of validators, and then entrust them to vote & produce a set of blocks 

### SteemIt
- Tron and a number of exchanges colluded to get a controlling stake  in the SteemIt blockchain. First of a kind DPoS attack
- Once exchanges got a majority stake of delegated power, they were able to vote in a controlling set of validators. 
- With being able to set who the validators were, they effectively had full control over the protocol's consensus rules.
- Then they pushed an updated node software that unfroze funds that were from the initial pre-mine, which gave tron the controlling 
  asset in the system. They used this to be able to control the protocol indefinitely 
 
### Ethereum - Mempool attack
Need to learn about this!!!


# Node Vulnerabilities 

### Solana 
March 9 2020
- Solana testnet node failed to validate transaction signatures. 500M SOL were stolen

### Tendermit 
- DoS vulnerability when parsing invalid blocks 
- Resulted in a network halt

### FileCoin 
- Inflation bug discovered and exploited on testnet. 9B FIL minted.


# Wallet Vulnerabilities 

### Ripple - bug in how much you are vouching to send vs how much you send 
- Incorrect credidation 

### Monery Wallet
- Monero wallet was incorrectly parsing specially crafted coinbase transactions. 
- May result in invalid deposits displyed 

### Lightning Network 
- Vuln Disclosed which coul dlead to channel partner losing BTC

### Argent Wallet
- Wallet takeover vuln was patched after responsibility disclosed by OpenZeppelin
- Flaw was in the wallet's functionality which allowed for wallet recovery via Guardian nodes 
- When Guardian nodes were not well defined, anyone could take over those wallets

# Backdoors (In wallet and node software)

### Trinity Wallet 
- Wallet backdorred through a 3rd party dependency to steal funds (via key disclosure)

### RavenCoin 
- Inflation bug emergency patch. Bug was maliciously introduced. 300M RVN minted and sold
  on exchanges 

# Layer 2 Issues (Smart Contracts)
### bZx
- Margin trading bug exploited resulting in ~1M$ worth of ETH theft. 
- Flash loans were used to amplify the attack 

What's a flash loan?
- Basically a loan where you can borrow an asset and return it back to the initial point all within the same transaction 
- Fees are very low or non-existent for a flash loan (due to limited time of loan), and you can have a huge amout of assets 
  available to you 
- This breaks the assumption that if an attack is expensive enough to exploit, it's safe...  
- In the event that the transaction reverts, it's no big deal because the attacker can just return the funds

### Balancer

### Bncor



Delegation: 

## Addendum

What is Bit Coin Gold?
- BTG was a hard fork on the original cryptocurrency which took place in Oct 24, 2017
- BTG's stated purpose has been to "Make bitcoin decentralized again"
- Devs believe that by adopting a new Proof of Work based algo for the mining process, 
  BTG would not disproportionally favor mining operatations on specialized equiptment
- Crytpocurrency is listed on 40+ exchanges in 11 national currencies

What is a checkpoint?
- A checkpoint is when block hash values up to a specific point in time are hard-coded into the official bitcoin client.
- The client takes all transactions confirmed up to the checkpoint as irreversible







What is a Hard Fork?
- Link: [Blockchain Hard Fork](https://www.investopedia.com/terms/h/hard-fork.asp#:~:text=What%20Is%20a%20Hard%20Fork,version%20of%20the%20protocol%20software)
- A hard fork as it relates to blockchain technology is a radical change to a network's protocol that makes previously invalid blocks
and transactions invalid, or vice-versa. A hard fork requires all nodes or users to upgrade to the latest version of the protocol software

- 
