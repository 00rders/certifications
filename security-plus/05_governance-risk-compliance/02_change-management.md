### 📘 Notes — Change Management  
**CompTIA Security+ Objective: 4.4 — Explain change management processes and procedures**

---

### 🧠 Core Concepts

**Change Management** is a structured IT process for controlling system, application, or infrastructure changes while minimizing risk and ensuring accountability.

> Every change — even a small patch — has the potential to introduce system downtime, security vulnerabilities, or unexpected disruptions if not properly managed.

Change management enables:
- Controlled updates with reduced impact
- Communication between teams and stakeholders
- Fast recovery when changes go wrong
- Compliance with audit and documentation requirements

---

### 🔁 Key Components of the Change Management Process

| Step | Description |
|------|-------------|
| **1. Change Request (CR)** | Formal ticket submitted by a technical or business stakeholder — outlines what is changing, why, when, and the potential impact |
| **2. Review & Approval** | The **Change Advisory Board (CAB)** or delegated authority assesses risks, timing, and organizational readiness |
| **3. Communication** | Stakeholders are informed about the nature and timing of the change — including users, security teams, and leadership |
| **4. Scheduling** | Changes are implemented during **approved maintenance windows** (often off-peak) to limit disruption |
| **5. Sandbox Testing** | Changes are tested in a **non-production environment** before live deployment to catch issues early |
| **6. Risk Assessment** | Teams must evaluate: <br> - Risk of implementing the change <br> - Risk of *not* implementing (e.g., leaving vulnerabilities unpatched) |
| **7. Backout Plan (Rollback)** | A documented process to revert changes if problems occur — may involve restoring configs, snapshots, or prior versions |
| **8. Implementation** | The change is deployed using version-controlled, tested procedures — tracked by ticket ID or logs |
| **9. Validation & Monitoring** | Confirm that systems are behaving as expected — check logs, alerts, and application behavior |
| **10. Documentation & Auditing** | All changes are logged for future auditing, forensics, and incident investigation |
| **11. Emergency Change Protocol** | Critical fixes (e.g., zero-day patches) may bypass full approval but **must be documented afterward** |

---

### 🔐 Why It Matters in Security

- Misconfigurations caused by uncontrolled changes are a **top cause of security breaches**
- Auditable change logs help:
  - Trace incidents
  - Identify root cause
  - Justify compliance to regulators
- Proper change controls prevent:
  - Firewall misrules
  - Bad patch deployments
  - Unplanned system outages

> 🔑 Well-managed changes = reduced risk, faster recovery, and greater trust in infrastructure integrity

---

### 💼 Real-World SOC Example

> A network engineer modifies a firewall rule to block deprecated outbound DNS traffic.  
> The change is **not reviewed or communicated**.  
> Result: Multiple security tools and remote workers lose connectivity to update services and intelligence feeds.  
> The SOC is flooded with alerts due to **telemetry failure**, wasting analyst time.  
> Since there was no backout plan or change record, recovery is delayed for hours.  
>  
> Had the process followed change management:
> - Stakeholders would have flagged the DNS dependency  
> - The change would have been rejected or modified  
> - Rollback could’ve happened in minutes

---

### ✅ CompTIA Objective Mapping

- **Objective 4.4** — Change management procedures
- Key terms:
  - CAB (Change Advisory Board)
  - CR (Change Request)
  - Risk analysis
  - Maintenance window
  - Backout/rollback plan
  - Sandbox testing
  - Emergency change handling

---

**Logged by 00rders**
