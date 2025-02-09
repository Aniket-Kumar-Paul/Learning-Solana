# SOLANA

## Basic Theory
### Transaction
- **Signatures** - Array of signature of private keys(users) made for the txn
- **Message** - Payload of info. that we send to the program

### Message
- **Header** - Info. about no. of signatures, accounts, & read-only accounts w/o signatures
- **Account Addresses** - Array of addresses of accounts that we are interacting with
- **Recent Blockhash** - Hash of the last observed blockchain ledger
- **Instructions** - Array of data used by smart contracts to complete the txn

### Instructions
- **Program ID** - The smart contract, txn will interact with
- **Accounts** - Array of accounts which contains state info. of the user
- **Data** - (Serialized) Byte array of data the program will use to handle each txn

### Accounts
- Accounts keep track of stae on a solana program
- Stored on the blockchain similar to a file on your hard drive
- **Signer** - Signature of the user giving authorization to execute the txn
- **Read-only** - Indicate if data in the account can be modified
- **Executable** - Account created at the deployment of the smart contract. Only executable accounts can process instructions. All additional user accounts must be owned by the executable account
- **Rent** - Lamport(SOL) that users pay to keep the account on the program. When it reaches 0, theaccount is removed. It's also possible to be rent-exempted.
- **Data** - Serialized metadata that allows user to store custom data in the account on the blockchain