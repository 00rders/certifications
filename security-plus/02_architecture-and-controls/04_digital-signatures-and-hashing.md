### 📘 Notes — Digital Signatures and Hashing  
**CompTIA Security+ Objective: 2.8 — Summarize the basics of cryptographic concepts**

---

### 🧠 Core Concepts

#### 🔒 Hashing
- A **one-way mathematical function** that converts input data into a fixed-length value (hash digest)
- Critical characteristics:
  - **Deterministic** — Same input always yields the same output
  - **Non-reversible** — You cannot reconstruct original input from the hash
  - **Collision-resistant** — It’s difficult to find two different inputs that produce the same hash
  - **Avalanche effect** — Tiny input changes create drastically different outputs
- **Purpose**: Ensures **integrity** of data

🛠️ **Hashing Algorithms**:
- `SHA-256`: Secure, modern standard (used in blockchain, SSL, etc.)
- `SHA-1`: Deprecated due to collision weaknesses
- `MD5`: Fast, but broken — no longer trusted

---

#### ✍️ Digital Signatures
- A **cryptographic method** to verify:
  - ✅ **Integrity** — Has the content changed?
  - ✅ **Authentication** — Who sent it?
  - ✅ **Non-repudiation** — Proof the sender can’t deny it

🔑 **Built using asymmetric encryption**:
- Private key: Used to **sign**
- Public key: Used to **verify**

🔁 **Process Workflow**:
1. Sender hashes the message
2. Hash is **encrypted with sender’s private key** → this is the digital signature
3. Receiver:
   - Decrypts the signature with sender’s **public key**
   - Re-hashes the received message
   - Compares hashes: If they match → message is authentic and unchanged

---

### 🧪 Common Uses in Security

- **Hashing**:
  - Password storage (e.g., salted hashes in `/etc/shadow`)
  - File verification (e.g., integrity checks with SHA-256)
  - Log auditing and timestamp verification
- **Digital Signatures**:
  - Email signing (PGP, S/MIME)
  - Code signing (Microsoft Authenticode, Apple Developer ID)
  - HTTPS (TLS handshake involves digital certs with signed keys)
  - Blockchain transactions (e.g., Bitcoin uses ECDSA signatures)

---

### 🔐 Why It Matters in Security

- **Hashing** maintains data **integrity** across systems, especially in environments where storage, transfer, or validation is involved
- **Digital signatures** bind identity to action, creating **trust** between parties and **proof of authorship**
- Together, they enable:
  - Safe updates and patching
  - Secure remote work (VPN, TLS)
  - Tamper detection in logs, backups, and software supply chains

---

### 💼 Real-World SOC Example

> A user downloads a firmware update from a third-party vendor.  
> The update includes a `.sig` digital signature and a published SHA-256 hash.  
> The SOC team:
> - Validates the signature using the vendor’s **public key**  
> - Recomputes the SHA-256 hash on the downloaded file  
> - Finds a **mismatch**, suggesting file tampering  
>  
> As a result, the SOC halts deployment — preventing a **potential supply chain compromise**.

---

### ✅ CompTIA Objective Mapping

- **2.8** — Understand and apply:
  - Hashing
  - Digital signatures
  - Message integrity
  - Authentication
  - Non-repudiation

---

*Logged by 00rders*
