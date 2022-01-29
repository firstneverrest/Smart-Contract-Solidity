# Smart Contract with Solidity

Smart Contract is a program that runs on the Ethereum blockchain. You can deploy smart contract to your cryptocurrency wallet like MetaMask.

## Tools

- Remix IDE

## Solidity

### Basic syntax

- similar to Java
- semi-colon is required
- use open and close curly bracket
- `/` (single-line comment) and `/* */` (multiple-line comment)
- pragma - a directive to tell language and compiler version

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0; // define language and compiler

contract MyContract{
    bool status = false;
    string name = "Chitsanupong";
    int amount = 1000;
    uint public balance = 5000;
}
```

### Data type

- boolean
- integer - uint & int
- string
- struct
- array
- mapping

### Access modifier

- public
- private

```
// define guide

// public
string public name;

// private
uint private _balance;

// define initial value
string public name = "Chitsanupong";

```

### Constructor

Define initial value in smart contract

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0; // define language and compiler

contract MyContract{
    string _name;
    uint _balance;

    constructor(string memory name, uint balance) {
        require(balance >= 1000, "balance must greater and equal to 1000");
        _name = name;
        _balance = balance;
    }
}
```

Before deployment, you need to provide initial value in constructor. `Require()` use to create constraint of initial value such as balance >= 1000.

## Function

- Pure - a function can access only constant and not access any value in storage
- View - a function can get value from storage but cannot edit
- Payable - a function can edit value in storage

```
// view
function getBalance() public view returns (uint balance) {
    return _balance;
}

// pure
function getBalance() public pure returns (uint balance) {
    return 1000;
}

// payable
function deposit(uint amount) public {
    _balance += amount;
}

```

## Remix IDE

Remix IDE is an open source tool that helps writing Solidity contracts straight from the browser. It has modules for testing, debugging and deploying of smart contracts.

### Compiling

After press `ctrl + s` to save, Remix will compile your code automatically. Then, You receive ABI (Application Binary Interface) and Byte code.

### Deploy & Run Transaction

Select environment, account, gas limit, contract and then click Deploy.

- Every time you deploy the contract, you need to pay gas price.
- When the button color is orange like deployment & transaction, it means that you need to pay gas price.
- When you would like to access public variable in contract, you do not need to pay gas price (click blue button).

## MetaMask

MetaMask is a crypto wallet and gateway to blockchain apps. After finishing writing smart contract and you would like to deploy to ethereum network, Metamask can help you do that. MetaMask can run on web browser and mobile app.

- Go to [official website](https://metamask.io/)
- Install with chrome extension
- Create a Wallet

### Networks

- Ethereum Mainnet - real network to make real transaction
- Test network - use for testing smart contract (you need to set show/hide test networks to show)

### Accounts

You can have more than one account

### Testnet Faucet

Find free money to use in test network

- [Chainlink](https://faucets.chain.link/)

## Deploy smart contract

- In Remix IDE, choose injected Web3 environment
- If the message pop up that cannot find injected Web3, reload page once
- choose an account
- compile and deploy
- open [Etherscan](https://etherscan.io/) and choose your testnet to watch your smart contract
- copy your smart contract address from Remix IDE
- verify and publish - copy solidity contract source code and paste to verify

## Reference

- [learning-smart-contract](https://github.com/kongruksiamza/learning-smart-contract)
