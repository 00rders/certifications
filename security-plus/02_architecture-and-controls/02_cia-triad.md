### 📘 Notes — CIA Triad: Confidentiality, Integrity, Availability  
**CompTIA Security+ Objective: 2.8 — Summarize the basics of cryptographic concepts**

---

### 🧠 Core Concepts

The **CIA Triad** is the foundation of cybersecurity. It defines the three core objectives that all security mechanisms must enforce:

---

#### 🔒 Confidentiality — *Prevent Unauthorized Access*
- **Goal:** Ensure only authorized users can view sensitive information.
- **Methods:**
  - Encryption (AES, TLS)
  - Access controls (RBAC, ACLs)
  - Need-to-know policies
  - Data classification
- **Threats:**
  - Data breaches
  - Insider threats
  - Eavesdropping

---

#### 🧾 Integrity — *Preserve Data Accuracy*
- **Goal:** Ensure data is unmodified, authentic, and reliable.
- **Methods:**
  - Hashing (SHA-256)
  - Checksums and file integrity monitoring
  - Digital signatures
  - Version control systems
- **Threats:**
  - Tampering (e.g., MITM attacks)
  - Corrupt files or software
  - Unauthorized database changes

---

#### 🟢 Availability — *Maintain Timely Access*
- **Goal:** Ensure systems and data are accessible when needed.
- **Methods:**
  - Redundancy (RAID, clustering)
  - Backup and disaster recovery
  - DDoS protection and uptime SLAs
  - High availability architecture
- **Threats:**
  - DDoS attacks
  - Power outages
  - Hardware failure

---

### ⚖️ Interdependence of the Triad

- **Compromising one element often affects the others:**
  - A ransomware attack affects **availability**, may compromise **confidentiality**, and undermines **integrity**
  - Over-encryption to protect **confidentiality** could reduce **availability** for valid users

---

### 🔐 Why It Matters in Security

- Every control or policy should support at least one CIA pillar
- Analysts use the triad to:
  - Evaluate risks and prioritize incident response
  - Design security architecture
  - Align with compliance standards (NIST, ISO, HIPAA)

---

### 💼 Real-World SOC Example

> A healthcare provider is hit by a DDoS attack on its online portal.  
> - **Availability** is compromised — patients can’t access services.  
> - The SOC team activates geo-blocking and failover DNS routing.  
> - After recovery, logs are verified for **integrity**, and no **confidential** patient data was exposed.  
> - The event is documented to improve triad-aligned resilience for future incidents.

---

*Logged by 00rders*
