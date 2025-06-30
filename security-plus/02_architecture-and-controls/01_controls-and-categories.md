### 📘 Notes — Security Controls and Control Categories  
**CompTIA Security+ Objective: 5.1 — Compare and contrast various types of controls**

---

### 🧠 Core Concepts

Security controls are the mechanisms used to protect systems, data, and people by enforcing the **CIA Triad**:
- **Confidentiality** (protecting data from unauthorized access)
- **Integrity** (ensuring data accuracy and trustworthiness)
- **Availability** (ensuring systems and data are accessible when needed)

Security controls are classified in **two ways**:

---

#### 🔧 Control Types (How a control is implemented)

- **Technical (Logical)**  
  - Implemented using technology or systems  
  - Examples: Firewalls, antivirus software, access control lists, encryption, IDS/IPS

- **Administrative (Managerial)**  
  - Implemented via policies, management decisions, and organizational processes  
  - Examples: Security policies, hiring practices, background checks, user training

- **Operational (Procedural)**  
  - Implemented via day-to-day operations and tasks  
  - Examples: Incident response plans, physical access logs, awareness campaigns, maintenance procedures

---

#### 🎯 Control Categories (What a control is intended to do)

- **Preventive**  
  - Designed to stop an attack or threat from occurring  
  - Examples: Door locks, firewalls, antivirus software, MFA, security awareness training

- **Detective**  
  - Designed to identify and log security events after they occur  
  - Examples: Log monitoring, SIEM alerts, motion sensors, CCTV, tripwires

- **Corrective**  
  - Designed to mitigate harm or restore systems after an incident  
  - Examples: Patching, restoring from backup, changing firewall rules, reimaging systems

- **Deterrent**  
  - Discourages actions through fear of consequences  
  - Examples: Warning signs, security cameras, security guards

- **Compensating**  
  - Alternative controls that provide similar protection when primary controls aren’t feasible  
  - Example: Using CCTV and logs when full access control can’t be implemented

---

### 🔐 Why It Matters in Security

- Proper classification of controls helps security teams:
  - Design layered defense-in-depth strategies
  - Prioritize responses to incidents
  - Evaluate gaps in protection during audits or assessments
- Controls are a core part of every **risk mitigation plan** and compliance framework

---

### 💼 Real-World SOC Example

> A brute-force login attempt succeeds due to weak credentials — a failure of a **Preventive** control (password policy).  
> The attempt is logged by the SIEM and triggers an alert — a **Detective** control.  
> The SOC responds by blocking the IP, resetting credentials, and enabling MFA — combining **Corrective** and **Preventive** measures.  
> A policy update follows to enforce stronger passwords — an **Administrative** and **Preventive** control.

---

*Logged by 00rders*
