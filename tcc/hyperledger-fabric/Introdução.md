## Blockchain
- immutable transaction ledger
- distributed network
- peer nodes
- validation by a consensus protocol
- group in blocks
- hash

### Bitcoin and Ethereum:
- public
- permissionless
- anyone can join the network annonimously

### Enterprise use:
- KYC (know your customer)
- AML (anti money laundering)
- participants must be identified
- network must be permissioned
- high transaction throughput
- low latency
- hyperledger fabric!!

## What is hyperledger fabric
- Serves as the foundation for developing applications or solutions with a modular architecture
- Private blockchain
- Creates subnets (channels)
- Chaincode (smart contracts)
- Enterprise context
- Linux foundation
- Smart contracts in Java, Node or Go

> One of the most important of the platform’s differentiators is its support for **pluggable consensus protocols** that enable the platform to be more effectively customized to fit particular use cases and trust models. For instance, when deployed within a single enterprise, or operated by a trusted authority, fully byzantine fault tolerant consensus might be considered unnecessary and an excessive drag on performance and throughput. In situations such as that, a [crash fault-tolerant](https://en.wikipedia.org/wiki/Fault_tolerance) (CFT) consensus protocol might be more than adequate whereas, in a multi-party, decentralized use case, a more traditional [byzantine fault tolerant](https://en.wikipedia.org/wiki/Byzantine_fault_tolerance) (BFT) consensus protocol might be required.

### Modularity

> Design principle that divides the app into smaller, self contained units or modules.
> Each module has a specific functionality or responsibility


- Consensus
- Identity management protocols
- Crypto libraries
- Peer to peer gossip

### Smart contracts
- Chaincodes
- 1. Many smart contracts run concurrently
- 2. May be deployed dynamically
- 3. App code should be treated as unsafe and even malicious

1. Validates and orders transactions then propagates to all peer nodes
2. Each peer executes the transactions sequentially

### Fabric approach
- **execute, order, validate**
- execute a transaction and check its correctness
- order via pluggable consensus
- validate before commit to the ledger






https://www.youtube.com/watch?v=iTV89Tqfmgk
https://hyperledger-fabric.readthedocs.io/en/latest/whatis.html