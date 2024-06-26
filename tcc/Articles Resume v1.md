ee- witnissed: testemunhado
- wary: receoso
- willing: disposto
- escrow: depósito de garantia

## Bitcoin: A peer-to-peer Electronic Cash System
### Resume:
- Peer-to-peer electronic cash
- digital signatures are part of solution
- its benefits are lost if a trusted third party is required
- resolves the double-spending problem
- Hash based
- Proof of Work
- Record cannot be changed without redoing the proof-of-work
- Longest chain serves as proof of squence
- Came from the largest pool of CPU power.
- Nodes can enter and leave the network anytime
### Introduction:
> Commerce on the Internet has come to rely almost exclusively on financial institutions serving as trusted third parties to process electronic payments.

- cost of mediation
- limits
- percentage of frauds accepted as unaviodable

> A certain percentage of fraud is accepted as unavoidable. These costs and payment uncertainties can be avoided in person by using physical currency, but no mechanism exists to make payments over a communications channel without a trusted party.

- a system based in cryptographic proof instead of trust
> What is needed is an electronic payment system based on cryptographic proof instead of trust, allowing any two willing parties to transact directly with each other without the need for a trusted third party.

> we propose a solution to the double-spending problem using a peer-to-peer distributed timestamp server to generate computational proof of the chronological order of transactions

> The system is secure as long as honest nodes collectively control more CPU power than any cooperating group of attacker nodes.

### Transactions
> We define an electronic coin as a chain of digital signatures.

Each owner transfers the coin to the next by digitally signing a hash of the previous transaction and the public key of the next owner
![[Screenshot 2024-04-27 at 14.03.53.png]]
The problem of double-spending: solution is to add a central company: 
> The problem with this solution is that the fate of the entire money system depends on the company running the mint, with every transaction having to go through them, just like a bank.

- All nodes must be aware of all transactions
- Just like the company is
- The  history and all transactions are publicly announced
### Timestamp Server
- All transactions have a timestamp
- The transaction is public and widely published

### Proof-of-work
> The proof-of-work involves scanning for a value that when hashed, such as with SHA-256, the hash begins with a number of zero bits
> The average work required is exponential in the number of zero bits required and can be verified by executing a single hash.

- To scam, you need to scam a block with proof-of-work and then all blocks later (practically impossible)
- It is one-CPU-one-vote

### Network
1.  New transactions are broadcast to all nodes.
2.  Each node collects new transactions into a block.
3.  Each node works on finding a difficult proof-of-work for its block.
4.  When a node finds a proof-of-work, it broadcasts the block to all nodes.
5.  Nodes accept the block only if all transactions in it are valid and not already spent.
6.  Nodes express their acceptance of the block by working on creating the next block in the chain, using the hash of the accepted block as the previous hash.
### The incentive


## Analysis on Blockchain Consensus Mechanism Based on Proof of Work and Proof of Stake
### Introduction
With the brief description of bitcoin principle in Nakamoto's study[1] on November 11, 2008, as well as the official launch of bitcoin system and the advent of Genesis block in 2009, the bitcoin system has been developing tepidly for nearly 10 years. After that, people find that through the underlying technology of blockchain, it can realize the same function in a completely decentralized environment, compared to the traditional centralized environment. The key to complete this function is the consensus algorithm.

The core of the consensus mechanism is to solve the problem of consistency in the distributed system through the consensus algorithm, so that each node can be recognized and cannot be tampered with. In the blockchain system, it mainly solves the consistency of transaction data and transaction status of each node in the distributed system, and realizes decentralized multi-party mutual trust

Consensus algorithm is the core technology of blockchain and the key technology to realize the Internet from information interconnection to value interconnection.

One is proof of work (POW), which is the probability of obtaining rights by consuming computing power. The greater the computing power is, the higher the probability can be. Its advantages are the strong randomness and great fairness, while its disadvantages are energy consumption and low consensus efficiency.

The second is the proof of stake (POS), which is the probability of obtaining rights by holding assets. The more assets are, the greater the probability can be. Its advantage is energy conservation and environmental protection, while the disadvantage is power concentration.

### Proof of work
- PROOF OF WORK: based on hashcash

##

## Proof-of-Search: Combining Blockchain Consensus Formation with Solving Optimization Problems

## Shaping the future of Ethereum: exploring energy consumption in Proof-of-Work and Proof-of- Stake consensus