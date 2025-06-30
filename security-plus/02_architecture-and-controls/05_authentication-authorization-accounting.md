### 📘 Notes — Authentication, Authorization, and Accounting (AAA)  
**CompTIA Security+ Objective: 4.1 — Compare authentication, authorization, and accounting concepts**

---

### 🧠 Core Concepts

The **AAA security framework** governs secure access to systems and resources by defining **who** can access, **what** they can do, and **how** those actions are tracked.

---

#### 🔐 1. Authentication — *Who are you?*
- The process of verifying **identity**
- Proves that a user/device is legitimate before access is granted

✅ **Common Methods**:
- Username + password (least secure)
- Smart cards (e.g., CAC/PIV)
- One-time passwords (OTP)
- Software/hardware tokens (e.g., RSA SecurID)
- Biometric scanners (e.g., facial, fingerprint)
- Certificates (e.g., X.509)
- Federated identity systems (e.g., SAML, OAuth, OpenID Connect)

✅ **Multi-Factor Authentication (MFA)**:
> Combines **two or more** types of factors:

- **Something you know** — password, PIN  
- **Something you have** — token, badge, phone  
- **Something you are** — biometric: iris, fingerprint  
- **Somewhere you are** — IP, geolocation  
- **Something you do** — behavior: typing speed, gestures  

---

#### 🔑 2. Authorization — *What can you access?*
- Happens **after** authentication
- Determines the **level of access** a subject has

🧰 **Access Control Models**:
- **RBAC (Role-Based Access Control)** — access by job role  
- **ABAC (Attribute-Based)** — access by attributes (e.g., time of day, department)  
- **MAC (Mandatory)** — enforced labels/classification levels (used in military/government)  
- **DAC (Discretionary)** — owner decides who has access  

Examples:
- User can access shared finance drive but not modify files  
- Admins can restart servers; interns cannot  

---

#### 📈 3. Accounting — *What did you do?*
- The **record-keeping phase**  
- Logs actions and tracks system usage for **auditing, security, and compliance**

📊 **Examples**:
- Login timestamps
- File access records
- VPN session logs
- Command history

🛠️ **Tools Used**:
- **SIEM platforms** (e.g., Splunk, Elastic, QRadar)
- **Syslog** for log forwarding
- **AAA servers** (e.g., RADIUS, TACACS+) also provide accounting features

---

### 🔐 Why It Matters in Security

AAA is **foundational** to modern identity and access management (IAM) systems.  
It provides:
- Enforced **least privilege**
- Auditable access trails
- Detection of suspicious activity
- Data for forensic investigations and compliance

🔁 These controls help enforce:
- **Zero trust**
- **Defense in depth**
- **Risk reduction and segmentation**

---

### 💼 Real-World SOC Example

> A third-party vendor connects remotely via VPN (Authentication).  
> Their access is limited to a software update folder (Authorization).  
> Their session is recorded — login time, IP address, files accessed (Accounting).  
> Later, a log review reveals the vendor accessed restricted finance data.  
> This triggers an incident response, and logs are submitted for regulatory review.

---

### ✅ CompTIA Objective Mapping

- **4.1** — Understand:
  - Authentication types and factors
  - Authorization models (RBAC, ABAC, MAC, DAC)
  - Accounting systems and log correlation

---

*Logged by 00rders*
