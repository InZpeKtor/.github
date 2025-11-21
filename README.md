# inZpeKtor — Product Documentation

## Overview  
Today the team validated the core idea, iterated on the product, and we’re fully aligned on the final direction for **inZpeKtor**.  
The project originally targeted blockchain protocols that wanted to verify their users through our Clean Hands Proof integration.  
After valuable feedback from mentors, we shifted our focus toward **institutions and banks** that require strong, privacy-preserving identity verification through the **inZpeKtor ID**.

This document explains the updated product flow, reputation system, and current development progress.

---

## 1. inZpeKtor ID Flow  

### **Account Creation**
1. Users log into the **inZpeKtor** web platform.  
2. The platform requests account creation and identity linkage.

### **ZK Proof Generation**
Users generate a Zero-Knowledge proof that verifies:

- **Linked to a KYC identity**  
- **Proof of Life** (face scan)  
- **OFAC screening passed** *(automated)*  
- **USDC blacklist screening passed** *(automated)*  

If all checks succeed, the user receives an **inZpeKtor ID**, issued as an **NFT credential**.

### **ID Renewal Policy**
- inZpeKtor IDs must be renewed **every 90 days**.  
- Each renewal requires generating a fresh ZK proof.  

---

## 2. On-Chain Reputation System  

Every wallet tied to an inZpeKtor ID receives a **reputation score** based on its on-chain behavior.

### **Scoring Rules**
- Interaction with **verified safe addresses**: **+20 points**  
- Connection to any **SCF-related entity**: **+10 points**  
- Sending funds to a **Stellar DeFi protocol**: *small positive score* (to encourage ecosystem participation)

### **Reputation Levels**
| Score Range | Level               | Description                   |
|-------------|---------------------|-------------------------------|
| **0–10**    | ❌ SCAM             | Not authorized                |
| **10–20**   | ⚠️ Medium           | Average trust                 |
| **20–40**   | ✔️ Good             | Healthy behavior              |
| **40–50+**  | ⭐ Very Good        | Highly trustworthy            |

All checks and interactions are designed to be **cryptographically verifiable**.

---

## 3. Architecture & Development Progress  

We are now actively shaping the architecture of inZpeKtor, building the smart contracts, and implementing the first ZK-based features.

### **Current Achievements**
- Completed the **first functional ZK circuit**  
- Defined user flows and ID lifecycle  
- Designed the scoring logic for reputation  

### **Challenges & Learning**
Since no one on the team had fully implemented ZK systems before, the integration has required significant learning and experimentation.  
Despite this, the team successfully built the foundational ZK circuit and continues advancing.

### **Next Steps**
We are currently researching and testing integration with **Boundless** to streamline proof generation and verification pipelines.

---

## 4. Roadmap (Short-Term)
- Finalize ZK proof integration  
- Deploy first version of inZpeKtor ID smart contracts  
- Implement on-chain reputation scoring logic  
- Integrate Boundless to optimize performance  
- Launch early demo for institutional partners  

---

## 5. Summary  

**inZpeKtor** is evolving into a privacy-preserving identity and reputation layer designed for institutions and banks in need of strong AML-aligned verification.  
With ZK proofs, on-chain credentials, and a verifiable reputation engine, inZpeKtor aims to enable **clean, compliant, and private crypto interactions**.

---

*Maintained by the inZpeKtor Team*  
