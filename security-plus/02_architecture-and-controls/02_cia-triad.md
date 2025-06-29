### 📘 Notes — CIA Triad: Confidentiality, Integrity, Availability  
**CompTIA Security+ Objective: 2.8 — Summarize the basics of cryptographic concepts**

---

### 🧠 Core Concepts

The **CIA Triad** is the foundational model of information security.  
It outlines the three core goals that every security control, system, and policy must support:

---

#### 🔒 Confidentiality — *Keep it private*
- Prevents unauthorized access to sensitive data
- Maintains privacy and discretion
- Enforced using:
  - **Encryption** (e.g., AES, TLS)
  - **Access controls** (ACLs, RBAC)
  - **Data classification**
  - **Least privilege policies**
- Common threats:
  - Data breaches
  - Eavesdropping/sniffing
  - Insider theft

---

#### 🧾 Integrity — *Keep it accurate*
- Ensures data remains **unaltered, authentic, and consistent**
- Verifies that information has not been modified maliciously or accidentally
- Enforced using:
  - **Hashing** (e.g., SHA-256)
  - **Checksums**
  - **Digital signatures**
  - **Version control**
- Common threats:
  - Tampering
  - Man-in-the-middle attacks
  - Faulty updates or corrupted backups

---

#### 🟢 Availability — *Keep it accessible*
- Ensures data, systems, and services are **available when needed**
- Supports operational continuity
- Enforced using:
  - **Redundancy** (RAID, clustering)
  - **Backups and restores**
  - **DDoS mitigation**
  - **High-availability architecture (HA)**
- Common threats:
  - Hardware failure
  - Denial-of-service attacks
  - Natural disasters

---

### 🔄 Triad Interdependence

- A compromise to **one element often affects the others**
  - Example: A DDoS (availability) attack could obscure or delay integrity checks
  - Example: An over-restrictive control meant to ensure confidentiality could harm availability

---

### 🔐 Why It Matters in Security

- Every security decision — from firewall rules to password policies — should support at least one CIA principle
- The triad forms the **core lens** through which analysts:
  - Assess threats
  - Justify controls
  - Prioritize incident response
- Also used to:
  - Evaluate risk
  - Write policies
  - Comply with frameworks (e.g., NIST, ISO 27001, PCI-DSS)

---

### 💼 Real-World SOC Example

> A company’s main e-commerce site is hit by a DDoS attack.  
> - **Availability** is disrupted, blocking customer access  
> - The SOC team routes traffic through a backup CDN and begins blocking malicious IPs  
> - Post-recovery, they verify:
>   - Log **integrity** (no tampering occurred during downtime)  
>   - **Confidentiality** was maintained (no exposed PII or credentials)  
> - This layered response shows how the CIA triad remains central during incident handling

---

*Logged by 00rders*
