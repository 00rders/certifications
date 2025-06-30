### 📘 Notes — Zero Trust Architecture (ZTA)  
**CompTIA Security+ Objective: 2.1 — Compare security implications of different architecture models**

---

### 🧠 Core Concepts

**Zero Trust Architecture (ZTA)** is a modern security framework based on the principle:  
> 🛑 **Never trust, always verify — every user, every device, every time.**

ZTA **assumes breach by default**, and requires:
- **Explicit identity verification**
- **Granular access controls**
- **Continuous monitoring of trust**

No device or user — internal or external — is automatically trusted. Trust is earned *per request*, based on dynamic risk evaluation.

---

### 🧩 Core ZTA Components

#### ✅ 1. **Policy Engine (PE)**
- Brain of ZTA — makes **real-time access decisions**
- Considers:
  - **Identity and authentication strength**
  - **Device health/compliance**
  - **Geo-location/IP**
  - **Behavioral patterns**
  - **Time-of-day access rules**
  - **Threat intel (e.g., IP reputation)**

#### ✅ 2. **Policy Administrator (PA)**
- Acts on decisions made by PE  
- Pushes enforcement configurations to systems (e.g., firewall, proxy, IDP)
- Coordinates with **IAM**, **NAC**, and **cloud brokers**

#### ✅ 3. **Policy Enforcement Point (PEP)**
- The **access gateway** — enforces allow/block actions  
- Can be:
  - **Firewalls**
  - **Proxies**
  - **Endpoint agents**
  - **Cloud access brokers (CASB)**
  - **Microsegmentation gateways**

---

### 🔐 Security Advantages of ZTA

- Blocks **lateral movement** by isolating systems
- Applies **least privilege** dynamically (context-aware access)
- Eliminates **trusted network zones** (even internal LANs)
- Enables **risk-adaptive access** — decisions based on current threat posture

---

### 🚀 Where ZTA Shines

- **Remote work** and BYOD policies
- **Cloud-native infrastructure** (multi-cloud, hybrid)
- **Privileged access control**
- Organizations seeking **compliance** with:
  - PCI-DSS
  - HIPAA
  - NIST 800-207 (official ZTA framework)
  - CMMC

---

### 💡 Additional Benefits

- Enforces **microsegmentation** — isolates assets and apps  
- Enables **continuous trust evaluation** — not just at login  
- Simplifies auditing and improves **incident attribution**

---

### 💼 Real-World SOC Example

> A remote developer connects from a personal laptop.  
> The **Policy Engine** checks:
> - IP reputation: blacklisted country  
> - Device posture: no encryption or antivirus  
> - Time of day: abnormal for that user  
> Result:
> - **Policy Administrator** pushes a deny rule  
> - **PEP** blocks access and logs event  
> - SOC receives alert and investigates potential credential abuse  

---

### ✅ CompTIA Objective Mapping

- **2.1** — Know how ZTA differs from traditional perimeter-based security
- Understand roles of:
  - PE, PA, PEP
  - Microsegmentation
  - Continuous evaluation

---

*Logged by 00rders*
