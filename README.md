## Foundry

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

Foundry consists of:

-   **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
-   **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
-   **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
-   **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Documentation

https://book.getfoundry.sh/

## Usage

### Compile 
```shell
$ forge compile
```
To Deploy : 
forge create SimpleStorage --interactive

forge create SimpleStorage --rpc-url http://127.0.0.1:8545 --interactive

cast wallet import defaultKey --interactive 
cast wallet list 

Solidity Scripting : ( Deployment)
https://book.getfoundry.sh/tutorials/solidity-scripting


0xf39fd6e51aad88f6f4ce6ab8827279cfffb92266

### Deploy using Anvil 
// Deploys in Temporary Anvil Chain
forge script script/DeploySimpleStorage.s.sol

// DryRun Deployment to Anvil Blockchain 
forge script script/DeploySimpleStorage.s.sol --rpc-url http://127.0.0.1:8545

// Deploys to Anvil Blockchain 
forge script script/DeploySimpleStorage.s.sol --rpc-url http://127.0.0.1:8545 --broadcast --private-key <ANVIL_ACCOUNT_PRIVATE_KEY>

forge script script/DeploySimpleStorage.s.sol --rpc-url $SEPOLIA_RPC_URL --broadcast --private-key $PRIVATE_KEY

// Formats the code
forge fmt 

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Anvil

```shell
$ anvil
```

### Deploy

```shell
$ forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>
```

### Cast

```shell
$ cast <subcommand>
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```
