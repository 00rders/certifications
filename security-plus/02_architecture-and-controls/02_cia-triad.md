# 02 — CIA Triad: Confidentiality, Integrity, Availability

## 🧩 Scenario  
This module focuses on one of the most foundational security concepts: the **CIA Triad** — Confidentiality, Integrity, and Availability. The challenge wasn’t understanding what each term meant, but rather remembering **which security mechanisms map to which category**, especially under pressure.

## 🔧 What I Did  
- Watched the second Professor Messer video straight through.
- Took time after to reflect on which examples clicked and which felt fuzzy.
- Noted that **individual terms were easy to understand**, but **mapping controls (like fault tolerance) to the right triad pillar** felt more forgettable.

## 🧠 What I Learned  
- **Confidentiality**: Ensuring that data is only seen by those authorized.
  - Controls: Encryption, access control, classification, DLP
- **Integrity**: Ensuring data is accurate and unmodified.
  - Controls: Hashing, file checksums, digital signatures
- **Availability**: Ensuring systems and data are accessible when needed.
  - Controls: Redundancy, fault tolerance, backups, RAID

Biggest challenge: Remembering which specific tools or mechanisms fall under which CIA category — especially under exam pressure.

## 🔒 Why It Matters  
- The CIA Triad is the **foundation of all security frameworks**. Every control, policy, or response maps back to one or more of these three.
- In a SOC environment, being able to **quickly categorize what’s at risk (C, I, or A)** helps prioritize responses.

### 💼 Real-World Scenario  
If a company’s RAID array fails and systems go offline, it’s not just a hardware issue — it’s an **availability failure**. A SOC analyst would immediately check backups, uptime SLAs, and continuity plans. Misidentifying it as a confidentiality issue would waste critical response time.

---

## 🤖 What Could IRIS Do?
- Classify incidents based on CIA impact:
  - e.g., *"This alert affects Integrity due to possible data tampering."*
- Suggest relevant remediation based on the triad pillar:
  - If **availability** fails: suggest failover, load balancing, or HA clusters.
- Train new analysts by **quizzing them**: “Which CIA pillar does this alert threaten?”

---

*Logged by Operator 00rders, supported by IRIS — your SOC copilot.*
