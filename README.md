# MyToken Contract

This repository contains the Solidity smart contract for `MyToken`.

## Overview

The `MyToken` contract is a simple ERC-20 like token implementation with minting and burning functionalities.

### Features

- **Public Variables**: The contract stores the token name, abbreviation, and total supply.
- **Mapping**: The contract maintains a mapping of addresses to their respective token balances.
- **Mint Function**: Allows an increase in total supply and updates the balance of a specified address.
- **Burn Function**: Allows a decrease in total supply and updates the balance of a specified address, with checks to ensure sufficient balance.

## Requirements

The contract fulfills the following requirements:

1. **Public Variables**: 
   - `tokenName`: The name of the token, initialized to "META".
   - `tokenAbbrv`: The abbreviation of the token, initialized to "MTA".
   - `totalSupply`: The total supply of the token, initially set to 0.

2. **Mapping**:
   - `balances`: A mapping of addresses to their respective token balances.

3. **Mint Function**:
   - Signature: `function mint(address _address, uint _value) public`
   - Description: Increases the total supply by `_value` and increases the balance of the specified `_address` by `_value`.

4. **Burn Function**:
   - Signature: `function burn(address _address, uint _value) public`
   - Description: Decreases the total supply by `_value` and decreases the balance of the specified `_address` by `_value`, only if the balance of the `_address` is greater than or equal to `_value`.

## Usage

To use this contract, deploy it on an Ethereum compatible blockchain and interact with the mint and burn functions to manage token supply.

### Minting Tokens
To mint new tokens, call the `mint` function with the address to receive the tokens and the desired value to mint.

### Burning Tokens
To burn existing tokens, call the `burn` function with the address from which to burn the tokens and the amount to burn.

## Deployment Script

This contract includes a development run script `deploy.js` for deploying the contract. Make sure to set up the necessary environment and run the deployment script to deploy the contract on the desired network.

## License

This project is licensed under the MIT License.
