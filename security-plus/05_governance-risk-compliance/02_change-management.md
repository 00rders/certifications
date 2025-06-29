### 📘 Notes — Change Management  
**CompTIA Security+ Objective: 4.4 — Explain change management processes and procedures**

---

### 🧠 Core Concepts

**Change Management** is the structured process for planning, approving, implementing, and reviewing changes to IT systems, configurations, or infrastructure.

It exists to:
- Minimize risk to systems and services
- Ensure accountability and traceability
- Prevent downtime and configuration errors
- Provide controlled recovery in case of failure

Every change — even a small patch — can have **widespread impact** if done without planning.

---

### 🔁 Key Components of the Change Management Process

1. **Change Request (CR)**
   - Formal submission describing:
     - What is changing
     - Why it's needed
     - Affected systems/users
     - Timing (e.g., maintenance window)
     - Risk and impact levels
   - May be submitted by engineers, dev teams, or system owners

2. **Review and Approval**
   - Reviewed by the **Change Advisory Board (CAB)** or delegated approvers
   - CAB considers:
     - Risk level
     - Business impact
     - Stakeholder readiness
     - Resource availability
   - Not all changes go to CAB (low-risk or pre-approved changes may follow streamlined paths)

3. **Communication**
   - Stakeholders must be notified before rollout
   - Includes users, management, and technical staff
   - Communication should define:
     - What’s changing
     - When
     - What to expect

4. **Scheduling (Maintenance Windows)**
   - Changes should happen during low-risk periods (e.g., after hours, weekends)
   - Critical for reducing business disruption

5. **Testing in Sandboxes**
   - Simulate the change in an isolated, non-production environment
   - Helps detect breakage or unexpected behavior before full deployment

6. **Risk Assessment**
   - Analyze both the **risk of the change** and the **risk of not changing**
   - Example: Delaying a patch could expose the system to known vulnerabilities

7. **Backout Plan (Rollback Plan)**
   - A documented way to undo the change if something fails
   - May involve:
     - Restoring from backups
     - Reverting config files
     - Re-deploying previous versions

8. **Implementation**
   - Execute the change during the approved window
   - Use version control and scripts when possible to ensure consistency

9. **Validation and Monitoring**
   - Post-change checks:
     - Did the change apply successfully?
     - Did it break anything?
     - Are logs and services behaving normally?

10. **Documentation and Audit Logging**
    - All changes must be recorded in a change log or ticketing system
    - Enables:
      - Incident investigation
      - Compliance audits
      - Historical review of system state

11. **Emergency Change Handling**
    - For urgent security patches or system outages
    - May bypass full approval **but must still be documented retroactively**

---

### 🔐 Why It Matters in Security

- Poorly controlled changes are a top cause of system outages and security misconfigurations
- Change logs create an **audit trail** that can help trace breaches or suspicious behavior
- Good change management allows **risk-aware decision-making** without slowing down innovation

---

### 💼 Real-World SOC Example

> An engineer deploys a new firewall rule without going through change management.  
> The rule blocks outbound DNS for several departments, disrupting operations.  
> No backout plan was defined, and the engineer is unavailable.  
> After 2 hours of downtime, the SOC team restores service using a week-old config — but loses valuable logs and introduces new vulnerabilities.

> Had the change gone through proper channels:
> - It would’ve been tested in a sandbox  
> - Stakeholders would've been warned  
> - A backout plan would’ve restored services in minutes  
> - The change itself may have been rejected or delayed

---

### ✅ CompTIA Objective Mapping

- **Domain**: 4.4 — Operations and Incident Response  
- **Keywords**: CAB, CR, rollback, audit log, sandbox, risk analysis, stakeholder communication, emergency change

