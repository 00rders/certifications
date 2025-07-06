### 📘 Notes — Supply Chain Vulnerabilities  
**CompTIA Security+ Objective: 1.2 — Identify common types of vulnerabilities and their characteristics**

---

### 🧠 Core Concepts

#### 🧱 What Are Supply Chain Vulnerabilities?  
Supply chain vulnerabilities are risks introduced when external vendors — whether providing software, hardware, services, or code — become an **unintended attack vector** in your environment.

> 🧷 Third parties expand your trust boundary — and attackers exploit that trust.

---

### 🧬 Key Supply Chain Attack Vectors

| Vector                        | Description |
|------------------------------|-------------|
| **Malicious Code Injection** | Compromise during software builds or updates (e.g., SolarWinds) |
| **Firmware Manipulation**    | Hardware components tampered with before delivery |
| **Library Poisoning**        | Attackers embed malware into commonly used third-party packages |
| **Insider Risk at Vendor**   | A malicious actor inside the vendor organization compromises the supply |
| **Insecure Logistics**       | Devices or components intercepted and modified during transit |

> 🧪 *Even “trusted” vendors can introduce backdoors unintentionally or via compromise.*

---

### 🛠️ Risk-Based Response Strategy

| Scenario                          | Recommended Approach |
|-----------------------------------|-----------------------|
| **Using third-party software**    | Require SBOM, validate code signatures, and restrict network privileges |
| **Receiving vendor hardware**     | Perform integrity checks (e.g., firmware hash verification) |
| **Contracting new suppliers**     | Conduct security due diligence and include SLAs requiring audits |
| **Critical asset dependencies**   | Map supply chain tiers and assess upstream risk exposure |

---

### ⚠️ Why It Matters in Security

- **Nation-state actors** often exploit the supply chain to bypass perimeter defenses  
- SOCs must evaluate **who builds and maintains** every component in their stack  
- **Blind trust** in vendors can lead to **wide-scale compromises**
- Secure updates and dependency visibility (SBOM) are crucial to defense

---

### 💼 Real-World SOC Example

> A finance company deploys a remote access tool purchased from a verified vendor.  
> Weeks later, IRIS logs beaconing traffic from workstations.  
> The root cause is a compromised library embedded by a subcontractor used in the vendor's software build.  
> IRIS triggers a retroactive scan across all vendor packages and flags similar installs for quarantine.

---

### ✅ CompTIA Objective Mapping

- **1.2 — Common Vulnerabilities**
  - Third-party code risk  
  - Vendor firmware compromise  
  - Delivery tampering  
  - Rogue or poisoned packages  
  - Insider sabotage within supply chain  
- **2.6 — Vendor Risk Management**
  - Contractual enforcement, audits, and due diligence  
  - Secure acquisition policies

---

**Logged by 00rders**
