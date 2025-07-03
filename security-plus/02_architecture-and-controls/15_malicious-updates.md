# 🧠 Malicious Updates (SY0-701 – Domain 2.3)

## 🔍 Core Concept
**Malicious updates** occur when software updates are modified or spoofed to include malicious code. These attacks can exploit trust in vendors or software mechanisms and are difficult to detect once executed.

## 🦠 How Attackers Leverage Updates
- **Trojanized installers** may appear legitimate but carry malware.
- **Compromised update servers** can deliver signed but malicious binaries.
- **Third-party download sites** may host fake "official" update packages.
- **Man-in-the-middle attacks** on insecure update channels can swap binaries mid-download.

## 🛡️ Defense Strategies

| Method                             | Purpose |
|-----------------------------------|---------|
| **Digital Signatures**            | Verifies authenticity and integrity of the update |
| **Hash Comparison (e.g., SHA256)**| Ensures downloaded file wasn’t tampered with |
| **Trusted Vendor Sources**        | Updates should only come from official or trusted repositories |
| **Secure Channels (HTTPS)**       | Prevents interception and injection during transit |
| **Built-in Update Tools**         | Native update mechanisms are generally safer but not immune to exploitation |

## ❗ Important Reminder
Even **official software updaters** can be compromised (e.g., SolarWinds supply chain breach), so layered verification is key.

## 🧑‍💻 SOC Analyst Real-World Example
> The SOC team receives alerts from EDR showing unusual command-line activity during a scheduled update.  
> Investigation reveals the update package was delivered via a spoofed domain impersonating a legitimate vendor.  
> IRIS could assist by flagging the hash mismatch, auto-comparing the binary’s digital signature, and alerting on abnormal update behavior patterns.

---

✅ **Logged by 00rders**  
_Source: Professor Messer – “Malicious Updates” (SY0-701, Domain 2.3)_
