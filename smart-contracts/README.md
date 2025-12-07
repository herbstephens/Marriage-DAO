# 💍 Smart Marriage Protocol **World Chain Mainnet Deployment — Full Documentation**

This repository contains the smart contracts for the **Smart Marriage Protocol**, deployed on **World Chain Mainnet** during ETHGlobal.  
It includes:  

- Soulbound marriage NFTs  
- Anniversary milestone NFTs  
- A daily-emission ERC20 “TIME” token  
- A HumanBond contract integrating **World ID** for private, verifiable marriage proposals

---

## 📌 Deployed and verified Contract Addresses (World Chain Mainnet)

- **VowNFT** - `0xa1650cc531C2780FB8C006F4B8D314018F7f9ac9`
- **MilestoneNFT** - `0x0a2759241D0cb610e3E61dB351813ddF8A52F14c`
- **TimeToken** - `0x261F6d89491cbaDFf7813303363a514f4b226A82`
- **HumanBond** - `0x6494daa4e693F748Eb0a16041ECfCEd51392bB13`

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
