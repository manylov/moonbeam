
# ![moonbeam](media/moonbeam-cover.jpg)

Run an Ethereum compatible blockchain based on Substrate.

*See [moonbeam.network](https://moonbeam.network) for the moonbeam blockchain description.*  
*See [www.substrate.io](https://www.substrate.io/) for substrate information.*

## Install (linux)

### Moonbeam

```bash
git clone https://github.com/PureStake/moonbeam
cd moonbeam
```

### Dependencies

Install Rust:  
```bash
curl https://sh.rustup.rs -sSf | sh
```

Initialize your Wasm Build environment (*required for compiling Rust to Wasm*):  
```bash
./scripts/init.sh
```

## Build

Build Wasm and native code:  
```bash
cargo build --release
```  
(Building for the first time will take a long time, to install and compile all the libraries)

## Run

### Single node dev

```bash
target/release/node-moonbeam --dev
```


## Pallets
* aura: Time-based Authority Consensus (*for simplicity until more development is done)
* balances: Account & Balance management
* grandpa: GRANDPA Authority consensus
* sudo: Allow specific account to call any dispatchable ("Alice": `0x57d213d0927ccc7596044c6ba013dd05522aacba`)
* timestamp: On-Chain time management
* transaction-payment: Transaction payement (fee) management
* evm: EVM Execution. (Temporary until we work on pallet-ethereum)

* mb-core: Currently serves as a way to experiments with pallets and substrate
* mb-session: WIP implementation of governance
* mb-evm: Pallet to support EVM. It provides extra dispatchables

## Contribute

### Code style

Moonbeam is following the [substrate code style](https://openethereum.github.io/wiki/Substrate-Style-Guide)  
We provide a [.editorconfig](.editorconfig) (*compatible with VSCode using RLS*)
