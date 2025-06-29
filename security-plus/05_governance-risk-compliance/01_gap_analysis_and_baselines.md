### 📘 Notes — Gap Analysis and Security Baselines  
**CompTIA Security+ Objective: 5.4 — Summarize risk management processes and concepts**

---

### 🧠 Core Concepts

#### 🔎 Gap Analysis
- A structured comparison between an organization's **current security posture** and a **desired or required state**.
- Used to identify:
  - **Missing controls**
  - **Insufficient protections**
  - **Outdated configurations**
- Often conducted as part of:
  - Internal security audits
  - Third-party assessments
  - Compliance readiness checks

#### 🧱 Security Baseline
- A **minimum required configuration or control set** used to maintain a secure system state.
- Ensures consistency across:
  - Systems
  - Devices
  - Accounts
  - Networks
- Typically derived from:
  - **Industry standards** (e.g., NIST 800-53, CIS Benchmarks)
  - **Internal policy requirements**
  - **Legal or regulatory obligations** (e.g., HIPAA, PCI-DSS)

#### 🔁 Baselines + Gap Analysis Workflow
1. **Establish the baseline** (desired secure state)
2. **Perform gap analysis** to assess current posture
3. **Document deviations** and quantify risk
4. **Prioritize remediation** based on business impact and compliance urgency
5. **Update baseline** as systems or standards evolve

---

### 🔐 Why It Matters in Security

- Helps organizations ensure systems align with **known-good security practices**
- Identifies misconfigurations, missing patches, legacy services, and policy violations
- Strengthens the security lifecycle by:
  - Providing a measurement point for risk
  - Supporting **continuous improvement**
  - Enabling **justifiable investments** in remediation
- Forms the foundation of **risk assessments** and ongoing **governance programs**

---

### 💼 Real-World SOC Example

> Your organization mandates the CIS Level 1 benchmark for Linux servers.  
> During a gap analysis, it’s discovered that:
> - Several servers have SSH root login enabled  
> - Older TLS protocols are still active  
> - Patch management is inconsistent  
> The SOC team tags these gaps as critical, escalates the fix via change management, and uses the findings to revise onboarding procedures for new assets.

---

*Logged by 00rders*
