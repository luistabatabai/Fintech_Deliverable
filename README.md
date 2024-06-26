# Fintech_Deliverable
This is a brief explanation of the different functions and workings of the same Solidity Code that was used in the execution of the Demo, in the video attached in the deliverable

# PaymentSystem

## Working Overview
`PaymentSystem` is a smart contract implemented in Solidity that facilitates payments between clients and merchants. It automatically deducts VAT and a fee, transferring the respective amounts to designated government and company wallets.

## Features
- Automated VAT (21%) and fee (1%) deductions
- Balance tracking for clients, merchants, government, and company wallets

## Installation
If you want to test the working of this code, deploy it on a compatible Ethereum network. It has been tested on Remix, which is a testing platform within Ethereum, so its use is recommended.

## Usage
1. Deploy the `PaymentSystem` contract with the addresses of the government and company wallets.
2. Use the `makePayment` function to make payments to merchants. The function handles VAT and fee deductions automatically. You have to select the amount that you want to send. Currently you also have to input the merchant address (Copy it from the QR code), but this function will be automatized. 

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




