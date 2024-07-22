# NFT Vault Contract

## Overview

This is an updated version of the NFT Vault contract, now featuring a comprehensive staking mechanism. The contract allows users to stake their NFTs, implementing various features to enhance the staking experience and provide flexibility to users.

## Features

- **Minimum Staking Period**: Enforces a minimum duration for which NFTs must be staked.
- **Unstaking Duration**: Implements a cooldown period when unstaking NFTs.
- **Stake NFT**:
  - Transfers the NFT to the vault contract.
  - Prevents the staked NFT from being transferred or listed for sale.
- **Unstake NFT**: Initiates the unstaking process for a staked NFT.
- **Restake NFT**: Allows users to restake their NFT during the unstaking phase.
- **Hooks**: Provides hooks for calling other contracts upon completion of staking, unstaking, and withdrawal processes.

## Contract Structure

The contract is composed of several Rust files, each serving a specific purpose:

- `lib.rs`: The main entry point of the contract.
- `msg.rs`: Defines the messages for contract instantiation, execution, and querying.
- `state.rs`: Defines the state structures and storage.
- `execute.rs`: Implements the execution logic for various operations.
- `query.rs`: Implements the query logic.
- `error.rs`: Defines custom error types.
- `helpers.rs`: Contains helper functions.
- `hooks.rs`: Implements the hooking mechanism.

## Testing

The contract includes comprehensive tests in the `multitest.rs` file, ensuring the correct functionality of all features.

## Building

To build the contract, ensure you have Rust and Cargo installed, then run:

cargo build

## Generating Schema

To generate the JSON schema for the contract's messages and queries, run:

cargo run --bin schema

This will create schema files in the `schema` directory.

## Usage

To use this contract, you need to:

1. Deploy the contract to a compatible blockchain.
2. Interact with the contract using the defined messages in `msg.rs`.

For detailed information on each message and query, refer to the `msg.rs` file and the generated schema.

## Dependencies

This contract relies on several CosmWasm libraries and custom dependencies. For a full list, check the `Cargo.toml` file.

