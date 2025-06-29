### 📘 Notes — CIA Triad: Confidentiality, Integrity, Availability  
**CompTIA Security+ Objective: 2.8 — Summarize the basics of cryptographic concepts**

---

### 🧠 Core Concepts

The **CIA Triad** is the foundation of all information security models:

- **Confidentiality**  
  - Prevents unauthorized access to data  
  - Methods: Encryption, access controls, classification, need-to-know policies

- **Integrity**  
  - Ensures data is accurate and unaltered  
  - Methods: Hashing, checksums, digital signatures, version control

- **Availability**  
  - Ensures systems and data are accessible when needed  
  - Methods: Redundancy, backups, failover, DDoS protection, uptime SLAs

These three principles work together to secure systems holistically — compromising one often affects the others.

---

### 🔐 Why It Matters in Security

- Every security control should map back to at least one part of the CIA triad
- Helps analysts evaluate risks, justify controls, and structure responses
- The triad is baked into compliance frameworks, audits, and best practices

---

### 💼 Real-World SOC Example

> A DDoS attack takes down a public website.  
> - **Availability** is compromised.  
> - The SOC team activates a failover CDN and blocks malicious IPs.  
> - Once restored, they verify the **Integrity** of logs and **Confidentiality** of user data wasn’t affected.
