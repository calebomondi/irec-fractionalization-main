# I-REC Certificate Fractionalization Prototype

This project demonstrates the fractionalization of International Renewable Energy Certificates (I-RECs) using blockchain technology. It allows users to view, fractionalize, purchase, and track ownership of I-REC certificates on the Ethereum blockchain.

## Project Overview

I-REC certificates represent 1 megawatt-hour (MWh) of renewable energy generation. This prototype enables fractionalization of these certificates into smaller, more affordable units, making renewable energy investment accessible to a wider range of participants.

### Key Features

- View whole I-REC certificates represented as NFTs (ERC-721 tokens)
- Fractionalize certificates into smaller tradable tokens (ERC-20)
- Purchase or trade fractional tokens
- Track ownership of fractional tokens
- Ensure the sum of fractions equals the whole certificate

## Repository Structure

This repository contains two main components as submodules:

- `smart-contracts/`: Solidity smart contracts for I-REC tokenization and fractionalization
- `frontend/`: React-based user interface for interacting with the smart contracts

## Smart Contracts

The smart contracts implement:

1. An ERC-721 token representing whole I-REC certificates
2. An ERC-20 token representing fractional ownership of certificates
3. A fractionalization mechanism to split certificates into tradable units
4. The purchase of the tokens from the contract's reserve or from holder listings

### Contract Addresses (Sepolia Testnet)

- I-REC NFT Contract: `0x8539DA660BFEd7c0F49728CDA6726BeB1ecf2cBA`
- I-REC Fractionalized Tokens Contract: `0x953894c851453758b3Ec420f75e96217241DC038`
- I-REC Marketplace: `0xad0C0F88C72D0BB41a2614dE9Dc6750CC43a4f8e`

## Setup Instructions

### Prerequisites

- Node.js (v16+)
- Git
- MetaMask or another Ethereum wallet
- Sepolia testnet ETH for testing

### Installation

1. Clone the repository with submodules:
   ```bash
   git clone --recurse-submodules https://github.com/calebomondi/irec-fractionalization.git
   cd irec-fractionalization
   ```

2. Install dependencies for both smart contracts and frontend:
   ```bash
   # Install smart contract dependencies
   cd irec-smartcontracts
   npm install
   cd ..

   # Install frontend dependencies
   cd frontend
   npm install
   cd ..
   ```

### Running the Smart Contracts Locally

1. Navigate to the smart contracts directory:
   ```bash
   cd irec-smartcontracts
   ```

2. Compile the contracts:
   ```bash
   npx hardhat compile
   ```

3. Run tests:
   ```bash
   npx hardhat test
   ```

### Running the Frontend

1. Navigate to the frontend directory:
   ```bash
   cd irec-frontend
   ```

2. Start the development server:
   ```bash
   npm run dev
   ```

3. Open your browser and navigate to `http://localhost:5173`

## Usage Guide

1. **Connect Wallet**: Click the "Connect Wallet" button and select your MetaMask wallet
2. **View Certificates**: Browse available I-REC certificates
3. **Purchase Fractions**: Browse available fractions and purchase them
4. **View Your Holdings**: Check your owned whole certificates and fractions

## Development Process and Challenges

The development of this prototype involved several key challenges:

1. **Smart Contract Design**: Creating a secure system for tokenizing renewable energy certificates while ensuring the relationship between whole certificates and their fractions remains intact
2. **Blockchain Integration**: Implementing secure and efficient interactions between the frontend and smart contracts
3. **User Experience**: Designing an intuitive interface for users who may not be familiar with blockchain technology
