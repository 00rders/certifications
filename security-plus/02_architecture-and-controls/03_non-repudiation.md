### 📘 Notes — Non-Repudiation  
**CompTIA Security+ Objective: 2.8 — Summarize the basics of cryptographic concepts**

---

### 🧠 Core Concepts

**Non-repudiation** ensures that a party **cannot deny** the authenticity of their actions, messages, or transactions.  
It provides verifiable proof that:

- A message or action **originated from a specific sender**
- The content was **not tampered with** in transit
- The sender **cannot deny** having sent the message

Non-repudiation is achieved by combining:

- **Authentication** — Verifies identity  
- **Integrity** — Ensures data is unchanged  
- **Digital signatures** — Bind identity and content cryptographically

---

### 🔐 How Digital Signatures Provide Non-Repudiation

1. **Message is hashed** (e.g., with SHA-256)  
2. The hash is **encrypted with the sender’s private key** — creating the digital signature  
3. The receiver:
   - **Decrypts** the signature using the sender’s public key  
   - Hashes the received message independently  
   - **Compares** the two hashes:
     - If they match: the message is authentic and unaltered  
     - If they differ: tampering is detected

🔁 This process guarantees that only the **private key owner** could have created the signature — and that the message has not been changed.

---

### 🧾 Where Non-Repudiation is Used

- **Digital contracts and e-signatures** (e.g., DocuSign, Adobe Sign)
- **Wire transfers and payment approvals**
- **Software distribution (code signing certs)**
- **Secure messaging** (PGP, S/MIME)
- **Audit logs in regulated environments (SOX, HIPAA, PCI-DSS)**

---

### 🔐 Why It Matters in Security

- Provides legal and forensic evidence in disputes
- Prevents false denials in sensitive operations
- Enables:
  - **Attribution** of actions to users
  - **Enforcement** of corporate policy
  - **Trust** in automated and remote transactions

---

### 💼 Real-World SOC Example

> A user claims they never submitted a privileged access request.  
> The SOC analyst pulls system logs showing the request was signed with the user’s private key.  
> The analyst:
> - Verifies the digital signature using the user’s public key  
> - Matches the message hash to the signed hash  
> - Confirms authorship and integrity  
>  
> The evidence proves the user initiated the request — satisfying compliance and preventing false repudiation.

---

*Logged by 00rders*
