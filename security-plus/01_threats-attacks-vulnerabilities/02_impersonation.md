# 02_impersonation.md  
**Domain:** 1.0 Threats, Attacks, and Vulnerabilities  
**Logged by:** 00rders  
**Date:** 2025-07-01  

---

## 🧠 Core Concepts – Impersonation

- **Impersonation** is a **social engineering attack** where an attacker pretends to be a trusted individual (e.g., manager, IT support, law enforcement) to manipulate the victim.
- The attacker typically aims to:
  - Trick the user into **disclosing sensitive information**
  - Get them to **perform unauthorized actions** (e.g., disabling antivirus, resetting credentials)
- It **exploits authority, urgency, and human trust**
- Often used in conjunction with:
  - **Phishing** (email)
  - **Vishing** (phone)
  - **In-person** deception
- May involve or lead to **identity fraud**, where the attacker uses stolen PII to open accounts or gain deeper access.

---

## 🕵️ Impersonation Mechanics

| Tactic Used       | Explanation                                               |
|-------------------|-----------------------------------------------------------|
| Authority Abuse   | Claims to be a higher-up (e.g., boss, CEO, police)        |
| Urgency           | Pushes the target to act quickly, skipping verification   |
| Familiarity       | Mentions names or internal lingo to build credibility     |
| Pretexting        | Uses a false scenario to justify the request              |
| Tailgating        | May follow real employees into secure areas physically    |

---

## 🔐 Identity Fraud – As a Related Technique

- Involves **using someone’s stolen PII** to impersonate them at a deeper level
- Common fraud examples:
  - Opening **bank accounts**
  - Applying for **credit cards**
  - Accessing **HR portals, healthcare data, VPNs**

---

## 🛡️ Defense Strategies

| Defense                  | Explanation                                                     |
|--------------------------|-----------------------------------------------------------------|
| **Security awareness training** | Teach staff to verify identities, especially under pressure     |
| **Verification protocols**       | Use callback procedures, badge checks, or secondary contact methods |
| **Multi-factor authentication** | Prevents unauthorized account access even with stolen credentials |
| **Limit data exposure**         | Don’t share internal structures or personal data publicly       |
| **Incident reporting procedures** | Encourage fast reporting of suspicious requests or behavior    |

---

## 🧪 Real-World SOC Example

> An attacker calls the helpdesk pretending to be the company’s CTO, demanding an urgent password reset for their account due to a “VPN outage.”  
> The helpdesk technician bypasses normal procedures under pressure. The attacker logs in using the new credentials and begins lateral movement inside the environment.  
> SOC analysts detect an unfamiliar IP accessing internal resources. Investigation reveals impersonation as the initial access vector.

---

## ⚠️ CompTIA Exam Traps to Avoid

- Impersonation ≠ identity fraud — **Impersonation is a tactic**, identity fraud is an outcome/tool  
- Urgency and familiarity are **key indicators** of impersonation  
- Impersonation can happen in **any medium**: phone, email, in-person  
- Awareness training is **more important than just technical controls**  
- MFA mitigates **credential-based abuse**, but not **in-person tailgating**

---

## ✅ You Are Exam-Ready If You Can:

- Identify how impersonation works in a phone, email, or in-person scenario  
- Describe how attackers exploit trust and urgency to bypass verification  
- Explain the role of awareness training and verification in prevention  
- Distinguish impersonation from identity theft and other social engineering  
- Recall appropriate technical and procedural defenses (MFA, callback procedures)

---

### ✅ Final Mastery: Confirmed via full video reflection  
**Weak spot resolved**: Impersonation is a tactic, not identity theft itself  
**Score**: Self-assessed retention strong  
