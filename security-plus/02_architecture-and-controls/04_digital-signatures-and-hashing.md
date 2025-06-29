### 📘 Notes — Digital Signatures and Hashing  
**CompTIA Security+ Objective: 2.8 — Summarize the basics of cryptographic concepts**

---

### 🧠 Core Concepts

- **Hashing**  
  - One-way cryptographic function that outputs a fixed-length value  
  - Used to ensure **data integrity**  
  - Common algorithms: SHA-256, MD5 (deprecated)
  - If even one bit changes, the hash output changes drastically

- **Digital Signatures**  
  - Combines **hashing** with **asymmetric encryption** to prove:  
    - **Integrity**: Has the message been altered?  
    - **Authentication**: Who sent the message?  
    - **Non-repudiation**: Can the sender deny sending it?
  - Workflow:
    1. Sender hashes the message
    2. Sender encrypts the hash with their **private key** (signature)
    3. Receiver decrypts with **sender's public key** and compares hashes

---

### 🔐 Why It Matters in Security

- Hashing allows for quick and secure verification of files, passwords, and logs
- Digital signatures are used in:
  - Secure email (S/MIME, PGP)
  - Software signing
  - TLS/SSL certificates
- Both are critical for ensuring **trust** in data exchange and system integrity

---

### 💼 Real-World SOC Example

> A software package downloaded by a user comes with a `.sig` file and a hash value on the developer’s website.  
> - The SOC analyst uses the developer’s **public key** to verify the signature and ensure the file hasn’t been tampered with  
> - If the hash doesn’t match, the file is flagged as potentially c
