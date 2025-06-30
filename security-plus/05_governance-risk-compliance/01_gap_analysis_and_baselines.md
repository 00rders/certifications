### 📘 Notes — Gap Analysis and Security Baselines  
**CompTIA Security+ Objective: 5.4 — Summarize risk management processes and concepts**

---

### 🧠 Core Concepts

#### 🔎 Gap Analysis
- A formal method of identifying **discrepancies** between an organization’s **current security posture** and its **desired or required security state**
- Common use cases:
  - Internal audits
  - Compliance checks (HIPAA, PCI-DSS, GDPR)
  - Preparation for third-party assessments or certifications

> Example: Comparing current firewall rules to CIS benchmarks to reveal missing or misconfigured settings

---

#### 🧱 Security Baseline
- A defined **minimum level of security configuration** for systems, networks, and applications
- Includes:
  - Patch levels
  - Port/service configurations
  - Access controls
  - Encryption/enforcement policies
- Sources:
  - **Industry standards** (CIS, NIST 800-53, ISO/IEC 27001)
  - **Organizational policy**
  - **Legal/regulatory mandates**

---

### 🔁 Baseline & Gap Analysis Lifecycle

1. **Define the baseline** — using internal policy + frameworks  
2. **Assess current posture** — via gap analysis  
3. **Document gaps** — include severity, business risk, and impacted assets  
4. **Prioritize remediation** — based on risk appetite and compliance deadlines  
5. **Update baseline** — regularly to match evolving systems, threats, and standards

---

### 🔐 Why It Matters in Security

- Enables **proactive risk identification** before exploitation occurs
- Promotes **standardized security configurations** across all systems
- Supports:
  - **Change control and audit readiness**
  - **Incident prevention** (e.g., reducing attack surface)
  - **Budget justification** for tools, staffing, and controls

> ⚠️ A weak baseline or ignored gap analysis can lead to:
> - Misconfigurations
> - Compliance failures
> - Easier exploitation by attackers

---

### 💼 Real-World SOC Example

> A quarterly internal gap analysis shows:
> - Linux servers allow SSH root login  
> - TLS 1.0 still enabled  
> - Systems missing recent kernel patches  
>  
> The SOC tags these as high-priority misconfigurations.  
> The incident response team escalates remediation through the change management process.  
> The findings are later used to **update onboarding templates and security checklists**, preventing recurrence across new infrastructure.

---

### ✅ CompTIA Objective Mapping

- **5.4** — Risk management concepts:
  - Gap analysis
  - Security baselines
  - Threat modeling, risk appetite, and continuous improvement

---

**Logged by 00rders**
