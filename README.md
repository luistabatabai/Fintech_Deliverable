# Fintech_Deliverable
Solidity Code used in the execution of the Demo

# PaymentSystem

## Overview
`PaymentSystem` is a smart contract implemented in Solidity that facilitates payments between clients and merchants. It automatically deducts VAT and a fee, transferring the respective amounts to designated government and company wallets.

## Features
- Automated VAT (21%) and fee (1%) deductions
- Balance tracking for clients, merchants, government, and company wallets

## Installation
To use this contract, deploy it on a compatible Ethereum network. It has been tested on Remix, so its use is recommended.

## Usage
1. Deploy the `PaymentSystem` contract with the addresses of the government and company wallets.
2. Use the `makePayment` function to make payments to merchants. The function handles VAT and fee deductions automatically.

## Functions used:

### `constructor(address _governmentWallet, address _companyWallet)`
Initializes the contract with the specified government and company wallet addresses.

### `makePayment(address payable merchant) external payable`
Allows a client to make a payment to a merchant. The payment amount must be greater than zero.

## Events

### `PaymentMade(address indexed client, address indexed merchant, uint256 amount)`
Emitted when a payment is made.

### `Balances(address client, int256 clientBalance, address merchant, int256 merchantBalance, address governmentWallet, int256 governmentBalance, address companyWallet, int256 companyBalance)`
Emitted after a payment with the updated balances of all involved parties.




