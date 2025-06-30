### 📘 Notes — Data Encryption  
**CompTIA Security+ Objective: 2.8 — Summarize the basics of cryptographic concepts**

---

### 🧠 Core Concepts

#### 🔒 What Is Encryption?
Encryption is the process of converting **plaintext** into **ciphertext** using an algorithm and a key.  
Only those with the correct **decryption key** can restore the original data.

Encryption provides:
- **Confidentiality** (primary goal)
- **Data integrity** (when paired with hashing or signing)
- **Regulatory compliance** and **breach reduction**

---

### 🔐 Types of Encryption

#### 🔸 Symmetric Encryption
- Uses **one shared key** for both encryption and decryption
- ✅ Fast, efficient — ideal for **bulk data**
- ❌ Key distribution can be risky
- 📦 Common algorithms: **AES**, **3DES**, **Blowfish**, **RC4**

#### 🔸 Asymmetric Encryption
- Uses a **key pair**:
  - **Public key** → encrypts
  - **Private key** → decrypts
- ✅ Great for **key exchange**, **digital signatures**, and **identity verification**
- ❌ Slower and more resource-intensive
- 📦 Common algorithms: **RSA**, **ECC**, **DSA**

#### 🔸 Hybrid Encryption
- Combines asymmetric and symmetric encryption
- Common in:
  - **TLS/HTTPS**
  - **PGP**
  - **VPN tunnels**
- Strategy:
  1. Use **asymmetric encryption** to securely share a session key
  2. Use **symmetric encryption** for the actual data transfer

---

### 📦 Data States & Encryption Strategies

| Data State      | Description                          | Common Encryption Tools         |
|------------------|--------------------------------------|----------------------------------|
| **At Rest**     | Stored on devices or drives          | BitLocker, FileVault, VeraCrypt |
| **In Transit**  | Moving across networks               | TLS, IPsec, SSH, HTTPS          |
| **In Use**      | Actively processed in memory         | Secure Enclaves, Encrypted RAM  |

> 🔐 *"Data in Use" is the hardest to protect — relies on trusted platform modules (TPM) or secure CPU zones.*

---

### 📈 Cryptographic Strength & Key Management

- **Key length** directly affects security strength (e.g., AES-256 > AES-128)
- **Brute-force resistance** depends on key length + algorithm
- 🔁 Use:
  - **Key rotation** (scheduled key refresh)
  - **Expiration dates**
  - **Revocation mechanisms** (esp. for asymmetric keys)

> 🚫 Weak algorithms like **DES** and **MD5** are no longer secure — avoid on exams and in practice.

---

### ⚖️ Tradeoffs: Performance vs Security

| Factor         | Symmetric               | Asymmetric               |
|----------------|--------------------------|---------------------------|
| Speed          | ✅ Fast                  | ❌ Slow                  |
| Key Sharing    | ❌ Requires pre-shared   | ✅ Secure exchange       |
| Use Case       | Bulk data, file systems | Auth, signatures, keys   |

> 🧠 *Hybrid systems (like TLS) exist to leverage the best of both.*

---

### 🔐 Why It Matters in Security

- Encryption supports **Confidentiality**, a pillar of the **CIA Triad**
- Encrypted data is often **exempt from breach disclosure laws**
- Mandatory for compliance: **HIPAA, PCI-DSS, GDPR**
- Core to:
  - **VPNs**
  - **Cloud workloads**
  - **Wireless protection (WPA2/3)**

---

### 💼 Real-World SOC Example

> A hospital employee reports a stolen laptop.  
> SOC verifies that **BitLocker with AES-256** was enabled and TPM was configured.  
> Since the data at rest is encrypted and keys are protected, **no breach disclosure** is required.  
> Incident is logged as “non-critical with controls effective.”

---

### ✅ CompTIA Objective Mapping

- **2.8 — Cryptographic Concepts**
  - Symmetric vs. Asymmetric
  - Hybrid encryption
  - Data states and encryption strategy
  - Key strength, rotation, and risk mitigation

---

**Logged by 00rders**
