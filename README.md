# Tokenization-Engine Smart Contracts (MVP)

This repository comprises a collection of smart contracts designed for tokenizing assets, with a specific focus on battery assets used for our Minimum Viable Product (MVP) v1. The contracts are implemented in Solidity and intended for deployment on peaq Network via EVM-bridge.

## Overview

The system is composed of several key contracts:

- **GlobalStateContract**: Manages global parameters such as fees and whitelisted investors / companies.
- **ServiceContract**: Serves as the primary entry point for users to interact with the system. 
- **TokenContractERC20**: Represents the tokenized asset and includes functionalities like purchasing tokens. Simplified version of actual ERC-1400 contract (will be published in the future).
- **LiquidityContract**: Serves as a liquidity pool from which funds can be withdrawn by the asset owner.
- **RevenueDistributionContract**: Distributes revenue among token holders.
- **RevenueStreamContract**: Interface between tokenization engine (penomo) and Revenue Enabler (third party) to receive revenue funds and billing record. Simplified draft for showcase purpose.

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
- This public repository does not showcase our commit history / actual ERC1400 contracts and is meant for public access and review only.
