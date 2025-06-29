### 📘 Notes — Authentication, Authorization, and Accounting (AAA)  
**CompTIA Security+ Objective: 4.1 — Compare authentication, authorization, and accounting concepts**

---

### 🧠 Core Concepts

- **Authentication**: Proves identity  
  - Example: Password, fingerprint, smart card
  - May use **factors** (something you know, have, are)

- **Authorization**: Grants access to resources  
  - Example: File permissions, role-based access
  - Often based on policies, roles, or attributes

- **Accounting**: Tracks and logs activity  
  - Example: Access logs, session records, audit trails
  - Supports auditing and forensic investigations

---

### 🔐 Why It Matters in Security

- AAA is foundational to **access control models**.
- Every secure system must:
  - Prove identity
  - Limit access appropriately
  - Log what happened
- Helps with compliance, incident response, and insider threat detection

---

### 💼 Real-World SOC Example

> A user logs into a VPN (Authentication), accesses a secure financial report (Authorization), and the access is recorded in the SIEM (Accounting).  
> If a breach occurs, logs from Accounting help trace the source and confirm if permissions were excessive.
