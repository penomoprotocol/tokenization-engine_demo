# Tokenization Engine Smart Contracts (Demo)

This repository comprises a collection of smart contracts designed for tokenizing assets, with a specific focus on battery assets. The contracts are implemented in Solidity and intended for deployment on the Ethereum blockchain.

## Overview

The system is composed of several key contracts:

- **GlobalStateContract**: Manages global parameters such as fees and whitelisted investors / companies.
- **ServiceContract**: Serves as the primary entry point for users to interact with the system. 
- **TokenContractERC20**: Represents the tokenized asset and includes functionalities like purchasing tokens.
- **LiquidityContract**: Serves as a liquidity pool from which funds can be withdrawn by the asset owner.
- **RevenueDistributionContract**: Distributes revenue among token holders.
- **RevenueStreamContract**: Not part of penomo's domain. Represents a revenue stream into the tokenization engine. Simplified version of smart contract interface for rental revenue enabler.

## Local Deployment with Hardhat

### Prerequisites

- Node.js and npm installed.
- Hardhat and necessary dependencies installed.

### Steps

1. **Clone the Repository**:

    ```bash
    git clone [REPO_URL]
    cd [REPO_DIRECTORY]
    ```

2. **Install Dependencies**:

    ```bash
    npm install
    ```

3. **Compile the Contracts**:

    ```bash
    npx hardhat compile
    ```

4. **Deploy the Contracts Locally**:

    ```bash
    npx hardhat run scripts/deploy.js --network hardhat
    ```

5. **Interact with the Contracts**:

    After deployment, you can use Hardhat tasks or the Hardhat console to interact with your deployed contracts:

    ```bash
    npx hardhat console --network hardhat
    ```

6. **Testing (Optional)**:

    Run tests using:

    ```bash
    npx hardhat test
    ```

### Notes

- Hardhat will automatically create a local Ethereum environment for you, with several accounts pre-funded with Ether.
- Adjust gas prices and limits as necessary, depending on the Ethereum network's conditions.
