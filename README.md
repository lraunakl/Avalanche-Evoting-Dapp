# e-Voting-dApp
a simple application, in which we will be holding an election between the candidates. Users will be able to vote for their chosen candidate. So, to vote easily and efficiently using the browser, we also need a client-side application to interact with the blockchain

## Prerequisites

- [Truffle-suite](https://trufflesuite.com/)
- [Datahub](https://datahub-beta.figment.io/signup)
- [Avalanche's architecture.](https://docs.avax.network/learn/platform-overview/)

## Requirements
- NodeJS v8.9.4 or later.
- Truffle, which you can install with npm install -g truffle
- Metamask extension added to the browser, which you can add from here
- Express.js, dotenv and @truffle/hdwallet-provider (instructions to install these are below)
- You will also need to have performed a cross-chain swap via the [Transfer AVAX Between X-Chain and C-Chain](https://docs.avax.network/build/tutorials/platform/transfer-avax-between-x-chain-and-c-chain/) tutorial to get funds to your C-Chain address on the Fuji testnet.

## Project-setup

```sh
npm init
```

install dependencies

```sh
npm install express dotenv @truffle/hdwallet-provider --save

```
Then create a boilerplate truffle project:
```sh
truffle init
```

This will setup our initial project structure. Smart contracts will be stored in the `contracts` folder, deployment functions for migrating smart contracts to the network will be stored in the `migrations` folder. And `build/contracts` folder would contain information about the deployed contract, ABI etc.

- First of all, we need to create an account on Avalanche network. Please visit Avalanche Wallet to create your account and save your mnemonics in the .env file.
- Now copy your Datahub's Avalanche Fuji testnet API key in the .env file as shown below.
- Never share or commit your .env file! It may contain sensitive information such as credentials and API keys. Therefore, it is advised to always add .env to your .gitignore file.

```sh
MNEMONIC="<avalanche-wallet-mnemonic>"
APIKEY=<your-api-key>
```

## Compile Contracts with Truffle

Any time you make a change to Election.sol you need to run truffle compile.
```sh
truffle compile
```
you should see the following output:

![truffle-compile](https://github.com/tawseefnabi/e-Voting-dApp/blob/main/assets/truffle-compile.JPG)
