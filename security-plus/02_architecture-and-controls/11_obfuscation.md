# 🕵️ Obfuscation  
**CompTIA Security+ — Domain 2: Architecture & Design**  
*Logged by 00rders*

---

## ✅ Core Concepts

### 🔍 Obfuscation
- The process of **making data difficult to interpret**, often by hiding it *in plain sight*.
- **Not a replacement** for encryption — but can be used alongside it for **defense in depth**.
- Goal: Confuse, conceal, or mislead unauthorized observers.

---

### 🧬 Common Obfuscation Techniques

#### 📷 Steganography
- Hides data inside other data (e.g., **an image, audio file, or video**).
- Used in:
  - Malware command and control
  - Covert communication
- As long as the **receiver knows the method**, the original message can be extracted.

#### 🌐 Protocol-level Obfuscation
- Data hidden inside **network protocols** (e.g., HTTP headers, DNS queries).
- Can be used for:
  - Exfiltration
  - Circumventing firewalls or detection tools

---

## 🧩 Related Concepts

### 🔐 Tokenization
- Replaces **sensitive data** with a **non-sensitive placeholder** (a “token”).
- Token holds **no mathematical or exploitable relationship** to the original data.
- Example: 
  - Apple Pay or Google Pay → uses **one-time-use tokens** transmitted via NFC.
  - Even if intercepted, the token is useless.

### 🕶️ Data Masking
- Conceals **part of the real data** to protect confidentiality.
- Example:
  - `**** **** **** 1234` on credit card displays
- Used in:
  - Testing environments
  - User interface displays
  - Privacy-preserving analytics

---

## 🧠 Real-World SOC Application
> While investigating outbound DNS traffic, you detect steganographic data hidden in DNS TXT records — a form of **protocol-level obfuscation** used for covert exfiltration. Your IR tool detects a mismatch between the file size and visual content of a .png image, hinting at **data embedded via steganography**.

---

## 🎯 Exam Takeaways
- **Obfuscation ≠ Encryption**, but still useful
- **Steganography** = hide data inside files
- **Tokenization** = safe replacement for sensitive data (esp. in payments)
- **Data masking** = obscuring partial data (UI, logs, testing)

---

*Let me know if you want a short quiz — or we can roll right into the next Messer video.*
