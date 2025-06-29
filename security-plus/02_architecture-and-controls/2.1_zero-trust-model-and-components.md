### 📘 Notes — Zero Trust Architecture  
**CompTIA Security+ Objective: 2.1 — Compare security implications of different architecture models**

---

### 🧠 Core Concepts

- **Zero Trust** means: *“Never trust, always verify.”*
  - No device or user is inherently trusted — even if already inside the network perimeter.
  - Every access request is evaluated in real-time based on **identity**, **context**, and **policy**.

- **Core Components** of a Zero Trust architecture:
  - **Policy Engine (PE)**:  
    - Makes access decisions based on rules, identity, location, and device posture.
  - **Policy Administrator (PA)**:  
    - Pushes decisions and configurations to enforcement points.
  - **Policy Enforcement Point (PEP)**:  
    - Grants or denies access to resources (e.g., apps, files, services).

- These components work together to:
  - Evaluate each request independently
  - Reduce risk from lateral movement
  - Provide granular access control in real time

---

### 🔐 Why It Matters in Security

- Zero Trust is critical for modern **remote work**, **cloud environments**, and **hybrid infrastructure**.
- As an analyst, understanding how policy-based access control works allows:
  - Better log analysis
  - Incident response when access is denied or abused
  - Debugging trust and access failures in enterprise environments

---

### 💼 Real-World SOC Example

> A remote employee attempts to access a secure Git repository.  
> The **Policy Engine** evaluates:
> - Device compliance  
> - User identity and group  
> - Geolocation and time of day  
> The **Policy Administrator** sends access instructions to the **PEP**, which denies access because the user’s device hasn’t passed a recent compliance check.

---

### ✅ CompTIA Objective Mapping

- **Domain**: 2.1 — Security implications of architecture models  
- **Relevance**: Zero Trust replaces traditional perimeter defenses with dynamic policy-based enforcement for every access attempt.
