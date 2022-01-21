# Forge Template
> A catered template of https://github.com/FrankieIsLost/forge-template.

A template for quickly getting started with forge

## Getting Started

```
mkdir my-project
cd my-project
forge init --template https://github.com/DeGatchi/forge-contract
npm install ## install development dependencies
forge build
forge test
```

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
