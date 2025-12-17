# SpectrumLedger

Built for Base

SpectrumLedger is a minimal Base-first repository that combines OnchainKit wallet UX with Viem-powered JSON-RPC reads. It’s intended for quick validation of Base connectivity, chainId correctness, and basic account balance checks.

## Highlights

- Targets Base Mainnet (8453) and Base Sepolia (84532)
- Uses OnchainKit for wallet onboarding UI
- Uses Viem to query chainId, block height, and native ETH balance
- Includes Basescan deployment and verification references

## Networks

Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  
RPC: https://sepolia.base.org  

Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  
RPC: https://mainnet.base.org  

## Main File

app/spectrumLedger.ts

At runtime the app:
- Initializes an OnchainKitProvider on the selected Base chain
- Presents wallet connection UI via OnchainKit Wallet
- Reads Base state using Viem:
  - RPC chainId
  - latest block number
  - native balance for a supplied address
- Prints explorer context through Basescan URLs

## Repository Structure

app/  
- spectrumLedger.ts  
  React entry component that wires wallet UX + Base RPC reads.

Recommended companion files:
- package.json
- tsconfig.json
- index.html / main.tsx
- .env (optional)

## Libraries

OnchainKit  
https://github.com/coinbase/onchainkit  

Viem  
RPC client for Base reads

## Installation and Running

Requirements:
- Node.js 18+
- Browser environment with wallet support

Install dependencies and run with a typical React/Vite or Next.js dev server.

Optional environment variables:
- VITE_BASE_RPC_URL
- VITE_BASE_SEPOLIA_RPC_URL

## Author

GitHub: https://github.com/eater-dimmer

Public contact (email): eater.dimmer-0i@icloud.com

X (twitter): https://x.com/modyemad7773

## License

MIT License

## References

createBaseAccount reference:  
https://docs.base.org/base-account/reference/core/createBaseAccount?utm_source=chatgpt.com

Account Abstraction on Base:  
https://docs.base.org/base-chain/tools/account-abstraction?utm_source=chatgpt.com

OnchainKit repository:  
https://github.com/coinbase/onchainkit

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract #1 address:  
0xd4aa0d9efb85f748a6360b4f8f6d56a86fab7295

Deployment and verification:
- https://sepolia.basescan.org/address/0xd4aa0d9efb85f748a6360b4f8f6d56a86fab7295  
- https://sepolia.basescan.org/0xd4aa0d9efb85f748a6360b4f8f6d56a86fab7295/0#code  

Contract #2 address:  
0x0bea09b4c8b48048122e0dd5e861bdeb8a42e545

Deployment and verification:
- https://sepolia.basescan.org/address/0x0bea09b4c8b48048122e0dd5e861bdeb8a42e545
- https://sepolia.basescan.org/0x0bea09b4c8b48048122e0dd5e861bdeb8a42e545/0#code  
