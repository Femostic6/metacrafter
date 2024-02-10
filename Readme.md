# Vault Contract

This is a solidity smart contract for a vault that allows users to deposit and withdraw ERC20 tokens while maintaining a balance of shares that represent their ownership in the vault.

## Features

- Users can deposit ERC20 tokens into the vault and receive shares in return.
- Users can withdraw their ERC20 tokens from the vault by burning their shares.
- The contract keeps track of total supply and individual balances of shares for each user.

## Usage

1. Deploy the `Vault` contract, providing the address of the ERC20 token contract as an argument.
2. Users can deposit ERC20 tokens into the vault using the `deposit` function.
3. Users can withdraw ERC20 tokens from the vault using the `withdraw` function, specifying the number of shares they want to burn.

## Code Explanation

- The `Vault` contract implements the `IERC20` interface, ensuring compatibility with ERC20 tokens.
- It maintains a mapping of balances for each user and tracks the total supply of shares.
- The `deposit` function calculates the number of shares to mint based on the deposited amount and the current total supply.
- The `withdraw` function calculates the amount of ERC20 tokens to return based on the number of shares burned and the current total supply.
