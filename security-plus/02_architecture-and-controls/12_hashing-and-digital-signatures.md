# 🔏 Hashing and Digital Signatures  
**CompTIA Security+ — Domain 2: Architecture & Design**  
*Logged by 00rders*

---

## ✅ Core Concepts

### 🔁 Hashing
- A **one-way cryptographic function** that converts input data into a fixed-length string (hash).
- Common algorithms:
  - `SHA-256`, `SHA-1`, `MD5` (⚠️ outdated)
- Used to:
  - Ensure **data integrity**
  - Detect **file tampering**
  - Store **passwords** securely (when combined with salt)

---

### 🧂 Salt (Password Hashing Enhancement)
- A **random value** added to a password *before* it’s hashed.
- Purpose:
  - Defeats **rainbow table attacks**
  - Makes **each hash unique**, even if two users choose the same password
- Example:
  - `"password123"` → salt: `"8@4f$"` → hash: SHA256(`"8@4f$password123"`)

---

## 🧾 Digital Signatures

### 🔐 What They Do
- Provide:
  - **Authentication** (proves the sender is who they say they are)
  - **Integrity** (proves the message wasn't altered)
  - **Non-repudiation** (sender cannot deny having sent it)

### 🧰 How They Work (Corrected Flow)
1. **Sender hashes** the original message using SHA-256.
2. Sender then **encrypts the hash using their *private key***.
   - ✅ This creates the **digital signature**.
3. **Signature + original message** are sent to the recipient.
4. **Recipient decrypts** the signature using the sender’s **public key**, revealing the original hash.
5. They hash the received message themselves and compare both hashes:
   - ✅ If hashes match → integrity and authenticity confirmed.

---

## 🧠 Real-World SOC Application
> You receive a critical software patch from a vendor. You hash the file and compare it to the published hash on the vendor’s website. It matches — confirming **integrity**. Additionally, the patch file is signed with the vendor’s private key. Your system verifies it using their **public key**, confirming **authenticity**.

---

## 🎯 Exam Takeaways
- **Hashing is one-way** — cannot be reversed
- **Salting defeats rainbow tables**
- **Digital signatures = hashed data encrypted with the sender’s private key**
- **Verify** with the sender’s **public key**

---

*Let me know when you're ready for the focused exam-style quiz.*
