# Smart Contract with Solidity

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

## Remix IDE

Remix IDE is an open source tool that helps writing Solidity contracts straight from the browser. It has modules for testing, debugging and deploying of smart contracts.

### Compiling

After press `ctrl + s` to save, Remix will compile your code automatically. Then, You receive ABI (Application Binary Interface) and Byte code.

### Deploy & Run Transaction

Select environment, account, gas limit, contract and then click Deploy.

- Every time you deploy the contract, you need to pay gas price.
- When the button color is orange like deployment & transaction, it means that you need to pay gas price.
- When you would like to access public variable in contract, you do not need to pay gas price (click blue button).

## Reference

- [learning-smart-contract](https://github.com/kongruksiamza/learning-smart-contract)
