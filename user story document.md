# Qualdano Platform User Story Document

## Overview
Qualdano is a decentralized platform that enables secure and verifiable storage of Qualtrics survey data hashes on the Cardano blockchain. The platform consists of three main components:
1. Qualtrics Custom Workflow Integration
2. Qualdano Web Application
3. Smart Contract on Cardano Blockchain

## User Stories by Component

### 1. Qualtrics Integration

#### Setting Up Automated Hashing
As a survey administrator:
- I can access the Qualtrics survey workflow settings
- I can enable the Qualdano workflow for my survey
- I can set a 24-hour interval for data hashing
- I receive confirmation when the workflow is successfully configured
- I understand that I need to manually download and store the raw data every 24 hours when hashing occurs

#### Workflow Operation
As a survey administrator:
- I can view the timestamp of the last successful hash
- I can modify or disable the workflow at any time

### 2. Qualdano Web Application

#### Landing Page
As a visitor:
- I can view information about the platform
- I can access platform documentation
- I can click the "Launch App" button to begin
- I understand the platform's purpose and value proposition

#### Authentication
As a user:
- I can choose between connecting a Cardano wallet or using username/password
- If choosing username/password:
  - I can create a random username
  - I can set my password
  - I understand that no personal information is collected
- I can log out at any time

#### Verification Page
As an authenticated user:
- I can upload raw data files for verification
- I can view the verification results immediately
- I can see a log of recent verification activities
- I receive clear feedback on verification success or failure

#### Transactions Page
As an authenticated user:
- I can view a complete table of hash transactions
- I can filter transactions by survey ID
- I can view transaction details including:
  - Timestamp
  - Survey ID
  - Transaction hash
  - Data hash

#### Upload Page
As an authenticated user:
- I can manually upload survey data for hashing
- I receive immediate feedback on the hashing process
- I understand that raw data is not stored on the platform

#### Account Management
As an authenticated user:
- I can add/remove survey IDs to track
- I can view all my tracked surveys in one place

### 3. Smart Contract Integration

#### Hash Storage
As a platform user:
- My data hashes are automatically stored on the Cardano blockchain
- I can view the blockchain transaction details
- I receive confirmation when hashes are successfully stored
- I can verify the integrity of stored hashes

## Data Flow Description

### Automated Hashing Process
1. The Qualtrics workflow triggers every 24 hours
2. Raw survey data is hashed using a standardized algorithm
3. Hash is sent to the Qualdano web app
4. Web app interacts with smart contract to store hash
5. Transaction is recorded and associated with user's account
6. User downloads raw data for local storage

### Verification Process
1. User accesses verification page
2. Uploads raw data file for verification
3. Platform generates hash using same algorithm
4. Hash is compared with blockchain record
5. Results are displayed to user
6. Verification attempt is logged

## Security and Privacy Considerations

### Data Handling
- No raw survey data is stored on the platform
- Only cryptographic hashes are stored on the blockchain
- Users are responsible for maintaining their raw data
- Authentication is pseudo-anonymous

### User Privacy
- No personal information is collected
- Usernames are randomly generated
- Survey IDs are the only stored identifiers
- Wallet connections are optional

## Platform Benefits

### For Survey Administrators
- Automated data integrity verification
- Blockchain-based immutable record keeping
- Flexible authentication options
- Easy tracking of multiple surveys

### For Organizations
- Enhanced data credibility
- Transparent verification process
- No additional data storage requirements
- Integration with existing Qualtrics workflows

## Technical Requirements

### User Interface
- Responsive web design
- Built with Next.js
- Intuitive navigation
- Clear error handling

### Authentication
- Cardano wallet integration
- Username/password option

### Blockchain Integration
- Cardano smart contract interaction
- Efficient hash storage
- Reliable verification process
