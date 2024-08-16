# Voting Application

## Overview

The Voting Application is a decentralized system that utilizes blockchain technology to manage and conduct elections. It provides a transparent and secure way for users to register, vote, and view election results. The following document outlines the basic workflow of the application.

## Workflow

### 1. **Election Creation**

- **Admin Role:** 
  - The administrator initiates the election process by deploying the application on a blockchain network (Ethereum Virtual Machine, EVM).
  - The admin creates a new election instance and enters the election details, including the list of candidates available for voters to choose from.
  
### 2. **Voter Registration**

- **Voter Role:** 
  - Prospective voters connect to the same blockchain network and register to become eligible voters.
  - Upon successful registration, the voter's details are sent to the admin's dashboard for verification.

### 3. **Verification Process**

- **Admin Role:**
  - The administrator reviews the submitted registration details (blockchain account address, name, and phone number) to ensure accuracy and consistency with existing records.
  - If the details are verified and valid, the admin approves the registration, making the voter eligible to participate in the election.

### 4. **Casting Votes**

- **Voter Role:**
  - Once approved, the voter accesses the voting page to cast their vote for their preferred candidate.

### 5. **Election Closure and Results**

- **Admin Role:**
  - After the designated voting period concludes, the admin ends the election.
  - The system then closes the voting process and displays the results, with the winning candidate prominently announced at the top of the results page.

## Getting Started

### Requirements

- [Node.js](https://nodejs.org)
- [Truffle](https://www.trufflesuite.com/truffle)
- [Ganache](https://github.com/trufflesuite/ganache-cli) (Cli)
- [Metamask](https://metamask.io/) (Browser Extension)

#### Getting the requirements

1. Download and install **NodeJS**

   Download and install NodeJS from [here](https://nodejs.org/en/download/ "Go to official NodeJS download page.").

1. Install **truffle** and **ganache-cli** using node packager manager (npm)

   ```shell
   npm install -g truffle
   npm install -g ganache-cli
   ```

1. Install **metamask** browser extension

   Download and install metamask from [here](https://metamask.io/download "Go to official metamask download page.").

### Configuring the project for development

1. Clone this repository

   ```shell
   git clone https://github.com/sharma-rakshit/dVoting.git
   cd dVoting
   ```

2. Run local Ethereum blockchain

   ```shell
   ganache-cli
   ```

   > Note: Do not close `ganache-cli` (the blockchain network needs to be running all the time)

3. Configure metamask on the browser with the following details

   New RPC URL: `http://127.0.0.1:8545` *(use `port: 7545` for **ganache gui**, update it in the file:`truffle-config.js` as well)*

   Chain ID: `1337`

4. Import account(s) using private keys from ganache-cli to the metamask extension on the browser

5. Deploy smart contract to the (local) blockchain network (i.e ganache-cli)

   ```shell
   # on the dVoting directory
   truffle migrate
   ```

   > Note: Use `truffle migrate --reset` for re-deployments

6. Launch the development server (frontend)

   ```shell
   cd client
   npm install
   npm start
   ```

   > If you encounter **error** during `npm install`, please note that you might need to install Microsoft Visual C++ Redistributable packages from [learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170) (here is the direct download link for X64: [aka.ms/vs/17/release/vc_redist.x64.exe](https://aka.ms/vs/17/release/vc_redist.x64.exe))


Made with ❤️ by [Rakshit Sharmal](https://rxit.me).
