# Forge Template
> A catered template of https://github.com/FrankieIsLost/forge-template.

A template for quickly getting started with forge

---

## Getting Started

If you don't have forge installed:
1. `curl -L https://foundry.paradigm.xyz | bash`
2. `foundryup`
3. `brew install libusb`
4. then forge should be intalled

```
mkdir my-project
cd my-project
forge init --template https://github.com/DeGatchi/forge-contract
npm install ## install development dependencies
forge build
forge test
```

---

## Flattening
Terminal: `forge flatten ./src/[folder]/[contract].sol` <br/>
Pipe into contract: `forge flatten ./src/[folder]/[contract].sol > output.sol`

---

## Running Tests
When adjusting the contract being tested you may need to compile from scratch. Sometimes forge bugs out and doesn't recompile properly. 
```
forge clean && forge test -vvv
```
- `-v`, `-vv`, `-vvv`, `-vvvv` : each v increases the details returned from the test (I usually use `-vvv` & `-vvvv`)
- `forge test -vvv --match--contract <CONTRACT_NAME>` : tests a single contract (don't put `.t.sol` or `.sol` at the end).

---

## Commonly Used Functions
- `hevm.warp(uint256)` : sets block.timestamp to `uint256`
- `hevm.prank(address)` : sets msg.sender to `address` for 1 tx
- `hevm.startPrank(address)` : sets msg.sender to `address` until `hevm.stopPrank()`
- `hevm.stopPrank()` : stops msg.sender being `address`
 
---

## Features

### Testing Utilities

Includes common testing contracts like `Hevm.sol` and `Console.sol`, as well as a `Utilities.sol` contract with common testing methods like creating users with an initial balance.

### Preinstalled dependencies

`ds-test`, `solmate` + `openzeppelin` are already installed.

### Truffle 

Installed for the truffle flattener b/c Forge isn't compatible w/ chain deployments separate from Ethereum.

### Linting

Pre-configured `solhint` and `prettier-plugin-solidity`. Can be run by

```
npm run solhint
npm run prettier
```

### CI with Github Actions

Automatically run linting and tests on pull requests.

### Default Configuration

Including `.gitignore`, `.vscode`, `remappings.txt`

## License
This project is open-sourced software licensed under the GNU Affero GPL v3.0 license. See the [License file](LICENSE.md) for more information.
