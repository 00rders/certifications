### 📘 Notes — Physical Security Controls  
**CompTIA Security+ Objective: 3.4 — Given a scenario, implement physical security controls**

---

### 🧠 Core Concepts

**Physical security** protects systems, data, and people from **real-world, physical threats**, including:
- Theft, break-ins, and tampering
- Natural disasters (fire, flood, power loss)
- Insider sabotage or social engineering (tailgating, badge cloning)

> 📌 *Unlike logical controls (firewalls, passwords), physical controls use **tangible mechanisms** like doors, locks, cameras, and barriers.*

---

### 🧱 Categories of Physical Security Controls

#### 🔹 1. **Deterrent Controls**
- Designed to discourage intrusion
- Examples:
  - **Warning signs**
  - **Security lighting**
  - **Visible cameras**
  - **Security guards**

#### 🔹 2. **Preventive Controls**
- Aim to stop unauthorized access
- Examples:
  - **Fencing**, **bollards**, **locked doors**
  - **Mantraps**, **turnstiles**
  - **Badge readers**, **biometrics**
  - **Faraday cages** (signal blocking)

#### 🔹 3. **Detective Controls**
- Identify or alert to suspicious activity
- Examples:
  - **CCTV**, **motion sensors**, **glass break sensors**
  - **Alarms**, **access logs**
  - **Security patrol check-ins**

#### 🔹 4. **Corrective & Recovery Controls**
- Minimize damage or restore operations
- Examples:
  - **Fire suppression** (Halon, clean agent)
  - **Water leak sensors**
  - **HVAC systems**
  - **Uninterruptible Power Supplies (UPS)**
  - **Generators**, **backup systems**

---

### 🛑 Social Engineering & Physical Risk

- **Tailgating** — unauthorized person follows an employee inside
- **Shoulder surfing** — visually spying on credentials
- **Dumpster diving** — recovering sensitive data from discarded materials
- **Impersonation** — acting as maintenance, delivery, etc.

> 🎯 *Prevention depends on employee training, badge policies, and multi-layered access enforcement.*

---

### 🔐 Why It Matters in Security

- If an attacker gains **physical access**, they may:
  - Steal or destroy assets
  - Install keyloggers or rogue hardware (USB drops, Pi attacks)
  - Bypass encryption (e.g., cold boot attack)
- Physical controls **support** digital controls:
  - Server room locks support firewall protections
  - CCTV validates SIEM alerts or unusual login patterns
- Required for compliance: **PCI-DSS**, **HIPAA**, **FISMA**

---

### 💼 Real-World SOC Example

> During a routine SOC check, a spike in outbound traffic is flagged.  
> Investigation reveals a **rogue Raspberry Pi** connected to a switch.  
> Video footage confirms the device was dropped by an unknown individual during a **shift change tailgating event**.  
> Thanks to **mantrap logs**, **CCTV**, and **badge audit trails**, the intruder is identified and data exfiltration stopped before damage escalates.

---

### ✅ CompTIA Objective Mapping

- **3.4** — Implementing physical controls
  - Fences, badge systems, surveillance
  - Mantraps, HVAC, lighting, fire suppression
  - Insider threat mitigation and detection

---

**Logged by 00rders**
