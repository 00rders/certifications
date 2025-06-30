### 📘 Notes — Technical Change Management  
**CompTIA Security+ Objective: 4.4 — Explain change management processes and procedures**

---

### 🧠 Core Concepts

**Technical change management** governs how IT and infrastructure changes are **planned, approved, implemented, and documented** — with the goal of minimizing risk and downtime.

> 📌 *Change management is not just about documentation — it’s about maintaining **operational stability, security, and accountability** across the environment.*

---

### 🛠️ Types of Technical Changes

- **Firewall rule updates** — allowlists/denylists, port changes  
- **Patch management** — applying security updates to OS/software  
- **Configuration changes** — DNS, routing, permissions  
- **Infrastructure shifts** — new servers, storage, network segments  
- **Service restarts or rollouts** — applying changes, updating applications

---

### 🔁 Core Change Control Components

#### 1. **Scope Definition**
- Clarifies what is allowed to change and **what’s off-limits**
- Includes:
  - Systems affected
  - Time window
  - Rollback criteria
- Scope changes require re-approval or post-change documentation

#### 2. **Downtime Planning**
- Downtime = **planned unavailability** for updates
- Must be:
  - Communicated in advance
  - Scheduled during **low-impact windows**
  - Paired with rollback plans or redundancies
- **Post-change validation** is required to confirm uptime

#### 3. **Legacy Systems**
- Old or fragile systems that:
  - Lack documentation
  - Can’t be patched easily
  - May break under standard change procedures
- Often require:
  - Custom handling
  - Senior engineer involvement
  - "Do Not Touch" designation unless risk-justified

#### 4. **Dependency Mapping**
- All systems have **interdependencies**
  - Example: A DNS change might affect email, VPN, threat feeds
- Poor mapping causes **cascading failures**
- SOCs and engineers must:
  - Identify upstream/downstream dependencies
  - Validate integrations post-change

#### 5. **Documentation and Version Control**
- All changes must be:
  - **Logged** with change description, timestamps, and personnel
  - **Versioned** — config files, rulesets, scripts
  - **Auditable** for forensic and compliance needs
- Tools: Git, Ansible, CMDBs, ticketing systems (Jira, ServiceNow)

---

### 🔐 Why It Matters in Security

- Improper or undocumented changes can:
  - **Break critical services**
  - Open **attack surfaces**
  - Obscure the **root cause** of incidents
- SOC teams depend on:
  - **Change logs** for incident correlation
  - **Version rollbacks** to restore service
  - **Approval history** for accountability

> 💡 Misconfigurations are a top cause of security breaches.

---

### 💼 Real-World SOC Example

> A firewall rule change disables outbound connections to a deprecated API.  
> Minutes later, the SOC SIEM dashboard loses its connection to a threat intelligence feed.  
> Engineers consult the **change log**, identify the unintended dependency, and roll back the config.  
> Because the change was versioned and downtime planned, **service is restored in under 10 minutes** without escalated incident status.

---

### ✅ CompTIA Objective Mapping

- **4.4** — Change management in secure environments
  - Planning, approval, rollback, and impact analysis
  - Documentation and audit trails
  - Dependency awareness and legacy system precautions

---

**Logged by 00rders**
