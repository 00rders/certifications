### 📘 Notes — Digital Signatures and Hashing  
**CompTIA Security+ Objective: 2.8 — Summarize the basics of cryptographic concepts**

---

### 🧠 Core Concepts

#### 🔒 Hashing
- A **one-way cryptographic function** that transforms input into a fixed-length string (hash value)
- Key traits:
  - **Deterministic** — same input always yields same hash
  - **Irreversible** — original data can't be derived from the hash
  - **Avalanche effect** — small changes in input cause drastically different output
- Primary use: **data integrity**
- Common algorithms:
  - **SHA-256** — modern, secure, widely used
  - **SHA-1** — deprecated due to collision vulnerabilities
  - **MD5** — deprecated, fast but insecure

#### ✍️ Digital Signatures
- A **cryptographic method** for verifying:
  - **Integrity** — has the message changed?
  - **Authentication** — who sent the message?
  - **Non-repudiation** — the sender cannot deny they sent it
- Uses **asymmetric encryption** to sign the hash of the data

##### 🔁 Workflow:
1. Sender hashes the original message
2. Sender encrypts the hash with their **private key** (creating the signature)
3. Receiver:
   - Decrypts the signature using sender’s **public key**
   - Re-hashes the received message
   - Compares both hashes — if they match, signature is valid

---

### 🔐 Why It Matters in Security

- **Hashing**:
  - Ensures the contents of files, logs, or passwords haven’t changed
  - Used in:
    - File verification (e.g., checksum comparison)
    - Password storage (hash + salt)
    - Message integrity

- **Digital Signatures**:
  - Widely used in:
    - **Secure email** (S/MIME, PGP)
    - **Software/code signing** to prevent tampering
    - **TLS/SSL certificates** for HTTPS websites
    - **Blockchain transactions** and smart contract validation

- Together, these tools form the backbone of **trusted communications** and **data assurance** across systems and networks

---

### 💼 Real-World SOC Example

> A user downloads a third-party software package.  
> The developer provides a `.sig` file and a published SHA-256 hash on their site.  
> The SOC analyst:
> - Verifies the digital signature using the developer’s **public key**
> - Compares the published SHA-256 hash to a freshly computed one
> - Finds the hashes **don’t match**, flagging the file as potentially malicious or corrupted — stopping a supply chain attack before it begins

---

*Logged by 00rders*
