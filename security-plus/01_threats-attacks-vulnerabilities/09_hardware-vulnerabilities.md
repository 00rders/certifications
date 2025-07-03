### 📘 Notes — Hardware Vulnerabilities  
**CompTIA Security+ Objective: 1.2 — Identify common types of vulnerabilities and their characteristics**

---

### 🧠 Core Concepts

#### 🧱 What Are Hardware Vulnerabilities?
Hardware vulnerabilities are flaws or weaknesses in physical devices, firmware, or embedded systems that can be exploited to compromise confidentiality, integrity, or availability.

> ⚠️ Hardware is its **own attack surface** — often overlooked compared to software.

---

### 🧬 Key Hardware Vulnerability Vectors

| Vector                        | Description |
|------------------------------|-------------|
| **Firmware Vulnerabilities** | IoT and embedded devices often use outdated or unpatched firmware |
| **Physical Access**          | Attackers with device access can dump data, clone storage, or install implants |
| **Legacy Hardware**          | Older systems may lack vendor support or security updates |
| **Supply Chain Risk**        | Insecure or compromised hardware/firmware introduced during manufacturing |
| **End-of-Life (EOL)**        | Devices no longer supported by the vendor pose increasing security risks |

> 🔐 *IoT devices often lack robust patching cycles and are built with insecure defaults.*

---

### 🛠️ Risk-Based Response Strategy

| Scenario                    | Recommended Approach |
|-----------------------------|-----------------------|
| **Still in use but unpatchable** | Add layered security (e.g., VLAN segmentation, NAC, physical controls) |
| **Business-critical legacy system** | Conduct risk assessment and justify controls |
| **End-of-Life device**     | Prioritize replacement or isolate it from critical assets |

---

### ⚠️ Why It Matters in Security

- IoT and embedded systems are **highly targeted**, especially in industrial and healthcare environments
- Long patch cycles = persistent exposure
- **Firmware exploitation** can bypass traditional OS-level protections
- SOC teams must **track lifecycle states** (e.g., EOL) and evaluate when legacy systems become a liability

---

### 💼 Real-World SOC Example

> A healthcare clinic uses legacy biometric readers no longer supported by the manufacturer.  
> SOC discovers the firmware allows unauthenticated USB access.  
> IRIS flags the device as EOL, auto-generates a risk memo, and recommends isolating it on its own VLAN until replacement is feasible.

---

### ✅ CompTIA Objective Mapping

- **1.2 — Common Vulnerabilities**
  - Firmware flaws and patch delays  
  - Legacy/EOL device risk  
  - Supply chain threats  
  - Physical attack surface  
  - Risk treatment strategies for unpatchable systems

---

**Logged by 00rders**
