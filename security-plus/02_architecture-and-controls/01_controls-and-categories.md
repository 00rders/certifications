### 📘 Notes — Security Controls and Control Categories  
**CompTIA Security+ Objective: 5.1 — Compare and contrast various types of controls**

---

### 🧠 Core Concepts

Security controls are mechanisms used to enforce the **CIA triad** (Confidentiality, Integrity, Availability).  
Each control has two key attributes:

---

#### 🔧 Control Types

- **Technical (Logical)**  
  - Enforced by technology and systems  
  - Examples: Firewalls, intrusion detection systems, encryption

- **Administrative (Managerial)**  
  - Enforced through policies, procedures, and training  
  - Examples: Security policies, background checks, awareness training

- **Operational (Procedural)**  
  - Enforced through daily routines and processes  
  - Examples: Incident response plans, physical security patrols

---

#### 🎯 Control Categories

- **Preventive** — Stops an attack from occurring  
  - Examples: Access control lists, door locks, security awareness training

- **Detective** — Identifies and logs an attack after it happens  
  - Examples: SIEM alerts, motion sensors, CCTV

- **Corrective** — Responds to and mitigates damage after an incident  
  - Examples: Patch deployment, backup restores, firewall rule updates

---

### 🔐 Why It Matters in Security

- Controls are the foundation of every security architecture
- Analysts must understand types and categories to:
  - Interpret alerts properly
  - Spot weaknesses or gaps in defenses
  - Communicate control failures to technical and non-technical teams

---

### 💼 Real-World SOC Example

> A brute-force login attempt bypasses weak credentials (failed **Preventive** control).  
> The login is logged and triggers an alert (**Detective** control).  
> The SOC team blocks the IP, resets credentials, and enables MFA (**Corrective** and **Preventive** controls combined).
