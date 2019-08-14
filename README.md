# OpenZeppelin Starter Kit GSN

An OpenZeppelin Starter Kit GSN containing React, OpenZeppelin SDK, OpenZeppelin Contracts, Gas Station Network, Truffle and Infura.

OpenZeppelin GSN Starter Kit comes with everything you need to start using Gas Station Network contracts inside your applications. It also includes all the GSN Providers & Web3 connectors that you need to abstract gas for your users.

In addition to the contents included in the [vanilla Starter Kit](https://github.com/OpenZeppelin/starter-kit/blob/master/README.md), this kit contains a step-by-step tutorial on how to enable Gas Station Network for a simple Counter Contract.

## Requirements

Install OpenZeppelin SDK, Ganache, and Truffle

```
npm install -g truffle@5.0.2 ganache-cli@6.3.0 @openzeppelin/cli@2.5.0
```

## Installation

Ensure you are in a new and empty directory, and run the `unpack` command with `OpenZeppelin/starter-kit-gsn` to create a starter project:

```javascript
openzeppelin unpack OpenZeppelin/starter-kit-gsn
```

## Run

In a new terminal window, run your local blockchain:

```
ganache-cli --deterministic
```

In your original terminal window, at the top level of your folder, initialize the project
and follow the prompts:

```javascript
openzeppelin init
```

In a new terminal window, in the `client` directory, run the React app:

```javascript
cd client
npm run start
```

## Interact

You can interact directly with your smart contracts from the `openzeppelin` cli.

`openzeppelin transfer`

send funds to a given address.

`openzeppelin balance [address]`

query the ETH balance of the specified account, also supports ERC20s.

`openzeppelin send-tx`

sends a transaction to your contract and returns the events.

`openzeppelin call`

execute a constant method and receive back the value.

Type `openzeppelin` to see a complete list of available commands.

## Test

Truffle can run tests written in Solidity or JavaScript against your smart contracts. Note the command varies slightly if you're in or outside of the truffle development console.

```javascript
// inside the development console.
test

// outside the development console..
truffle test
```

Jest is included for testing React components. Compile your contracts before running Jest, or you may receive some file not found errors.

```javascript
// ensure you are inside the client directory when running this
npm run test
```

## Build

To build the application for production, use the build script. A production build will be in the `client/build` folder.

```javascript
// ensure you are inside the client directory when running this
npm run build
```

## FAQ

- **How do I use this with the Ganache-CLI?**

  It's as easy as modifying the config file! [Check out our documentation on adding network configurations](http://truffleframework.com/docs/advanced/configuration#networks).

- **Where is my production build?**

  The production build will be in the `client/build` folder after running `npm run build` in the `client` folder.

- **Where can I find more documentation?**

  Check out the [OpenZeppelin Starter Kits documentation](https://docs.openzeppelin.com/starter-kits/).
