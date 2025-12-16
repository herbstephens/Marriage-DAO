# 💍 Smart Marriage Protocol **World Chain Mainnet Deployment — Full Documentation**

This repository contains the smart contracts for the **Smart Marriage Protocol**, deployed on **World Chain Mainnet** during ETHGlobal.  
It includes:  

- Soulbound marriage NFTs  
- Anniversary milestone NFTs  
- A daily-emission ERC20 “TIME” token  
- A HumanBond contract integrating **World ID** for private, verifiable marriage proposals

---

## 📌 Deployed and verified Contract Addresses (World Chain Mainnet)

- **VowNFT** - `0x4Cef5DC94C3C0319F5FABbb6D3d6130d798C3B6F`
- **MilestoneNFT** - `0x0919Df3678039BCe59abdD19D7bf9e7D1b7eb5d8`
- **TimeToken** - `0xE4215A8e6c2ED64832e135ddd220905e666E7E40`
- **HumanBond** - `0x543E4a77A51944C7671c77Dd7B963dD455AB55AD`

---

## 🚀 Deployment Guide (World Chain Mainnet)

### ✅ Prerequisites

Ensure the following are installed/configured:

- Foundry (`forge` >= **1.5.0**)
- OpenZeppelin Contracts
- forge-std
- Contracts compile without errors: forge build
- World ID Router Address confirmed:
0x17B354dD2595411ff79041f930e491A4Df39A278
- .env file with RPC_URL and PRIVATE_KEY are set
- Check Wallet Balance, ensure wallet has 0.05–0.1 ETH on World Chain Mainnet.

### Deploying to World Chain via Script

```bash
forge script script/Deploy.s.sol:DeployScript \
  --rpc-url $WORLDCHAIN_RPC_URL \
  --private-key $PRIVATE_KEY \
  --broadcast \
  --verify \
  -vvvv
```

### Useful Resources

- World Chain RPC: https://rpc.worldchain.org
- Chain ID: 480
- Router: 0x17B354dD2595411ff79041f930e491A4Df39A278
- Group ID: 1
- External Nullifiers: generated during deployment
- World Chain Docs: https://docs.world.org/world-chain
- World ID Docs: https://docs.world.org/world-id

## Contracts Overview

### VowNFT

Soulbound NFT representing a verified marriage.

### MilestoneNFT

**Year and URI**:

Soulbound NFT representing a milestones reached by the couple.

### TimeToken

ERC20 token representing time spent together.

### HumanBond

- World ID verification  
- Proposal flow  
- Acceptance flow  
- VowNFT minting  
- MilestoneNFT minting  
- TimeToken minting  

#### Acknowledgements

Built at ETHGlobal Buenos Aires.
Contracts authored and tested by **Leticia Azevedo**.

#### License

MIT License
