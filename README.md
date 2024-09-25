# Trusted Blockchain-based Crowdfunding Platform

This project implements a **Trusted Crowd-Funding Platform** using **Blockchain** technology, **Smart Contracts**, and **Ethereum**. The goal is to provide a secure, transparent, and immutable system for crowdsourcing that resolves the common issues with traditional crowdfunding platforms. Contributors have greater control over their funds, and the process ensures accountability for all involved parties.

## Table of Contents
1. [Overview](#overview)
2. [Tech Stack](#tech-stack)
3. [Features](#features)
4. [System Workflow](#system-workflow)
5. [Installation](#installation)
6. [Usage](#usage)
7. [Smart Contracts](#smart-contracts)
8. [Contributing](#contributing)
9. [License](#license)

## Overview

Crowdfunding is an essential tool for startups and entrepreneurs to raise capital. However, most existing platforms lack transparency and give donors no control over their funds once donated. Our blockchain-based platform addresses these issues by offering a decentralized system that uses **Smart Contracts** to guarantee that funds are used as intended.

This platform uses **Blockchain** to secure all transactions and ensure transparency, with each donation recorded immutably on the blockchain. Donors can monitor and approve the spending of funds, and **Smart Contracts** automatically handle the distribution of funds once certain conditions are met.

## Tech Stack

The following technologies were used in the development of this project:

### **Frontend:**
- **HTML/CSS**: For building the web interface.
- **JavaScript (Web3.js & Ether.js)**: For interacting with the Ethereum blockchain.
- **Bootstrap**: For responsive web design.

### **Blockchain:**
- **Solidity**: For writing the smart contracts.
- **Ethereum**: The blockchain platform used.
- **Hardhat**: Development environment for Ethereum-based smart contracts.
- **Ganache**: Local Ethereum blockchain used for testing.
- **Metamask**: Wallet integration for users to connect their Ethereum accounts.

### **Backend:**
- **Node.js**: For backend server functionalities.
- **Express.js**: Backend framework.
- **Hardhat**: For compiling, deploying, and managing smart contracts.
  
### **Testing:**
- **Mocha & Chai**: For smart contract testing and validation.

## Features

1. **Secure Donations**: Funds are securely donated using Ethereum.
2. **Smart Contracts**: Automate the release of funds based on predefined conditions.
3. **Real-Time Monitoring**: Donors can monitor how their funds are being used.
4. **Metamask Integration**: Users can connect their Ethereum wallet for secure transactions.
5. **Campaign Management**: Campaign creators can manage funding, while contributors can approve expenses.
6. **Transparency**: All transactions are recorded immutably on the blockchain.

## System Workflow

1. **Admin/Project Manager Role:**
   - Create and manage crowdfunding campaigns.
   - Manage campaign details such as funding goals, project descriptions, and deadlines.
   - All projects are submitted for approval before they are published.
   - Approve or reject campaign expense requests.

2. **Donor/Investor Role:**
   - Register and connect their Ethereum wallet using **Metamask**.
   - Browse ongoing campaigns and choose to contribute.
   - Review and approve expense requests submitted by campaign managers.
   - Funds are transferred using **Smart Contracts** only after a majority of contributors approve.

### Transaction Flow:
1. Donors contribute to a project by sending Ether to a campaign.
2. Campaign managers request funds for specific expenses.
3. Contributors vote on these requests.
4. If the majority of contributors agree, the smart contract automatically transfers the funds.

## Installation

### Prerequisites:
- **Node.js** and **npm** (for package management)
- **Metamask** wallet extension
- **Hardhat** for Ethereum smart contract development
- **Ganache** for local blockchain simulation

### Steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-repo/crowdfunding-platform.git
   cd crowdfunding-platform
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Setup Ganache (Local Blockchain):**
   Install **Ganache** and run a local blockchain.

4. **Compile Smart Contracts:**
   ```bash
   npx hardhat compile
   ```

5. **Deploy Smart Contracts:**
   ```bash
   npx hardhat run scripts/deploy.js --network localhost
   ```

6. **Run the Application:**
   ```bash
   npm start
   ```

7. **Open Metamask** and connect it to your local Ganache blockchain.

## Usage

1. **Admin Panel**:
   - Log in with admin credentials.
   - View submitted campaigns and approve/reject them.
   - Monitor campaign progress and transactions.
  
2. **User/Investor Interface**:
   - Create an account and connect your wallet using **Metamask**.
   - Browse through active campaigns.
   - Contribute by sending Ether to the selected campaign.
   - Approve or reject expense requests.
   - Track your contributions and transactions.

## Smart Contracts

The core of this platform is built using **Solidity** smart contracts. Key contract functionalities include:
- **Campaign Creation**: Campaign managers can define funding goals, deadlines, and project details.
- **Contribution Handling**: Contributors send Ether to a campaign, and their contributions are tracked.
- **Expense Requests**: Campaign managers request funds, and contributors vote to approve or reject.
- **Fund Disbursement**: If a request is approved, funds are automatically transferred.

### Key Contracts:
1. **CampaignFactory.sol**: Allows users to create new campaigns.
2. **Campaign.sol**: Manages campaign-specific logic including contributions, expense requests, and fund management.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch.
3. Make the necessary changes.
4. Submit a pull request.

## License

This project is licensed under the MIT License.
