# Smart-contract-IoT

This repository serves for a hand-on introduction to smart contracts for IoT developers and engineers. 

The [wiki page](https://github.com/kachris/Smart-contract-IoT/wiki) contains Reference design material and guides on how to develop smart contract applications for IoT systems. 

Some useful introduction on smart contracts. 

A smart contract is a self-executing digital agreement, with the terms directly written into code. It automatically enforces and executes actions based on predefined conditions, without the need for intermediaries. Often used on blockchain networks like Ethereum, smart contracts ensure transparency, security, and efficiency in transactions.

FAQ and misconceptions. 

MultiChain has posted [here](https://www.multichain.com/blog/2016/04/beware-impossible-smart-contract/) a very useful guide on the basic misconceptions about smart contracts. 

The most frequent misconceptions regarding smart contracts in IoT systems:

**Misconception 1**: A smart contract reads some data from a sensor and based on the value it performs some action.

A smart contract cannot directly interact with external sensors or systems because it operates within a blockchain, which is a closed and deterministic environment. This is by design to maintain security, consensus, and reliability across the network. Blockchains can't inherently access external data (like sensor readings) because doing so would make the system vulnerable to manipulation and compromise its decentralized nature.

To address this limitation, "oracles" are used. Oracles act as intermediaries that securely bring external data into the blockchain, enabling smart contracts to respond to real-world events, like sensor data. However, without an oracle, a smart contract has no way to access or trust external information.

**Misconception 2**: A smart contract initates an event (i.e. control of an output pin) when the value of the Ethereum is above a specific threshold. 

A smart contract cannot directly initiate an event, like controlling an output pin, based on the value of Ethereum because it operates solely within the blockchain environment and cannot access external data or control external systems on its own. Specifically, the price of Ethereum (ETH) is an external, off-chain value that the blockchain itself doesn't know.

Like with sensor data, smart contracts are limited to information and actions within the blockchain. To interact with external data (such as ETH prices), you would need an external "oracle." An oracle fetches the price from an off-chain source and feeds it into the smart contract, which can then react. But without an oracle, the smart contract is isolated from external systems, including price data, and cannot trigger actions like controlling hardware or output pins directly.

So, while a smart contract can respond to external conditions with the help of oracles, it cannot do so by itself.
