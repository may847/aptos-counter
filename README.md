Aptos Counter

A simple smart contract on the Aptos blockchain that implements a counter. This project demonstrates how to create and interact with a basic Move module on Aptos.

Features

Deploy a Move module on Aptos

Increment and decrement a counter

Query the current counter value

Prerequisites

Before you begin, ensure you have the following installed:

Aptos CLI

Move CLI

Node.js (for interacting via scripts)

An Aptos testnet account

Installation

Clone the repository:

git clone https://github.com/may847/aptos-counter.git
cd aptos-counter

Set up Aptos CLI:

aptos init

Compile the Move module:

aptos move compile --named-addresses counter=default

Deploying the Smart Contract

Publish the Move module to the Aptos testnet:

aptos move publish --named-addresses counter=your_account_address

Verify the module is deployed:

aptos account list --account your_account_address

Interacting with the Counter

Increment the Counter

aptos move run --function-id 'your_account_address::counter::increment' --args u64:1

Decrement the Counter

aptos move run --function-id 'your_account_address::counter::decrement' --args u64:1

Query the Counter Value

aptos move view --function-id 'your_account_address::counter::get_value'

Contributing

Contributions are welcome! Feel free to fork the repository and submit a pull request.

License

This project is licensed under the MIT License. See the LICENSE file for details.
