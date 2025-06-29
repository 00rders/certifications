### 📘 Notes — Authentication, Authorization, and Accounting (AAA)  
**CompTIA Security+ Objective: 4.1 — Compare authentication, authorization, and accounting concepts**

---

### 🧠 Core Concepts

The **AAA model** is the foundation of secure access control systems.  
It defines the lifecycle of user interaction with resources:

---

#### 🔐 1. Authentication — *Who are you?*
- Verifies the identity of a user or device
- Methods include:
  - **Username + password**
  - **Biometrics** (fingerprint, retina)
  - **Tokens** (hardware or software)
  - **Smart cards**
  - **Multi-factor authentication (MFA)**

##### 📚 MFA Factor Types:
- **Something you know** — password, PIN
- **Something you have** — smart card, phone, hardware token
- **Something you are** — fingerprint, facial recognition
- **Somewhere you are** — geolocation, IP range
- **Something you do** — typing patterns, behavior biometrics

---

#### 🔑 2. Authorization — *What are you allowed to do?*
- Occurs after successful authentication
- Determines access rights based on:
  - **Roles** (RBAC — Role-Based Access Control)
  - **Attributes** (ABAC — Attribute-Based Access Control)
  - **Discretionary or mandatory access models**
- Examples:
  - Accessing shared drives, cloud apps, or admin panels

---

#### 📈 3. Accounting (Auditing) — *What did you do?*
- Tracks and records user activity for:
  - **Auditing**
  - **Compliance**
  - **Threat detection**
- Examples:
  - Session logs, login/logout timestamps, command histories
- Tools: Syslog, SIEMs (Security Information and Event Management)

---

### 🔐 Why It Matters in Security

- AAA provides **full visibility and control** over who is in your environment, what they can do, and what they’ve done
- Critical for:
  - **Forensic investigations**
  - **Insider threat detection**
  - **Regulatory compliance**
  - **Least privilege enforcement**

---

### 💼 Real-World SOC Example

> A contractor logs into the VPN (Authentication), accesses HR records (Authorization), and the session is fully recorded in the SIEM (Accounting).  
> A data exfiltration alert is triggered.  
> The SOC team uses audit logs to trace the access path, confirm file movement, and determine whether proper authorization controls were bypassed.

---

*Logged by 00rders*
