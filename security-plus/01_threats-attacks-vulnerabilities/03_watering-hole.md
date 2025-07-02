# 03_watering-hole.md  
**Domain:** 1.0 Threats, Attacks, and Vulnerabilities  
**Logged by:** 00rders  
**Date:** 2025-07-01  

---

## 🧠 Core Concepts – Watering Hole Attacks

- A **watering hole attack** targets **a location or resource** that a specific group of users (the real targets) are likely to visit.
- Rather than attacking the user directly, the attacker **compromises a third-party website or service** commonly used by the target — often one with **lower security defenses**.
- The goal is to **infect the victim’s machine** when they visit the trusted site, which may later enable:
  - **Credential harvesting**
  - **Malware installation**
  - **Backdoor access**
  - **Lateral movement** into the user's organization

---

## 🧪 Example Scenarios

| Watering Hole     | Target Victim                           |
|-------------------|------------------------------------------|
| Local coffee shop Wi-Fi | Remote employee logging in from public network |
| Niche industry blog | Company engineers who frequent the site |
| Third-party vendor portal | Supply chain partner’s employees    |
| Compromised update server | Internal systems installing “trusted” software |

---

## 🛡️ Why It’s Dangerous

- Leverages **trust** in third-party services
- Harder to detect — traffic often appears legitimate
- Bypasses perimeter defenses by letting the **user bring the attack in**

---

## 🛡️ Defense Strategies

| Control                      | Description                                                   |
|------------------------------|---------------------------------------------------------------|
| **Layered security model**   | Combine host-based, network, and application security         |
| **Web filtering / proxies**  | Block access to known malicious or suspicious sites           |
| **Endpoint protection**      | Detects anomalies even on trusted domains                     |
| **Threat intel feeds**       | Stay aware of compromised third-party services                |
| **User behavior analytics (UBA)** | Detects unusual activity or lateral movement               |
| **User education**           | Encourage caution even on trusted sites and public Wi-Fi      |

---

## 🧪 Real-World SOC Example

> A finance employee visits a com
