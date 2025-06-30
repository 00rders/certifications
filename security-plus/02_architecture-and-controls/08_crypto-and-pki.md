### 📘 Notes — Cryptographic Concepts & Public Key Infrastructure (PKI)  
**CompTIA Security+ Objective: 2.8 — Summarize the basics of cryptographic concepts**

---

### 🧠 Core Concepts

#### 🔐 Symmetric Encryption — *"One key to rule them all"*
- Uses the **same key** to encrypt and decrypt data.
- ✅ **Fast**, lightweight, and ideal for bulk data (e.g., full disk encryption)
- ❌ Downside: **Key distribution risk** — both parties must securely share the key
- 📦 Common algorithms: **AES**, **3DES**, **Blowfish**

#### 🔐 Asymmetric Encryption — *"Two keys for secure exchange"*
- Uses a **key pair**:
  - **Public key** → used to **encrypt** or verify
  - **Private key** → used to **decrypt** or sign
- Powers:
  - **Secure key exchange**
  - **Digital signatures**
  - **Email/message encryption**
  - **Authentication (e.g., SSH, HTTPS)**

#### 🔁 Hybrid Encryption — *Best of both worlds*
- **Asymmetric encryption** used to exchange a session key
- That key is then used with **symmetric encryption** for speed
- Common in TLS, PGP, VPN tunnels

---

### 🔑 Key Management Concepts

#### 🧪 Key Pair Generation
- Keys are generated **mathematically linked** (e.g., RSA, ECC)
- Public key is freely shared; private key must be **stored securely**

#### 🧳 Key Escrow
- A **trusted third-party** (internal or external) stores encryption keys
- Enables:
  - **Recovery** in case of loss
  - **Compliance** and lawful access (with proper authorization)
- Often used in enterprise environments and government sectors

---

### 🏛️ Public Key Infrastructure (PKI)

**PKI** is a trust framework used to manage **digital certificates** and **asymmetric encryption**.

#### PKI Core Components:

| Component | Role |
|-----------|------|
| **Certificate Authority (CA)** | Issues and signs certificates |
| **Registration Authority (RA)** | Verifies user identities on behalf of the CA |
| **Certificates (X.509)** | Bind public keys to identities |
| **CRL (Certificate Revocation List)** | Offline list of revoked certificates |
| **OCSP (Online Certificate Status Protocol)** | Real-time certificate status check |
| **Key Recovery Agent (KRA)** | Recovers lost keys in key escrow systems |
| **Trust Model** | Defines how trust is built (hierarchical, web-of-trust, etc.) |

---

### 🧠 Exam Tips

- **Symmetric = fast, 1 key**, but has key distribution risk  
- **Asymmetric = slow, 2 keys**, used for signatures and secure key exchange  
- **Digital certificates** prove identity, not encrypt data  
- **PKI = infrastructure**, not an algorithm  
- Know **OCSP = real-time** and **CRL = static list**

---

### 🔐 Why It Matters in Security

- Enables **confidentiality** across untrusted networks (e.g., internet)
- Verifies **authenticity and identity** using digital signatures
- Supports:
  - **HTTPS / TLS**
  - **Email signing/encryption (PGP, S/MIME)**
  - **VPNs, SSH, software updates**

---

### 💼 Real-World SOC Example

> A user connects to a secure internal site over HTTPS.  
> - The server presents a digital certificate from the internal **CA**  
> - The browser performs an **OCSP** check to verify it’s valid and not revoked  
> - A **TLS session** is negotiated using hybrid encryption  
> - Data is exchanged using **symmetric AES**, but session keys were exchanged using **RSA (asymmetric)**  
> - SOC analysts verify the certificate chain and signature trust path when investigating alerts

---

### ✅ CompTIA Objective Mapping

- **2.8 — Cryptographic Concepts**
  - Symmetric vs. Asymmetric
  - Key management and escrow
  - PKI components
  - Certificate revocation (CRL vs. OCSP)
  - Digital signature use cases

---

*Logged by 00rders*
