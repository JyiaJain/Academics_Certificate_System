# Blockchain Academic Certificate System

A decentralized application (dApp) for issuing, managing, and verifying academic certificates using Ethereum blockchain technology. This system provides tamper-proof credential verification while maintaining student privacy and institutional integrity.

![Project Banner](assets/comp_logo.png)

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [System Architecture](#system-architecture)
- [Technology Stack](#technology-stack)
- [Installation & Setup](#installation--setup)
- [Usage Guide](#usage-guide)
- [Smart Contracts](#smart-contracts)
- [Demo](#demo)
- [Future Work](#future-work)
- [Contributing](#contributing)
- [License](#license)

## Overview

This project implements a blockchain-based solution for academic institutions to issue verifiable digital certificates. By leveraging Ethereum's blockchain technology, we create a secure, transparent, and decentralized system for credential management that eliminates forgery and simplifies verification processes.

## Features

- **Secure Certificate Issuance**: Institutions can issue tamper-proof certificates anchored on the blockchain
- **Decentralized Verification**: Anyone can verify certificate authenticity without depending on the issuing institution
- **User Authentication**: Secure login system for institutions and certificate holders
- **Certificate Management**: Institutions can view, issue and manage all certificates
- **Instant Verification**: Third parties can instantly verify certificate authenticity

## System Architecture

The application consists of three main components:

1. **Smart Contracts**: Ethereum-based contracts written in Solidity that handle certificate issuance and verification
2. **Backend**: Python with Streamlit for web interface and business logic
3. **Database**: Firebase for storing certificate metadata and user credentials

![System Architecture Diagram](placeholder-for-architecture-diagram.png)

## Technology Stack

- **Blockchain**: Ethereum (Solidity)
- **Smart Contract Environment**: Truffle Framework
- **Frontend**: Streamlit
- **Backend**: Python
- **Database**: Firebase
- **Wallet Integration**: MetaMask
- **Deployment**: Ethereum Testnet

## Installation & Setup

### Prerequisites
- Python 3.10+
- Node.js 14+
- Truffle Suite
- MetaMask extension or other Ethereum wallet
- Git

### Installation Steps

1. Clone the repository:
```bash
git clone https://github.com/yourusername/blockchain-academic-certificate-system.git
cd blockchain-academic-certificate-system
```

2. Install dependencies for smart contract development:
```bash
npm install
```

3. Install Python dependencies:
```bash
cd application
pip install -r requirements.txt
```

4. Configure environment variables:
   - Create a `.env` file in the `application` directory based on the provided example
   - Add your Firebase configuration details
   - Add your Ethereum network details

5. Compile and migrate smart contracts:
```bash
truffle compile
truffle migrate --network development
```

6. Run the application:
```bash
cd application
streamlit run app.py
```

## Usage Guide

### For Institutions
1. Register as an institution using the registration page
2. Log in with your institutional credentials  
3. Navigate to the certificate issuance page
4. Complete the certificate details form and submit
5. The certificate will be issued on the blockchain and available for verification

### For Verifiers
1. Navigate to the verification page
2. Enter the certificate ID or upload the certificate
3. The system will verify the certificate against the blockchain records
4. View verification results and certificate details

## Smart Contracts

The system utilizes the following smart contracts:

### Certification.sol
The main contract that handles certificate issuance and verification. It includes functions for:
- Issuing new certificates
- Verifying certificate authenticity
- Retrieving certificate data

## Demo

### Institution Dashboard
![Institution Dashboard](placeholder-for-institution-dashboard.png)
*The institution dashboard for managing certificate issuance and tracking*

### Certificate Issuance
![Certificate Issuance](placeholder-for-certificate-issuance.png)
*The certificate issuance interface*

### Certificate Verification
![Certificate Verification](placeholder-for-verification.png)
*The verification interface showing a successfully verified certificate*

## Project Structure

```
├── application           # Streamlit web application
│   ├── app.py            # Main application entry point
│   ├── connection.py     # Web3 connection handling
│   ├── db                # Database integration
│   ├── pages             # Application pages
│   └── utils             # Utility functions
├── assets                # Images and static resources
├── build                 # Compiled smart contracts
├── contracts             # Solidity smart contracts
├── migrations            # Truffle migration scripts
└── truffle-config.js     # Truffle configuration
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
