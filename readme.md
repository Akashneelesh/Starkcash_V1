
# StarkCash💰 -  "Elevating Privacy, Empowering Transactions in the Decentralized Realm. This Project is made with ❤️ during Starknet Hacker House India 2023.

## Overview

StarkCash is a cutting-edge decentralized application (DApp) built on the StarkNet platform, designed to elevate the privacy and anonymity aspects of cryptocurrency transactions. The technical architecture comprises these crucial functions: Encryption function, Burnable address, Mint Function, Decryption function, and a relayer.

This project showcases an implementation of the EIP - 7503 (Wormhole). Which enables minting of secretly burnt ethers as a native privacy solution.

## Key Functions
1. Encryption Function: It takes in the withdrawer address and encrypts it, which is then passed on to the Deposit function
2. Deposit Function: It has two components: the amount and encrypted address. Whoch after succefully invoke woruld emit an event with the amount and the encrypted address
3. Burn Address : It is an address where we put the address as input and we calculate the hash of hash. The address should be a burnable address.
5. Orchestrator/ Relayer : This listens to the emitted event and then processes the data and decrypts thee encrypted address. Which is then relayed to mint the tokens to the decrypted address
   
## Smart Contract Implementation

The smart contract is coded in Cairo, leveraging the StarkNet platform. It incorporates a Storage struct managing critical storage components, events signaling deposit, errors, and external functions for contract initialization, depositing and upgrading the contract.

## Events

StarkCash emits events capturing pivotal activities:
- Deposited: Signifies a triumphant deposit, including the deposited amount.

- Initializable: Handles initialization events from the Initializable trait.

-Emited:
## Smart Contract Components

### Storage

The Storage struct meticulously manages:
- `initializable_storage`: Storage space dedicated to the Initializable trait.
- `denomination_message_hash`: LegacyMap preserving message hashes and their deposit status.
- `token_dispatcher`: An instance of the IERC20Dispatcher trait.

### Events

1. Deposited Event
   - Commemorates a prosperous deposit.
   - Contains detailed information about the deposited amount.


### Initializable Component

Handles the initialization process by incorporating events from the Initializable trait.

### External Functions

1. Initialize Function
   - Commences the contract with a specified token address for seamless integration.

2. Deposit Function
   - Facilitates depositing processes, implementing Pederson hashing and updating deposit status.
   - Triggers a Deposited event upon a successful deposit.
   - Retrieves and provides real-time information on the contract's token balance.


## Usage

StarkCash introduces a robust and private environment for executing cryptocurrency transactions on the StarkNet platform. Developers can leverage the provided functions to enable decentralized and confidential financial interactions, ensuring both security and privacy in a decentralized financial ecosystem.

## Run the project locally
1. Clone the repository
2. Do a quick `npm i`
3. Do `npm run dev`
### Voilaaaa! You are ready✨.


### References 
https://eips.ethereum.org/EIPS/eip-7503
