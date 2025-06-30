### 📘 Notes — Cryptographic Concepts & Public Key Infrastructure (PKI)  
**CompTIA Security+ Objective: 2.8 — Summarize the basics of cryptographic concepts**

---

### 🧠 Core Concepts

#### Symmetric Encryption
- Uses **one key** to encrypt and decrypt data.
- Fast and efficient — ideal for large amounts of data.
- Major downside: key distribution is difficult and insecure at scale.
- Example: AES (Advanced Encryption Standard)

#### Asymmetric Encryption
- Uses **two keys**:
  - **Public key**: Shared openly, used to **encrypt**
  - **Private key**: Kept secret, used to **decrypt**
- Enables secure communication without sharing private keys.
- Supports features like:
  - **Authentication**
  - **Non-repudiation**
  - **Digital signatures**

#### Key Concepts
- **Key Pair Generation**:
  - Public/private keys are generated together and mathematically linked.
  - Usually created once unless compromised or rotated.

- **Key Escrow**:
  - A third-party system that stores private keys securely.
  - Allows recovery if keys are lost or during legal/investigative access.
  - Can be **internal** or **outsourced** (e.g., to a certificate authority or enterprise vault)

#### Public Key Infrastructure (PKI)
- The entire system managing **asymmetric encryption** and **digital certificates**.
- Provides:
  - **Certificate Authorities (CAs)**: Issue and validate certificates
  - **Registration Authorities (RAs)**: Validate identities before issuing certs
  - **Certificate Revocation Lists (CRLs)** / **OCSP**: Check if certs are revoked
- Enables encrypted web communication (HTTPS), secure email, and user/device authentication.

---

### 🔐 Why It Matters in Security

- Asymmetric encryption enables **trust** in public communications.
- PKI ensures the **authenticity** of digital identities.
- Encryption underpins nearly every secure service — from VPNs to file transfer to SSO.

---

### 💼 Real-World SOC Example

> An employee sends a sensitive document via email using end-to-end encryption.  
> - The recipient encrypts the message with the sender's **public key**.  
> - The sender decrypts it using their **private key**.  
> - Later, auditors review logs showing the **digital signature**, confirming both sender identity and message integrity.  
> - The SOC verifies certificate validity using OCSP before trusting the origin.

---

### ✅ CompTIA Objective Mapping

- **2.8** — Cryptographic concepts: symmetric vs asymmetric, key management, non-repudiation, hashing, PKI
- Includes support concepts used in other objectives (e.g., secure communication protocols, authentication)

---

*Logged by 00rders*
