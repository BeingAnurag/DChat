# DChat

DChat is a Web3 encrypted chat application built with Next.js and Hardhat (Solidity). This repository contains the front-end, smart contract, and deployment scripts.

## What is included
- Next.js app (React components, pages, styles)
- Hardhat smart contract (`contracts/ChatApp.sol`)
- Deployment scripts (`scripts/deploy.js`)
- Basic `.gitignore` set for Node, Next.js, and Hardhat

## Quick local steps
1. Install dependencies:

```cmd
cd "c:\Users\Anurag Kr\Downloads\dchat"
npm install
```

2. Start Next dev server:

```cmd
npm run dev
```

3. Run Hardhat tests or local node:

```cmd
npx hardhat test
npx hardhat node
```

## Notes
- Sensitive files like `.env` are ignored by `.gitignore`. Keep private keys and secrets out of source control.
- Create a GitHub repo (see instructions below) then push.
