# Web3 Token Launchpad

A Solana-based decentralized application (dApp) for creating custom tokens on the Solana Devnet using the SPL Token-2022 program. Users can specify token details (name, symbol, metadata URI, and initial supply) and mint tokens via a web interface.

## Features
- Connects to Solana Devnet using `@solana/wallet-adapter-react`.
- Supports wallet integration with `UnsafeBurnerWalletAdapter`.
- Allows users to input:
  - Token name
  - Token symbol
  - Metadata URI (e.g., image URL)
  - Initial supply
- Creates a token mint, initializes metadata, sets up an associated token account, and mints the specified supply.
- Built with React and styled with CSS.


## Prerequisites
- Node.js (v16 or later)
- npm or yarn
- A Solana-compatible wallet (e.g., browser extension or burner wallet for testing)
- Access to Solana Devnet RPC (`https://api.devnet.solana.com`)

## Setup
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/garvmanc/web3-token-launchpad.git
   cd web3-token-launchpad

2. **Install the dependencies**:
   ```bash
   npm install
   npm install @solana/web3.js
   npm install @solana/spl-token
   npm i @solana/wallet-adapter-react
   npm i @solana/wallet-adapter-react-ui
   npm i @solana/spl-token-metadata

3. **Run the Application**
   ```bash
   npm start

## Usage
**Connect Wallet:**
- Click the "Connect Wallet" button (via WalletMultiButton) to connect a wallet (e.g., Unsafe Burner Wallet for Devnet testing).
- Ensure the wallet is funded with Devnet SOL (request airdrop at https://faucet.solana.com).

**Enter Token Details:**
- Name: Token name (e.g., "MyToken").
- Symbol: Token symbol (e.g., "MTK").
- Image URL: URI for token metadata (e.g., a JSON file hosted on IPFS or a public server).
- Initial Supply: Number of tokens to mint (e.g., 100 for 100 tokens with 9 decimals).

**Create Token:**
- Click "Create a token".
- If inputs are valid, the app:
  - Generates a mint keypair.
  - Creates a token mint with metadata.
  - Sets up an associated token account.
  - Mints the specified supply to the wallet.
- Check the browser console for the mint public key and transaction logs.
- Verify the token in Solana Explorer (Devnet) using the mint public key.

## Contributing:

- Fork the repository.
- Create a branch: git checkout -b feature-name.
- Commit changes: git commit -m "Add feature".
- Push to branch: git push origin feature-name.
- Open a pull request.