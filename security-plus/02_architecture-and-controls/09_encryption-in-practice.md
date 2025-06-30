### 📘 Notes — Data Encryption  
**CompTIA Security+ Objective: 2.8 — Summarize the basics of cryptographic concepts**

---

### 🧠 Core Concepts

#### 🔒 What Is Encryption?
- The process of **converting plaintext into ciphertext** using a mathematical algorithm and key.
- Only authorized users with the correct **decryption key** can convert the data back into readable form.

---

#### 🧭 Types of Encryption

- **Symmetric Encryption**
  - Uses **one key** for both encryption and decryption.
  - Fast and efficient — ideal for encrypting **large volumes of data** (e.g., full disk encryption).
  - Key challenge: Secure **key distribution** between sender and receiver.
  - Examples: AES, DES, 3DES, RC4

- **Asymmetric Encryption**
  - Uses a **key pair**: **Public key** (shared) and **Private key** (kept secret).
  - Public key encrypts; private key decrypts.
  - Enables **secure communication** without needing to pre-share keys.
  - Used in: Email security, key exchanges, digital signatures
  - Examples: RSA, ECC, DSA

- **Hybrid Encryption**
  - Common in modern protocols like TLS.
  - Uses **asymmetric encryption** to securely exchange a **symmetric key** for the session.
  - Combines speed and security.

---

### 📦 Data States and Encryption

- **Data at Rest**: On hard drives, SSDs, databases  
  - Use: BitLocker, FileVault, full-disk encryption, database encryption

- **Data in Transit**: Sent across networks  
  - Use: TLS, VPN, SSH, IPsec

- **Data in Use**: Actively processed by systems  
  - Typically harder to protect, but solutions include encrypted memory or secure enclaves.

---

### 🔁 Cryptographic Strength and Evolution

- **Longer keys = stronger encryption**, but more CPU/memory overhead.
- As **processing power increases** (e.g., faster CPUs, quantum computing threats), older algorithms or short key lengths become **vulnerable** to brute-force attacks.
  - Example: DES (56-bit) is obsolete; AES-256 is considered strong.
- **Regular key rotation** and **algorithm updates** are crucial to stay secure.
- **Multi-layer encryption** (encrypting data multiple times using different keys or algorithms) adds defense-in-depth but can impact performance.

---

### ⚖️ Tradeoffs: Performance vs Security

- **Symmetric encryption**: High speed, low latency — best for bulk data
- **Asymmetric encryption**: Strong trust model, but slower — best for authentication, key exchange
- Smart systems **combine both** in hybrid models for optimal performance and security

---

### 🔐 Why It Matters in Security

- Protects data against theft, interception, and unauthorized access
- Required for compliance (HIPAA, PCI-DSS, GDPR, etc.)
- Encrypted data (without key compromise) is often **not legally reportable** if breached
- Core to:
  - **Confidentiality** (CIA triad)
  - **Trust** between users, services, and organizations

---

### 💼 Real-World SOC Example

> A healthcare employee’s laptop is stolen.  
> It was encrypted using AES-256 with BitLocker and TPM authentication.  
> No reportable breach occurred because encryption protected **data at rest**.  
> The SOC analyst verified the encryption policy and logged the event as non-critical.

---

### ✅ CompTIA Objective Mapping

- **Domain**: 2.8 — Cryptographic concepts  
- **Relevance**: Encryption enables secure data exchange and access control at every layer of the security stack.

---

**Logged by 00rders**
