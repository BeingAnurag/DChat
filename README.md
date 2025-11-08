# DChat — Web3 Encrypted Chat DApp

DChat is a decentralized chat application (DApp) that demonstrates secure, private, and censorship-resistant messaging using Ethereum. The front-end is built with Next.js and the smart contracts are built/deployed using Hardhat and Solidity. Wallet integration uses MetaMask.

Key goals:
- Decentralized messaging using Ethereum smart contracts
- MetaMask authentication and wallet-based identity
- End-to-end encrypted chat payloads (app-layer encryption)

Contents
- Next.js front-end (components, pages, styles)
- Smart contract: `contracts/ChatApp.sol`
- Deployment scripts: `scripts/deploy.js`
- Tests: `test/` (Hardhat tests)
- Config: `hardhat.config.js`, `next.config.js`

Features
- Secure and private blockchain-based messaging
- MetaMask wallet authentication
- Smart contract logic on an EVM-compatible chain
- End-to-end encrypted messages stored/relayed via contracts

Prerequisites
- Node.js (v18.17.1 or higher)
- npm (comes with Node) or yarn/pnpm
- MetaMask browser extension
- VS Code (recommended)

Quick setup (local development)
1. Clone this repository:

```cmd
git clone https://github.com/BeingAnurag/DChat.git
cd "c:\Users\Anurag Kr\Downloads\dchat"
```

2. Install dependencies:

```cmd
npm install
```

3. Create a `.env` file in the repo root with your keys (example):

```
PRIVATE_KEY=your_wallet_private_key (for deployments)
ALCHEMY_API_KEY_OR_URL=https://eth-goerli.g.alchemy.com/v2/your-key
```

Important: `.env` is ignored by `.gitignore`. Never commit private keys.

4. Deploy smart contracts (example to Goerli):

```cmd
npx hardhat run scripts/deploy.js --network goerli
```

5. Start the Next.js dev server:

```cmd
npm run dev
# open http://localhost:3000
```

6. Run Hardhat tests:

```cmd
npx hardhat test
```

Notes on deployment
- Replace `goerli` with any configured network in `hardhat.config.js`.
- For real deployments, use secure secret management for private keys (do not keep them in plaintext locally).

Technologies used
- Next.js (React)
- Solidity (smart contracts)
- Hardhat (development + deployment)
- MetaMask (wallet)
- Ethereum / EVM-compatible chains

Helpful commands
- Install deps: `npm install`
- Start dev server: `npm run dev`
- Deploy contracts: `npx hardhat run scripts/deploy.js --network <network>`
- Run tests: `npx hardhat test`

Creating and pushing the GitHub repo (if needed)
If you haven't created the remote repo on GitHub yet, you can create it on the website and then push:

```cmd
cd "c:\Users\Anurag Kr\Downloads\dchat"
git branch -M main
git remote add origin https://github.com/BeingAnurag/DChat.git
git push -u origin main
```

Or create and push in one step using the GitHub CLI (`gh`):

```cmd
gh repo create BeingAnurag/DChat --public --source=. --remote=origin --push
```

Codespaces, collaborators and next steps
- To start a Codespace: open the repo on GitHub and click "Start coding with Codespaces".
- Add collaborators: GitHub > Settings > Manage access > Invite collaborators by username or email.
- Consider adding a CONTRIBUTING.md and CODE_OF_CONDUCT.md if you expect external collaborators.

Security and privacy
- Keep `.env` and private keys out of source control. Use `.gitignore` (already included) and a secrets manager for production.
- Application-level encryption (E2E) should be managed client-side — private keys never leave the user's device.

License
- This repository is licensed under the MIT License (see `LICENSE`).

More resources
- Hardhat: https://hardhat.org/
- MetaMask: https://metamask.io/
- Remix IDE: https://remix.ethereum.org/

If you'd like, I can:
- Add a CONTRIBUTING.md and simple setup script
- Create a GitHub Actions workflow to run Hardhat tests on push
- Prepare a Codespaces devcontainer configuration

Tell me which of the above you'd like next and I'll implement it.
