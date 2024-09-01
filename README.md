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



### Foundry zkSync

Detected your preferred shell is zsh and added foundryup-zksync to PATH.
Run 'source /Users/siva/.zshenv' or start a new terminal session to use foundryup-zksync.
Then, simply run 'foundryup-zksync' to install foundry-zksync.
Sourcing the shell configuration file: '/Users/siva/.zshenv'
Running foundryup-zksync setup...


```
// Installs vanilla foundry
foundryup 

// To go to foundry-zkysnc 
foundryup-zksync

forge build --zksync
```


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

# To convert Dex to Decima
$ cast to-base 0x67613 dec
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```


### Gas Calculation / Estimation

- Get the Gas Used from broadcast/run/xxx.json
    - cast to-base 0x67613 dec
    - 423443
- Get the latest ETH fees(Gwei) from Etherscan
    - Ex: https://etherscan.io/tx/0x62e286951975d0dd8dda4650d03fb386a906f95659455a90fe6e94bb0c5dcd8a
    - Gas Price : 0.606 Gwei
- Gas Cost to deploy : Gas Used * Gas Price 
    - 423443 * 0.606 
    - 256606.458 Gwei
- Go to https://eth-converter.com/
    - Use Gas cost to get the price in Ether and USD 
    - $0.63
- https://l2fees.info/
    - To compare the fees in l2 networks 


### References : 
- https://github.com/Cyfrin/foundry-simple-storage-cu
- https://updraft.cyfrin.io/courses/foundry/foundry-simple-storage/why-l2
