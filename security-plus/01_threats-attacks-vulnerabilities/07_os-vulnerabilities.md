### 📘 Notes — Operating System Vulnerabilities  
**CompTIA Security+ Objective: 1.2 — Identify common types of vulnerabilities and their characteristics**

---

### 🧠 Core Concepts

#### 🖥️ What Are OS Vulnerabilities?
Operating System (OS) vulnerabilities are flaws, bugs, or insecure configurations within the operating system layer that can be exploited by attackers.

OS vulnerabilities matter because:
- Every device relies on an OS — making it a **prime target**
- Operating systems are extremely complex (millions of lines of code)
- A single vulnerability can impact **thousands of systems at scale**

---

### 🛠️ Common Vulnerability Types

#### 🔸 Privilege Escalation
- Exploiting flaws to gain unauthorized admin/root access
- May bypass UAC or exploit kernel-level bugs

#### 🔸 Kernel Vulnerabilities
- Found in the core OS layer
- Can allow complete system compromise if exploited

#### 🔸 Driver/Service Exploits
- Vulnerable or unsigned drivers and services provide a low-level entry point
- Legacy components are often unpatched

#### 🔸 Misconfigurations
- Unnecessary services enabled
- Insecure file/folder permissions
- Default admin credentials left in place

---

### 🔁 Patch Management Best Practices

| Environment         | Patch Strategy                                             |
|---------------------|------------------------------------------------------------|
| **Personal Systems**| Backup important data and update regularly                 |
| **Enterprise Systems**| Test patches in sandboxed environments before wide rollout |
| **Critical Devices**| Use phased deployment and change control processes         |

> 🔐 *Patch testing is essential in enterprise — untested updates can break large-scale deployments.*

---

### ⚠️ Why It Matters in Security

- OS vulnerabilities are a common **initial access vector** for attackers
- Exploits may lead to:
  - **System compromise**
  - **Persistence mechanisms**
  - **Credential dumping**
- Unpatched OS flaws are often targeted in **zero-day** or **known-CVE** campaigns

---

### 💼 Real-World SOC Example

> The SOC receives alerts about lateral movement attempts across multiple workstations.  
> Investigation shows all affected systems are missing a recent **Windows kernel patch** tied to a known CVE.  
> IRIS could automate CVE lookup, verify patch levels via asset management, and recommend a staged update plan.

---

### ✅ CompTIA Objective Mapping

- **1.2 — Common Vulnerabilities**
  - OS and kernel-level flaws
  - Misconfiguration risks
  - Unpatched services and privilege escalation vectors

---

**Logged by 00rders**
