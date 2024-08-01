# IC-Paymaster
IC-Paymaster is a decentralized payment management system that integrates with ICP Chain Fusion to facilitate secure and efficient transactions. The platform supports ERC20 tokens, NFTs, and various paymaster functionalities to manage payments and approvals.

Table of Contents
Introduction
Features
Project Structure
Installation
Usage
Configuration
Contracts
Testing
Contributing
License
Introduction
IC-Paymaster provides a versatile payment management system that allows for smooth transactions using ERC20 tokens and NFTs. It includes various paymaster functionalities to handle payments and approvals efficiently.

Features
ERC20 Token Support: Manage and utilize ERC20 tokens within the platform.
NFT Integration: Handle NFT transactions and interactions.
Paymaster Functions: Includes various paymasters for approval and general payment functionalities.
Frontend Interface: User-friendly interface for managing transactions and interacting with paymasters.
Project Structure

ic-paymaster/
├── .devcontainer/
├── canisters/
│   └── chain_fusion/
├── src/
│   ├── Cargo.toml
│   └── chain_fusion.did
├── contracts/
│   ├── erc20/
│   │   └── MyERC20Token.sol
│   ├── nft/
│   │   └── MyNFT.sol
│   ├── paymasters/
│   │   ├── ApprovalPaymaster.sol
│   │   ├── GeneralPaymaster.sol
│   │   └── MyPaymaster.sol
│   └── token/
│       ├── ERC20.sol
│       └── Greeter.sol
├── deploy/
│   ├── erc20/
│   │   └── deploy.ts
│   ├── deploy-paymaster.ts
│   ├── deploy.ts
│   ├── interact.ts
│   └── use-paymaster.ts
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Button.js
│   │   │   ├── Check.js
│   │   │   ├── Dropdown.js
│   │   │   ├── Greeting.js
│   │   │   ├── Input.js
│   │   │   ├── InstructionsCard.js
│   │   │   ├── PaymasterMessage.js
│   │   │   ├── Spinner.js
│   │   │   ├── Title.js
│   │   │   └── TxDetails.js
│   │   ├── constants/
│   │   │   └── consts.js
│   │   ├── hooks/
│   │   │   ├── useAccountChanges.js
│   │   │   └── useWeb3.js
│   │   ├── pages/
│   │   │   ├── _app.js
│   │   │   ├── _document.js
│   │   │   └── index.js
│   │   ├── styles/
│   │   │   └── globals.css
│   │   ├── utils/
│   │   │   ├── formatAddress.js
│   │   │   ├── index.js
│   │   │   ├── paymasterUtils.js
│   │   │   ├── updateGreeting.js
│   │   │   └── updateNFTBalance.js
├── .eslintrc.json
├── .gitignore
├── README.md
├── jsconfig.json
├── next.config.js
├── package.json
├── postcss.config.js
├── tailwind.config.js
├── yarn.lock
├── lib/
│   └── packages/
│       └── test/
│           ├── erc20/
│           │   └── myerc20token.test.ts
│           ├── nft/
│           │   └── mynft.test.ts
│           ├── greeter.test.ts
│           └── utils/
│               └── Greeter.sol
├── .gitignore
├── Caddyfile
├── Cargo.lock
├── Cargo.toml
├── README.md
├── deploy.sh
├── dfx.json
└── foundry.toml
Installation
To get started with IC-Paymaster, follow these steps:

Clone the repository:

git clone https://github.com/arhansuba/ic-paymaster.git
cd ic-paymaster
Install dependencies for the frontend:
bash
Kodu kopyala
cd frontend
yarn install
Usage
Deploying the Contracts
To deploy the smart contracts, use the provided scripts in the deploy directory. For example:

npx hardhat run deploy/deploy-paymaster.ts
Running the Frontend
To run the frontend application:


cd frontend
yarn start
Configuration
Configuration files for various components are located in the deploy and frontend/src directories. Modify these files as needed for your deployment and application setup.

Contracts
The smart contracts are located in the contracts directory. Key contracts include:

MyERC20Token.sol: ERC20 token contract.
MyNFT.sol: NFT contract.
ApprovalPaymaster.sol: Paymaster contract for handling approval-based payments.
GeneralPaymaster.sol: General paymaster contract for managing payments.
Testing
To run tests for the contracts:


npx hardhat test
For frontend tests, navigate to the lib/packages/test directory and run:


yarn test
Contributing
We welcome contributions to IC-Paymaster! Please open an issue or submit a pull request on GitHub.

License
This project is licensed under the MIT License. See the LICENSE file for details.
