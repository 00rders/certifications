### 📘 Notes — Non-Repudiation  
**CompTIA Security+ Objective: 2.8 — Summarize the basics of cryptographic concepts**

---

### 🧠 Core Concepts

**Non-repudiation** ensures that a user or system **cannot deny** performing an action, sending a message, or initiating a transaction.

It provides proof that:
- **The message came from a known sender**
- **The message was not altered**
- **The sender cannot later claim they didn’t send it**

Non-repudiation is built on the combined use of:
- **Authentication** — confirms the sender’s identity
- **Integrity** — verifies the data hasn't been modified
- **Digital signatures** — provide cryptographic evidence of authorship

---

### 🔐 How It Works (Using Asymmetric Cryptography)

- The sender hashes the message, then encrypts the hash with their **private key**  
- This encrypted hash becomes the **digital signature**
- The receiver:
  - Decrypts the signature using the sender’s **public key**
  - Re-hashes the received message
  - Compares the two hashes to confirm the message:
    - Was authored by the sender
    - Was not altered in transit

This method creates **cryptographic accountability**.

---

### 🧾 Use Cases Where Non-Repudiation Is Critical

- **Legal contracts and electronic signatures**
- **Financial transactions and wire transfers**
- **Audit trails and security logs**
- **Email and secure messaging (PGP, S/MIME)**
- **Supply chain integrity (software signing, blockchain)**

---

### 🔐 Why It Matters in Security

- Prevents users or attackers from denying actions that left a trace
- Enables **forensic investigation**, **legal enforcement**, and **policy accountability**
- Essential in environments where actions must be **verifiable and attributable** (e.g., financial services, government, regulated industries)

---

### 💼 Real-World SOC Example

> A finance employee claims they never authorized a wire transfer to an external account.  
> The SOC analyst reviews the logs and finds a digitally signed approval sent via a secure system.  
> Using the employee’s **public key**, they verify the digital signature was created with the employee’s **private key**.  
> The hash matches, confirming the message’s integrity and authorship.  
> The organization proves the action occurred and holds the employee accountable — enabling both legal protection and internal review.

---

*Logged by 00rders*
