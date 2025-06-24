# 01 — Security Controls & Categories

## 🧩 Scenario  
While watching the first Professor Messer Security+ video, I was introduced to the types of security controls organizations use to protect data, people, and systems. My goal was to distinguish between technical, administrative, and operational control types — and understand how they relate to control categories like preventive, detective, and corrective.

## 🔧 What I Did  
- Watched the full video without pausing.
- Reflected post-video and wrote down what stuck vs. what felt forgettable.
- Identified key control **types**:
  - **Technical** (e.g., firewalls, IDS)
  - **Administrative/Managerial** (e.g., security policies, training)
  - **Operational** (e.g., incident response plans)
- Identified key control **categories**:
  - **Preventive** (e.g., door locks)
  - **Detective** (e.g., logs, CCTV)
  - **Corrective** (e.g., restoring backups)

## 🧠 What I Learned  
- Security controls are implemented to **enforce the CIA triad** (confidentiality, integrity, availability).
- Controls have both a **type** (who/what enforces them) and a **category** (what purpose they serve).
- I retained the meanings of technical/admin/operational controls well — but may need to review their connection to **preventive/detective/corrective** labels.

## 🔒 Why It Matters  
- Understanding these control types is essential in a SOC role where **identifying control failures** is part of incident response.
- Helps me make sense of alerts: e.g., *“This is a failed preventive control — what compensating control caught it?”*

### 💼 Real-World Scenario  
A SOC analyst sees repeated login attempts to an admin portal. Recognizing this is a **failure of a preventive control**, they check logs (a **detective control**) and recommend MFA (an **additional preventive**). Categorizing controls this way speeds up risk triage and communication with management.

---

## 🤖 What Could IRIS Do?
- Automatically tag controls in alerts or reports:
  - e.g., `"[Tag] Technical: Firewall (Preventive)"`
- Help analysts learn from incidents by mapping which controls failed and which succeeded.
- Offer remediation suggestions based on **missing control types**.
- Maintain a control category matrix per system to spot gaps.

---

*Logged by Operator 00rders, supported by IRIS — your SOC copilot.*
