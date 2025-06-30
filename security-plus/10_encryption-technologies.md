# 🔐 Encryption Technologies  
**CompTIA Security+ — Domain 2: Architecture & Design**  
*Logged by 00rders*

---

## ✅ Core Encryption Hardware and Systems

### 🧩 Trusted Platform Module (TPM)
- A **dedicated cryptographic chip** built into a device's motherboard.
- Used for **local, hardware-bound encryption** (e.g., full disk encryption).
- Stores:
  - Encryption keys
  - Digital certificates
  - Password hashes
- Commonly used in: **BitLocker**, BIOS integrity checks.
- Cannot be moved or cloned → tied to a specific system.

---

### 🧩 Hardware Security Module (HSM)
- A **standalone physical device** used to generate, store, and manage encryption keys at scale.
- Supports **high-volume cryptographic operations**.
- Ideal for:
  - Cloud and enterprise infrastructure
  - SSL/TLS acceleration
  - Certificate authorities
- Often compliant with **FIPS 140-2** standards.

---

### 🧩 TPM vs. HSM

| Feature        | TPM                                  | HSM                                      |
|----------------|---------------------------------------|------------------------------------------|
| Location       | Embedded in motherboard              | External appliance or USB-based module   |
| Use Case       | Local key storage & boot verification | Centralized key management & acceleration |
| Performance    | Basic                                | High-speed crypto operations             |
| Example        | BitLocker                            | AWS CloudHSM, Azure Key Vault            |

---

### 🧩 Key Management System (KMS)
- Centralized platform to manage encryption keys across systems.
- Can be **on-prem** or **cloud-based** (e.g., AWS KMS, Azure Key Vault).
- Features:
  - Key generation, rotation, revocation
  - Role-based access control
  - Logging and auditing

---

### 🧩 Secure Enclave
- A **hardware-isolated processor area** inside a CPU.
- Stores **biometrics and cryptographic operations** separately from main OS and apps.
- Common in:
  - Apple devices (Touch ID, Face ID)
  - Intel SGX (Software Guard Extensions)
- Purpose: **Protect sensitive data even if the OS is compromised**.

---

## 🧠 Real-World SOC Application
> In an enterprise breach investigation, a SOC analyst may confirm that encryption keys were stored inside an **HSM**, preventing attackers from retrieving them even with system-level access. Meanwhile, **TPM logs** could verify that no unauthorized boot tampering occurred on affected workstations.

---

## 🎯 Exam Reinforcement Takeaways
- TPM = **single device** protection (e.g., laptop)  
- HSM = **enterprise-scale** key storage  
- KMS = **central management** for keys  
- Secure Enclave = **isolated zone** for sensitive operations  

---

*Ready for next video — or request a drill review if needed.*
