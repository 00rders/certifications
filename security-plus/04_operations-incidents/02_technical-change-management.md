### 📘 Notes — Technical Change Management  
**CompTIA Security+ Objective: 4.4 — Explain change management processes and procedures**

---

### 🧠 Core Concepts

**Technical change management** focuses on how changes are implemented at the **infrastructure level**, ensuring operational stability, security, and accountability.

While **administrative roles** decide *what* should change and *why*, **technical teams** are responsible for *how* the change is safely implemented.

---

### 🛠️ Common Technical Changes

- Firewall rule updates (e.g., allow/deny lists)  
- Server reconfigurations  
- Software version upgrades and patching  
- Device or service restarts  
- Infrastructure migrations (databases, networks)

---

### 🔁 Change Control Concepts

#### 1. **Scope of Change**
- Defines **exactly what is allowed** to change during the approved window
- May include:
  - Targeted systems
  - Time limits
  - Approved rollback plans
- The scope can be **adjusted mid-window** *if* needed to meet business outcomes, but must be documented

#### 2. **Downtime Planning**
- **Downtime** = when services will be unavailable during changes
- Best scheduled during **off-peak hours**
- Downtime should be **minimized** whenever possible
- Often requires **restarting services/systems** to apply updates or changes

#### 3. **Legacy Systems**
- Older systems that:
  - Are poorly documented
  - Run critical but fragile services
  - Have high risk if modified
- Typically marked as **“Do Not Touch”** unless absolutely necessary

#### 4. **Dependencies**
- Systems often rely on other services, configurations, or network paths
- Change in one area can break another
- Dependency mapping is crucial before implementing changes

#### 5. **Documentation + Version Control**
- All changes must be:
  - **Documented in detail** (what changed, when, by whom)
  - **Versioned** (especially config files and software deployments)
- This enables:
  - **Rollback** if needed
  - **Audit trails** for future analysis
  - **Clear communication** between teams and stakeholders

---

### 🔐 Why It Matters in Security

- Poorly managed technical changes are a **top cause of misconfigurations, outages, and security gaps**
- SOC analysts rely on version logs and change documentation to:
  - Trace unexpected behavior
  - Investigate incidents
  - Restore affected services

---

### 💼 Real-World SOC Example

> During a scheduled firewall change window, a deny rule is added to restrict outbound access to a deprecated API.  
> The scope included restarting the firewall service and applying config changes.  
> However, the change **unexpectedly blocked** access to a third-party threat intelligence feed.  
> Thanks to detailed documentation and versioned configs, the team quickly identifies the dependency and rolls back the change — restoring service with minimal downtime.

---

*Logged by 00rders*
