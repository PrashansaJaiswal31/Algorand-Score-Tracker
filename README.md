# 🎯 Score Tracker dApp on Algorand

## 📌 Project Description
My dApp is a **XXX** built on the Algorand blockchain.  
It is designed to provide a simple and interactive way to **track scores** securely on-chain.  
This project is perfect for beginners exploring **Algorand smart contracts** using **TypeScript**.

---

## 🚀 What it does
The **Score Tracker** dApp allows users to:
- Add points to a score  
- Subtract points from a score  
- Reset the score to zero  
- Read the current score anytime  

All these operations are stored on the **Algorand blockchain**, ensuring **security, immutability,<img width="1470" height="956" alt="Screenshot 2025-09-06 at 3 46 06 PM" src="https://github.com/user-attachments/assets/017b7b2a-4b9c-4644-b9ba-53e38a094866" />
 and transparency**.


---

## ✨ Features
- ✅ Built with **Algorand TypeScript SDK**  
- ✅ On-chain **score tracking** using `GlobalState`  
- ✅ Easy-to-understand smart contract structure  
- ✅ Beginner-friendly code for learning dApps  
- ✅ Extendable for **games, competitions, or reward systems**  

---

## 🔗 Deployed Smart Contract
Contract Link: https://lora.algokit.io/testnet/application/745464544

---

## 🛠️ Smart Contract Code
```ts
//paste your code
import { Contract, GlobalState, uint64 } from "@algorandfoundation/algorand-typescript";

// Score Tracker Contract
export class ScoreTracker extends Contract {

  // global state to store score
  score = GlobalState<uint64>({ key: "score", initialValue: 0 });

  // function to increase score
  addScore(points: uint64): uint64 {
    this.score.value = this.score.value + points;
    return this.score.value;
  }

  // function to decrease score
  subtractScore(points: uint64): uint64 {
    this.score.value = this.score.value - points;
    return this.score.value;
  }

  // function to reset score
  resetScore(): uint64 {
    this.score.value = 0;
    return this.score.value;
  }

  // function to read score
  getScore(): uint64 {
    return this.score.value;
  }
} 


<img width="1470" height="956" alt="Screenshot 2025-09-06 at 3 46 06 PM" src="https://github.com/user-attachments/assets/6c0b93eb-0089-4a0b-b287-bdfb6cc2a16d" />
