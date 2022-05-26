
# Security 

### What is the Mempool?
https://medium.com/dragonfly-research/we-live-in-a-mempool-backrunning-the-mev-crisis-a4ea0b493b05

### What are Mempool attacks?
https://cs.ucf.edu/~mohaisen/doc/icbc19a.pdf

### What is a Reentrant Microtrading Attack?
https://github.com/openzeppelin/exploit-uniswap

### What is Function Clashing?
https://github.com/tinchoabbate/function-clashing-poc

### How can wallets be back-doored?
https://blog.openzeppelin.com/backdooring-gnosis-safe-multisig-wallets/

### What is a sybil attack?
https://academy.binance.com/en/articles/sybil-attacks-explained

### What is a dusting attack? 
https://academy.binance.com/en/articles/what-is-a-dusting-attack

### Eclipse attack -  
https://academy.binance.com/en/articles/what-is-an-eclipse-attack

An eclipse attack is an attack where interaction with a previously trusted resource
becomes controlled by an attacker (ie. BGP reroute, block manip, etc...)

### What is Byzantine Fault Tolerance? 
https://academy.binance.com/en/articles/byzantine-fault-tolerance-explained

### What are common scams on Mobile Devices?
https://academy.binance.com/en/articles/common-scams-on-mobile-devices

### What is a Threshold Signature? 
https://academy.binance.com/en/articles/threshold-signatures-explained

### What is segregated witness? 
https://academy.binance.com/en/articles/a-beginners-guide-to-segretated-witness-segwit

### What is a multi-sig wallet? 
https://academy.binance.com/en/articles/what-is-a-multisig-wallet

### zk-snarks and zk-starks 
https://academy.binance.com/en/articles/zk-snarks-and-zk-starks-explained

### What is Selfish Mining?  
https://academy.binance.com/en/articles/selfish-mining-explained



### Schnorr Signatures - 
https://academy.binance.com/en/articles/what-do-schnorr-signatures-mean-for-bitcoin

### Blockchain Scalability - Sidechains & Payment Channels 
https://academy.binance.com/en/articles/blockchain-scalability-sidechains-and-payment-channels

# Coin Tech 

### What is  Tether (USDT) - https://academy.binance.com/en/articles/what-is-tether-usdt

### What is Coin Burn? https://academy.binance.com/en/articles/what-is-a-coin-burn

### What is a layer 2? https://academy.binance.com/en/glossary/layer-2

### What is the lightning network? - https://academy.binance.com/en/articles/what-is-lightning-network

### What is a Merkle Tree?
- [Merkle Trees and Roots Explained](https://academy.binance.com/en/articles/what-do-schnorr-signatures-mean-for-bitcoin)
- Merkle tree is created by dividing data into many pieces, which are hashed repeatedly to form the merkle root.
- This allowas us to efficiently verify if something has gone wrong with a piece of data. 

### How does this relate to crypto?
- When you start mining, you line up all the transactions you want ot include and construct a merkle tree. 
- You put the resulting root hash (32 bytes) in the block header. This makes it so you only need to hash the block header
  rather than the entire block 
- This works because it's tamper-proof. You effectiveyl summarize all of the block's transactions in a compact format

### Verification 
- Nodes running on devices with limited resources don't want to download and hash all of a block's transactions
- What they do is simply request a "Merkle proof" - evidence  provided by the full node that proves that your transaction is 
  in a particular block. 
- This is referred to as SPV (Simplified Payment Verification)
What is a light client?
- A light client is a node that doesn't hold a full copy of the block-chain
