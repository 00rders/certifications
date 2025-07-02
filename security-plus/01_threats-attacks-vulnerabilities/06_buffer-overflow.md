# 🧠 Buffer Overflows (SY0-701 – Domain 2.3)

## 🔍 Core Concept
A **buffer overflow** occurs when an application writes more data to a memory buffer than it was designed to hold. This causes excess data to overflow into adjacent memory locations, potentially overwriting important variables or control structures like return addresses.

## 🧬 How It Works
- Applications reserve a specific amount of memory (a buffer) for input.
- If input exceeds the buffer limit and lacks proper bounds checking, it spills over.
- Overflowed data can corrupt nearby memory or be crafted to hijack program execution.

## ⚔️ Why It’s Dangerous
- Can result in **unauthorized code execution**, **privilege escalation**, or **system crashes**.
- Used in **remote code execution (RCE)** exploits or to bypass authentication mechanisms.
- Difficult to execute — attacker needs precise control over input and knowledge of memory layout.

## 🛡️ Mitigation Strategies

| Mitigation Technique         | Purpose |
|-----------------------------|---------|
| Input Validation             | Ensures only expected input size and format are accepted |
| Bounds Checking              | Confirms data fits within memory limits before writing |
| Stack Canaries               | Inserts known values before return addresses to detect overwrites |
| ASLR (Address Space Layout Randomization) | Randomizes memory locations to prevent predictable targeting |
| DEP (Data Execution Prevention)           | Marks certain memory regions as non-executable |

## 🧑‍💻 SOC Analyst Real-World Example
A buffer overflow exploit attempt causes repeated crashes in a vulnerable web application.  
The SOC team observes stack corruption in memory logs and flags it as a possible RCE exploit.  
IRIS could assist by parsing memory dump logs, highlighting overflow patterns, and auto-suggesting mitigation flags like NX (non-executable memory) or stack canary alerts.

---

✅ **Logged by 00rders**  
_Source: Professor Messer – “Buffer Overflows” (SY0-701, Domain 2.3)_
