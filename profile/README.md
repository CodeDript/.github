# CodeDript

## Overview

CodeDript is a blockchain-based agreement management platform that facilitates secure contracts between clients and developers. The system uses Ethereum smart contracts for escrow payments, IPFS for decentralized document storage with complete transaction transparency.

## What is CodeDript?

CodeDript enables clients and developers to create and manage project agreements through a trustless, decentralized system. The platform ensures payment security through blockchain-based escrow, provides immutable record-keeping, and automates payment release based on Project completion.

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

**Step 2: Developer Confirmation**

- Developer reviews the project requirements from the documents provided
- Developer assigns pricing and estimated time to complete
- Developer signs the proposal using MetaMask

**Step 3: Agreement Review**

- Client reviews the proposed pricing and deliverable dates
- Client can approve, reject, or request modifications
- Both parties negotiate until mutual agreement is reached

**Step 4: Contract Execution**

- Both parties sign the agreement using MetaMask
- Client's wallet is charged the total project amount
- Funds are locked in the smart contract escrow
- Project documents are uploaded to IPFS
- IPFS content identifier (CID) and agreement metadata are recorded on the Ethereum testnet

### Project Execution



**Progress Monitoring:**

- Both parties can view the project status in real-time
- All transactions are visible on the Sepolia test network
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

- Express REST API
- User authentication and authorization
- Database operations (MongoDB & Supabase)
- Blockchain transaction coordination
- IPFS file management via Pinata

**Smart Contracts (codedript-blockchain)**

- Solidity contracts deployed on Ethereum Sepolia (Ethereum Test Network) 
- Escrow payment management
- Automated fund release logic
- Event emission for transaction tracking

**Infrastructure (codedript-infra)**

- Docker containerization
- Nginx reverse proxy
- SSL/TLS configuration
- Service orchestration



## Technology Stack

**Client:**

- React 18 with TypeScript
- Vite build tool
- ethers.js for blockchain interaction
- React Query for state management
- MetaMask SDK
- ThirdWeb SDK

**Server:**

- Node.js with Express framework
- MongoDB (Backup metadata storing)
- Supabase (Image Uploads)
- JWT authentication
- ethers.js library
- Pinata API gateway for IPFS

**Blockchain:**

- Solidity smart contracts
- Hardhat development environment
- Ethereum test network (Sepolia testnet)
- IPFS for decentralized storage

**Infrastructure:**

- Docker and Docker Compose
- Nginx web server
- GitHub Actions for CI/CD
- EC2 instance (deployment)





CodeDript - Blockchain-based Agreement Management Platform
