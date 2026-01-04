# 💍 Smart Marriage Protocol **World Chain Mainnet Deployment — Full Documentation**

This repository contains the smart contracts for the **Smart Marriage Protocol**, deployed on **World Chain Mainnet** during ETHGlobal.  
It includes:  

- Soulbound marriage NFTs  
- Anniversary milestone NFTs  
- A daily-emission ERC20 “TIME” token  
- A HumanBond contract integrating **World ID** for private, verifiable marriage proposals

---

## 📌 Deployed and verified Contract Addresses (World Chain Mainnet)

- **VowNFT** - `0x8c64c304854F9284ddb976918dF37Bd4f5949F22`
- **MilestoneNFT** - `0x566c4a366625F08A714dd092f8bD2F0E86f906f5`
- **TimeToken** - `0x39e629681a9db65D9352961d8dCD4C96C4A1169a`
- **HumanBond** - `0xB3cbCB0294995FE1aCD7187B94aEDBD4555c5A63`

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
