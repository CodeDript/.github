# CodeDript

## Overview

CodeDript is a blockchain-based agreement management platform that facilitates secure contracts between clients and developers. The system uses Ethereum smart contracts for escrow payments, IPFS for decentralized document storage, and provides milestone-based project tracking with complete transaction transparency.

## What is CodeDript?

CodeDript enables clients and developers to create and manage project agreements through a trustless, decentralized system. The platform ensures payment security through blockchain-based escrow, provides immutable record-keeping, and automates payment release based on milestone completion.

## How It Works

### User Registration and Authentication

Users (both clients and developers) authenticate using MetaMask wallet integration. This eliminates the need for traditional passwords and provides secure, wallet-based identity verification.

### Gig Marketplace

Developers create service listings (gigs) that include:

- Service descriptions and deliverables
- Pricing information
- Required skills and expertise
- Estimated delivery time

Clients browse the marketplace, filter available gigs, and select developers based on their requirements.

### Agreement Creation Workflow

**Step 1: Initial Proposal**

- Client selects a gig and provides project details
- Client uploads project specification documents
- Agreement enters "Processing" state

**Step 2: Milestone Definition**

- Developer reviews the project requirements
- Developer creates milestones with specific deliverables
- Developer assigns pricing for each milestone
- Developer signs the proposal using MetaMask

**Step 3: Agreement Review**

- Client reviews the proposed milestones and pricing
- Client can approve, reject, or request modifications
- Both parties negotiate until mutual agreement is reached

**Step 4: Contract Execution**

- Both parties sign the agreement using MetaMask
- Client's wallet is charged the total project amount
- Funds are locked in the smart contract escrow
- Project documents are uploaded to IPFS
- IPFS content identifier (CID) and agreement metadata are recorded on the Ethereum blockchain

### Project Execution

**Milestone Workflow:**

1. Developer completes work for a milestone
2. Developer uploads deliverables to IPFS
3. Client reviews the submission
4. Client approves or requests revisions
5. Upon approval, milestone completion is recorded on blockchain
6. Partial payment is released from escrow to developer

**Progress Monitoring:**

- Both parties can view milestone status in real-time
- All transactions are visible on the Ethereum network
- Escrow balance is tracked transparently
- Complete transaction history is maintained

### Change Request Process

During project execution:

- Client can submit change requests for additional work
- Developer reviews and approves or rejects the request
- Approved changes include additional pricing
- Client funds the additional amount
- Extra funds are added to the smart contract escrow
- All change requests are recorded on the blockchain

### Project Completion

**Final Delivery:**

- Developer submits final deliverables
- Final deliverable is uploaded to IPFS
- Client performs final review and approval

**Payment Settlement:**

- Upon final approval, remaining escrowed funds are released to developer
- Project ownership is transferred to client
- Final transaction is recorded on Ethereum network
- Agreement status is updated to "Completed"

**Post-Completion:**

- Complete transaction history remains accessible
- All documents remain available via IPFS
- Blockchain provides immutable audit trail

## System Architecture

## System Architecture

The platform consists of four main components:

**Frontend Application (codedript-client)**

- React-based user interface with TypeScript
- MetaMask wallet integration
- Real-time project dashboard
- IPFS document viewer

**Backend API (codedript-server)**

- Node.js/Express REST API
- User authentication and authorization
- Database operations (Supabase/PostgreSQL)
- Blockchain transaction coordination
- IPFS file management via Pinata

**Smart Contracts (codedript-blockchain)**

- Solidity contracts deployed on Ethereum
- Escrow payment management
- Milestone tracking and verification
- Automated fund release logic
- Event emission for transaction tracking

**Infrastructure (codedript-infra)**

- Docker containerization
- Nginx reverse proxy
- SSL/TLS configuration
- Service orchestration

## Key Features

### Security and Trust

- Wallet-based authentication (no passwords required)
- Smart contract escrow (trustless payment handling)
- Blockchain immutability (tamper-proof transaction records)
- Decentralized storage (IPFS for documents)
- Cryptographic signing of agreements

### Payment Protection

- Funds locked in smart contract until work completion
- Milestone-based payment release
- Automatic payment distribution
- Complete transaction transparency
- Support for additional funding via change requests

### Project Management

- Structured milestone tracking
- Progress visualization
- Document management via IPFS
- Change request workflow
- Real-time status updates

### Transparency and Verification

- All transactions recorded on Ethereum blockchain
- Public transaction verification
- Permanent document storage
- Complete audit trail
- Etherscan integration for transaction viewing

## Technology Stack

**Frontend:**

- React 18 with TypeScript
- Vite build tool
- ethers.js for blockchain interaction
- React Query for state management
- MetaMask SDK

**Backend:**

- Node.js with Express framework
- Supabase (PostgreSQL database)
- JWT authentication
- ethers.js library
- Pinata API for IPFS

**Blockchain:**

- Solidity smart contracts
- Hardhat development environment
- Ethereum network (Sepolia testnet / Mainnet)
- IPFS for decentralized storage

**Infrastructure:**

- Docker and Docker Compose
- Nginx web server
- GitHub Actions for CI/CD

## Prerequisites

To run this platform, you need:

- Node.js version 18 or higher
- MetaMask browser extension
- Ethereum testnet funds (for testing)
- Supabase account
- Pinata account (for IPFS)

## Installation and Setup

### 1. Clone Repository

```bash
git clone <repository-url>
cd CodeDript
```

### 2. Deploy Smart Contracts

```bash
cd codedript-blockchain
npm install
npx hardhat compile
npx hardhat run scripts/deploy.js --network sepolia
```

### 3. Configure Backend Server

```bash
cd codedript-server
npm install
cp .env.example .env
# Edit .env with your configuration
npm run dev
```

### 4. Configure Frontend Application

```bash
cd codedript-client
npm install
cp .env.example .env
# Edit .env with your configuration
npm run dev
```

### 5. Access the Platform

- Frontend: http://localhost:5173
- Backend API: http://localhost:5000

## Project Structure

```
CodeDript/
├── codedript-client/          # Frontend React application
├── codedript-server/          # Backend API server
├── codedript-blockchain/      # Smart contracts
└── codedript-infra/           # Deployment configuration
```

## Documentation

Detailed documentation for each component:

- **Frontend Documentation:** [codedript-client/README.md](../codedript-client/README.md)
- **Backend Documentation:** [codedript-server/README.md](../codedript-server/README.md)
- **Smart Contracts:** [codedript-blockchain/README.md](../codedript-blockchain/README.md)
- **Infrastructure Setup:** [codedript-infra/README.md](../codedript-infra/README.md)
- **API Reference:** [codedript-server/docs/](../codedript-server/docs/)

## Security Considerations

This platform handles cryptocurrency transactions. Users should:

- Verify all transaction details before signing
- Keep private keys secure and never share them
- Test thoroughly on testnets before using mainnet
- Understand the risks associated with blockchain technology
- Review smart contract code before interacting with contracts

## Contributing

Contributions are welcome. Please follow these steps:

1. Fork the repository
2. Create a feature branch
3. Commit your changes with clear messages
4. Push to your branch
5. Submit a pull request for review


## Support

For questions, issues, or support requests, please open an issue in the repository or contact the development team.

---

CodeDript - Blockchain-based Agreement Management Platform
