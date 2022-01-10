# Blockchain basics
In regular human-speak, a blockchain is just a public database. Blockchains store a history of transactions between parties on a forum that can be accessible by anybody.

- A blockchain is append-only. Once data has been written, it can't be changed.

- A blockchain takes the form of a linked-list instead of a table. That is, every set of transactions (known as a block) that is added to the blockchain must point to the previous block.

- Blockchains are decentralized - they're not owned by any particular organization, and can't be taken down in the same way as a regular database. That's because a single blockchain is copied among over hundreds of different users who each run nodes, each containing an identical copy of the entire history of the blockchain. 

## Cryptology, Hash and SHA256
A Blockchain is a chain of blocks that contain information. The data which is stored inside a block depends on the type of blockchain.

A Bitcoin block contains information about Sender, Receiver, number of Bitcoins to be transferred.

How Does a Blockchain Block Look Like?

Every block has:
- Data.
- Individual Hash.
- Hash of the previous block (parent hash).

The first block (Genesis Block) is the only one without a parent hash.

Every block in the blockchain has a unique SHA256 HASH that identifies its content, shared with the subsequent block.

If you change the hash, this will not correspond anymore to his children's parent hash, invalidating the block.

## PoW and PoS
Blockchains are decentralized. There is never a central entity that can decide what is true and what is not. Instead, in a blockchain network, a variety of nodes interact with each other.

As a blockchain usually stores data in a chain of blocks (hence the name), the network must decide what the actual truth is together, This is where consensus algorithms come in. Everyone can append a block. If two participants do it at the same time, the chain is forked.

Distributed consensus helps the network to decide which fork of the chain is actually the truth while ignoring or throwing away the wrong fork. It especially helps them to decide if a block that has been appended to the chain was so, rightfully.

<b>Proof of Work (PoW)</b>

This is the algorithm currently used by Bitcoin, Ethereum 1.x, and a few other blockchains.

Miners, the ones that append blocks to the chain, usually have to solve a moderately difficult to very difficult challenge to gain the right to append a block.

In case of Bitcoin, the network chooses a target hash that the miners must create. The miners take the hash of the previous block, the transactions that are to be included in the next block, and a so-called nonce, and then create a hash from all that data.

The nonce is simply an integer. It is the only thing that can be changed by the miners. The miners have to guess the right nonce so that it, together with the hash of the previous block and the new transactions, creates the target hash initially requested.

All other participants can easily check if the hash presented to them is indeed the correct one by simply hashing all the necessary data. If they get the hash they see, everything is alright. If not, they can throw away the block.

In case of Bitcoin, the difficulty of finding the right nonce can be adjusted by asking for a certain number of leading zeroes in the target hash. The more zeroes asked for, the more difficult the task becomes.

PoW is very energy-intensive.

<b>Proof-Of-Stake (PoS)</b>

This algorithm is the most common alternative to the energy-intensive PoW.

In PoS-based networks, miners are called validators. They lock away a certain amount of the network's coins and are randomly chosen by the network to validate the next block.

The choice is based on the amount of coins staked and other factors, like the stake's age. When a validator appends a new block, the stake's age is reset to zero to ensure that everyone gets their turn at some point.

Each individual blockchain implementation can decide which factors to take into account when choosing validators.

The algorithm is not energy-intensive at all but requires an investment upfront that sometimes isn't trivial.

If a validator tries to harm the network by appending fake blocks to the chain, it loses its stake on detection of the fraud. The investment upfront thus is to ensure that validators play by the rules.

# Ethereum
Ethereum is a global, decentralized platform for money and new kinds of applications. On Ethereum, you can write code that controls the money, and build applications accessible anywhere in the world.

## Ethereum vs Bitcoin
Like Bitcoin, ethereum is a distributed public blockchain network. Although there are some significant technical differences between the two, the most important distinction to note is that Bitcoin and Ethereum differ substantially in purpose and capability. Bitcoin offers one particular application of blockchain technology, a peer to peer electronic cash system that enables online Bitcoin payments. While Bitcoin is used to track ownership of digital currency (bitcoins),  ethereum focuses on running the programming code of any decentralized application.

In the Ethereum, instead of mining for bitcoin, miners work to earn Ether, a type of crypto token that fuels the network. Beyond a tradeable cryptocurrency, Ether is also used by application developers to pay for transaction fees and services on the ethereum network. 

## Smart Contracts
A smart contract is a self-contained program that defines a public agreement, or "contract" that automatically executes the terms of the agreement when called by a user on the blockchain.

Smart contracts are simply computer programs that run on a blockchain network. The concept was first coined by computer scientist and cryptographer Nick Szabo in the late 1990s. However, they were first implemented by the Ethereum protocol. The scripting language designed for Bitcoin is intentionally designed to be Turing incomplete and constrained to simple true/false evaluation of spending conditions, while <b>Solidity</b>, the premier programming language built for the Ethereum Virtual Machine (EVM), was meant to facilitate the use of Ethereum as a globally distributed computer, not just a protocol for digital currency. Several new blockchain protocols have since emerged. Most have smart contracts that are written in <b>Solidity</b>. Others are written in more contemporary languages like Rust (NEAR, Solana), Python (Algorand) and even Go and C/C++(EOS).


## Resources
- https://twitter.com/oliverjumpertz/status/1391769503869059084
- https://twitter.com/VittoStack/status/1439980837899055108
- https://betterprogramming.pub/how-to-become-a-blockchain-engineer-fa4386a0504f
- https://medium.com/immunefi/hacking-the-blockchain-an-ultimate-guide-4f34b33c6e8b
- https://www.web3.university/getting-started