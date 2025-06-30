# ⛓️ Blockchain  
**CompTIA Security+ — Domain 2: Architecture & Design**  
*Logged by 00rders*

---

## ✅ Core Concept

### 📖 What is Blockchain?
- A **distributed ledger** technology that records transactions **across multiple systems**.
- Designed for **transparency**, **integrity**, and **tamper resistance**.
- Once data is recorded in a block and **cryptographically hashed**, it becomes **nearly impossible to alter without detection**.

---

### 🧩 How It Works
- Transactions are grouped into a **block**.
- Each block includes:
  - Transaction data
  - A **hash of the current block**
  - A **hash of the previous block**
- This creates a **linked chain** of data blocks.
- If any data in a block changes → the hash changes → the **entire chain becomes invalid** unless re-mined by consensus.

---

### 🔍 Security Benefits
- **Integrity:** Altered data is immediately detectable due to hash mismatch.
- **Transparency:** All participants can verify and audit the chain.
- **Decentralization:** No single point of failure — copies exist across all nodes.

---

## 🧠 Real-World SOC Relevance
> While not widely used in day-to-day SOC operations, blockchain **concepts around integrity and tamper evidence** are relevant to secure logging, digital forensics, and next-gen identity management systems.

---

## 🎯 Exam Takeaways
- Blockchain = distributed, append-only ledger  
- Blocks contain data + hashes  
- Integrity is protected via cryptographic linkage  
- Compromised block = broken chain = red flag for tampering

---

*Ready for a super quick 2-question exam-style quiz?*
