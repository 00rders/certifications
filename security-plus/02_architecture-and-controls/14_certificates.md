# 06_certificates.md  
**Domain:** 2.0 Architecture and Design  
**Logged by:** 00rders  
**Date:** 2025-06-30  

---

## 🧠 Core Concepts – Certificates

- A **digital certificate** is a digitally signed file that:
  - Binds a **public key** to an identity (user, organization, server)
  - Is issued and signed by a **Certificate Authority (CA)**
- Certificates are structured using the **X.509 standard**
- Core components of a certificate:
  - **Subject** – who the cert is for
  - **Issuer** – who signed it
  - **Public Key** – used in encryption/signature verification
  - **Serial Number** – unique ID
  - **Validity Period** – start/end dates
  - **Signature** – CA's signature over the cert's hash

---

## 🏛️ Trust Models

| Model            | Description                                           |
|------------------|-------------------------------------------------------|
| **CA Model**     | Centralized trust hierarchy (root CA → intermediates) |
| **Web of Trust** | Decentralized; users sign each other’s keys (PGP)     |

---

## 🔐 Digital Signatures – Clarified

- A **digital signature** is:
  - A hash of the data, encrypted with the **sender’s private key**
  - Attached to a message or file
- It does **not** encrypt the message itself
- Provides:
  - ✅ **Integrity** – the message wasn’t altered
  - ✅ **Authentication** – proves sender owns private key

### ⚠️ Weak Spot Patched:
> A digital signature **is not the same** as encrypting a message.  
> It encrypts the **hash**, not the message itself — so no confidentiality is provided.

---

## 📉 Certificate Lifecycle + Revocation

| Status        | Meaning |
|---------------|---------|
| **Valid**     | Within time window, properly signed |
| **Expired**   | Past validity date |
| **Revoked**   | Invalidated early due to compromise, misuse |
| **Self-signed** | Not issued by CA; only trusted if manually added |
| **Broken chain** | Any expired or missing cert in the chain invalidates the whole chain |

**Revocation Check Methods:**
- **CRL (Certificate Revocation List)** – Static list
- **OCSP (Online Certificate Status Protocol)** – Real-time query
- **OCSP Stapling** – Server attaches signed OCSP response to speed things up

---

## 🔒 Common Use Cases

| Use Case                | Cert Type              |
|-------------------------|------------------------|
| HTTPS / Web Security    | TLS/SSL Certificate     |
| Email Signing/Encryption| S/MIME Certificate      |
| Signing Software        | Code Signing Certificate |
| User Auth on VPNs       | Client Certificate       |

---

## 🧪 Real-World SOC Example

> You’re analyzing a phishing domain and inspect its TLS certificate. It’s self-signed and not issued by a trusted CA. The chain is broken. This validates the site is likely spoofed and should be blocked.  
> You check CRL/OCSP status and log the incident.

---

## ⚠️ CompTIA Exam Traps to Avoid

- **Digital signatures ≠ encryption of the message**
- **Self-signed certificates are not inherently bad**, just untrusted by default
- **Code signing ≠ S/MIME** — don’t mix up certificate types
- **OCSP is for revocation**, not encryption
- **CRL is slower**, OCSP is faster and more dynamic

---

## ✅ You Are Exam-Ready If You Can:

- Explain what a digital certificate does and what it's made of  
- Distinguish **digital signatures** from **encryption**
- Identify when a certificate is invalid or revoked
- Choose the right cert type for HTTPS, email, and software signing
- Understand trust chains and the consequences of a broken chain
- Interpret **Web of Trust** vs **CA model**

---

### ✅ Final Mastery: Confirmed via full quiz + trap drill  
**Weak spot resolved**: Code signing ≠ S/MIME  
**Score**: 9/10 + 3/3 (trap drill)

---

