### 📘 Notes — Zero Trust Architecture  
**CompTIA Security+ Objective: 2.1 — Compare security implications of different architecture models**

---

### 🧠 Core Concepts

**Zero Trust Architecture (ZTA)** is a security model that assumes **no implicit trust** — regardless of network location.  
The mantra is: **"Never trust, always verify."**

- Every access request must be:
  - **Explicitly authenticated**
  - **Contextually authorized**
  - **Continuously monitored**
- This applies to:
  - Users, devices, applications, services — internal or external

---

### 🧩 Core ZTA Components

#### 1. **Policy Engine (PE)**
- Makes real-time decisions about access
- Evaluates:
  - User identity and role
  - Device compliance status
  - Location and behavior patterns
  - Time-of-day, risk scoring, and more

#### 2. **Policy Administrator (PA)**
- Enforces decisions from the Policy Engine
- Sends configuration instructions to network or service layer
- Works with systems like firewalls, proxies, microsegmentation gateways

#### 3. **Policy Enforcement Point (PEP)**
- The actual "gatekeeper"
- Grants or denies access to applications, APIs, databases, cloud services, etc.

---

### 🔐 Why It Matters in Security

- Prevents **lateral movement** — attackers who breach one endpoint can’t pivot easily
- Reduces insider threat by applying **least privilege** and context-driven controls
- Ideal for:
  - **Remote workforces**
  - **Cloud-native infrastructure**
  - **BYOD environments**
- Enables **fine-grained control** and rapid detection of abnormal access behavior

---

### 🧠 Additional ZTA Benefits

- Enforces **microsegmentation** — breaking networks into isolated segments
- Supports **continuous trust evaluation**, not just at login
- Facilitates compliance (e.g., PCI, HIPAA) through better access accountability

---

### 💼 Real-World SOC Example

> A remote contractor logs in from a personal laptop.  
> The **Policy Engine** sees:
> - Device is not encrypted  
> - Login originates from a high-risk country  
> - Time-of-day is outside normal window  
> The **PA** denies access via the **PEP** and triggers a security alert.  
> The SOC team uses this to investigate possible account misuse or VPN compromise.

---

*Logged by 00rders*
