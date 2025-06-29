### 📘 Notes — Non-Repudiation  
**CompTIA Security+ Objective: 2.8 — Summarize the basics of cryptographic concepts**

---

### 🧠 Core Concepts

- **Non-repudiation** ensures that a party **cannot deny** the authenticity of a message, action, or transaction.
- Built on a combination of:
  - **Authentication** — verifying identity
  - **Integrity** — ensuring data hasn’t changed
  - **Digital Signatures** — proving the sender and contents are valid

- Typically achieved using **asymmetric cryptography**:
  - Sender signs data with their **private key**
  - Anyone can verify it using the **public key**

---

### 🔐 Why It Matters in Security

- Critical for trust in communication, especially in:
  - Legal documents
  - Financial transactions
  - Secure email and messaging
- Prevents users from falsely claiming “I didn’t send that” or “That wasn’t me”

---

### 💼 Real-World SOC Example

> A user denies submitting a wire transfer request.  
> - The SOC analyst checks the digital signature on the transaction.  
> - It was signed with the user’s **private key** and verified with their **public key**, proving authorship.  
> - The organization confirms the action was legitimate and holds the user accountable.
