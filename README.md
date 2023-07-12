# ETH-AVAX-PROOF-Intermediate-EVM-Course-3
## MyToken
In this we will write a smart contract to create your own token on a local HardHat network. Once we have your contract, you should be able to use remix to interact with it. From remix, the contract owner should be able to mint tokens to a provided address. Any user should be able to burn and transfer tokens.

## Licensce
SPDX-License-Identifier: MIT  contract using MIT licensce.
## version
solidity ^0.8.0

## contract "MyToken" details
 * The MyToken contract is defined. It represents your custom token.
 * The name, symbol, decimals, and totalSupply variables are declared. These store information about the token, such as its name, symbol, decimal places, and total supply.
 * The  balanceOf  mapping is defined. It maps an address to the token balance of that address.
 * The Transfer and Burn events are declared. These events will be emitted when token transfers and burns occur.
 * The constructor function is defined. It initializes the token's properties when the contract is deployed.
 * The function takes _name, _symbol, _decimals, and _initialSupply as input parameters.
 * The values passed as arguments are assigned to the respective variables (name, symbol, decimals, totalSupply).
 * The token's total supply is calculated by multiplying _initialSupply with 10 raised to the power of _decimals.
 * The balanceOf mapping is updated to assign the total supply to the contract deployer's address (msg.sender).

## functions
 * `The transfer function` allows users to transfer tokens from their own address (msg.sender) to another address (_to).
   The function takes _to (the recipient's address) and _value (the amount of tokens to transfer) as input parameters.
   The token balances are updated accordingly: the sender's balance is decreased by _value, and the recipient's balance is increased by _value.
   The Transfer event is emitted to notify listeners about the token transfer.

 * `The burn function` allows users to burn (destroy) their own tokens.
   The function takes _value (the amount of tokens to burn) as an input parameter.
   The sender's balance is decreased by _value.
   The total token supply is decreased by _value.
   The Burn event is emitted to notify listeners about the burned tokens.

 * `The mint function` allows the contract owner to mint (create) new tokens and assign them to a specific address (_to).
   The function takes _to (the recipient's address) and _value (the amount of tokens to mint) as input parameters.
   The recipient's balance is increased by _value.
   The total token supply is increased by _value.
   The Transfer event is emitted with address(0) as the from parameter, indicating that the tokens are minted into existence.

## needs
make sure u created a locally hardhat network

## usage
Make sure you have Solidity ^0.8.0 installed. Compile and deploy the MyToken contract to a supported local hardhat network. Interact with the deployed contract by calling the available functions and providing the required parameters.

