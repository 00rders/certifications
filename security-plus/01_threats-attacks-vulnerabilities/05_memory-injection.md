# 05_memory-injection.md  
**Domain:** 1.0 Threats, Attacks, and Vulnerabilities  
**Logged by:** 00rders  
**Date:** 2025-07-01  

---

## 🧠 Core Concepts – Memory Injection

- For malware to **execute**, it must reside in **system memory**.
- Malware typically either:
  - Creates a **new malicious process**, or  
  - Injects itself into an **existing legitimate process**.
- **Memory injection** allows malware to run **within a trusted process**, inheriting:
  - The same **permissions** (read, write, execute)
  - The same **execution context** (e.g., signed binary, trusted app)
- This helps malware **evade antivirus and behavior-based detection**, especially if security tools only monitor standalone or unfamiliar processes.

---

## 💉 Common Memory Injection Techniques

| Technique             | Description                                                        |
|------------------------|--------------------------------------------------------------------|
| **DLL Injection**       | Injects a malicious DLL into another process’s memory space       |
| **Reflective Injection**| Loads code directly into memory without touching the disk         |
| **Process Hollowing**   | Suspends a legitimate process, replaces its code, resumes it      |
| **Code Cavities**       | Writes malicious code into unused portions of a process’s memory  |

---

## ⚠️ Why It’s Dangerous

- Runs under the guise of **trusted software**  
- Inherits **elevated permissions** without triggering alarms  
- Often used by **advanced persistent threats (APTs)**  
- Difficult to detect with **signature-based tools**

---

## 🛡️ Defense Strategies

| Control / Tool              | Purpose                                                      |
|-----------------------------|--------------------------------------------------------------|
| **Behavior-based detection**| Identifies unusual process behaviors or memory usage         |
| **EDR solutions**           | Endpoint Detection and Response tools log deep process activity |
| **Memory scanners**         | Search active memory for known payload patterns              |
| **Application control**     | Whitelist trusted apps and restrict code execution           |
| **Patch management**        | Reduces exploitability of injection entry points             |

---

## 🧪 Real-World SOC Example

> A helpdesk user reports lag while using Word.  
> EDR flags the Word process making unexpected outbound connections.  
> Deeper memory analysis reveals injected shellcode — an attacker had injected malware into `winword.exe` after gaining a foothold via phishing.  
> The malware leveraged the trusted process to evade antivirus and exfiltrate sensitive documents unnoticed.

---

## ⚠️ CompTIA Exam Traps to Avoid

- Memory injection ≠ code injection (e.g., SQL injection)  
- AV tools scanning only disk or processes **may miss injected malware**  
- Injection often leads to **privilege escalation**, not just stealth  
- Injection can occur **post-exploit** (after a foothold has already been gained)

---

## ✅ You Are Exam-Ready If You Can:

- Explain how memory injection allows malware to evade detection  
- Distinguish between process creation vs injection  
- Identify common injection methods like DLL and reflective injection  
- Recommend appropriate EDR and behavior-based defenses  
- Recognize why injected malware inherits trusted permissions  

---

### ✅ Final Mastery: Confirmed via video reflection  
**Weak spot resolved**: Memory injection ≠ separate process — it hides inside legit ones  
**Score**: Self-assessed retention strong  
