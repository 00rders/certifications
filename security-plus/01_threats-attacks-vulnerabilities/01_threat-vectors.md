# 01_threat_vectors.md  
**Domain:** 1.0 Threats, Attacks, and Vulnerabilities  
**Logged by:** 00rders  
**Date:** 2025-06-30  

---

## 🧠 Core Concepts

- A **threat vector** is the **pathway** or **method** that a threat actor uses to gain unauthorized access to a system, network, or device.
- Threat vectors do not describe the attack itself or the exploited vulnerability — they describe **how the attack reaches the victim**.

---

## 🚪 Common Threat Vectors

| Vector Type | Description |
|-------------|-------------|
| **Phishing** | Social engineering via email or text that tricks users into revealing sensitive info or installing malware |
| **Drive-by Download** | Malware is automatically downloaded when a user visits a compromised website — no interaction required |
| **Credential Reuse** | Using stolen credentials from a previous breach to access new systems |
| **Insider Threat** | An internal actor (malicious or negligent) misuses legitimate access |
| **Watering Hole Attack** | Targeting a trusted third-party site that the victim frequents and compromising it to distribute malware |
| **Supply Chain Attack** | Targeting an organization through a trusted third-party vendor or provider |
| **Shadow IT** | Unauthorized apps, devices, or services deployed without IT approval |
| **Removable Media** | USB drives or external media used to introduce malware or steal data |
| **Network-based** | Attacks delivered through open ports, unpatched services, or exposed APIs |

---

## 📉 Threat Vector vs Vulnerability

| Concept | Definition |
|---------|------------|
| **Threat Vector** | How the attacker gains access (e.g., phishing, drive-by, open port) |
| **Vulnerability** | The flaw or weakness being exploited (e.g., unpatched system, misconfigured ACL) |

---

## 🛡️ Real-World SOC Example

> A phishing email lures a user to click a link that leads to a malicious site.  
> - **Vector**: Email → Link (phishing + drive-by)  
> - **Vulnerability**: Browser plugin zero-day  
> - **Impact**: Initial access → malware dropper installed

Understanding the vector helps analysts classify entry points and improve detection/prevention at the perimeter.

---

## ⚠️ CompTIA Exam Traps

- A **vector** is not a vulnerability — it’s how the attack arrives.
- **Watering hole** attacks compromise a third-party website, not the user directly.
- **Drive-by downloads** can install malware *without user interaction*.
- **Insider threats** include both malicious and accidental actions.
- **Supply chain attacks** often target software vendors, logistics firms, or cloud providers as indirect access points.

---

## ✅ You Are Exam-Ready If You Can:

- Identify and classify different threat vectors  
- Distinguish vectors from vulnerabilities and exploits  
- Recognize how third-party and insider threats are introduced  
- Explain the real-world implications of each vector in a SOC context

---
