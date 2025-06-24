# 04 — Digital Signatures & Hashing

## 🧩 Context  
Hashing and digital signatures are foundational to validating data integrity and proving authenticity in secure systems. They are used everywhere from file verification to encrypted communications.

## 🔧 What I Learned

- A **hash** is a one-way mathematical function that turns any input (like a file) into a fixed-length string of characters.
- If even one byte of the input changes, the resulting hash changes completely — this makes it ideal for **detecting tampering**.
- A **digital signature** has two parts:
  1. The original data is hashed.
  2. The hash is encrypted using the sender’s **private key** (asymmetric encryption).
- To verify the signature:
  - The receiver decrypts the signature with the sender’s **public key**.
  - Then hashes the original data themselves and compares it to the decrypted hash.
  - If they match, the message is authentic and unaltered.

## 🔒 Why It Matters

- **Integrity**: Confirms that data hasn't been modified.
- **Authentication**: Proves the sender's identity using cryptographic keys.
- **Non-repudiation**: The sender can’t deny having sent the message if the signature is valid.

## 🛠 Real-World Application Scenario  
An incident response team investigates a suspicious email with an attachment. The analyst checks the digital signature and finds the hash doesn't match — indicating the file was tampered with in transit. This helps the team block the payload and begin mitigation immediately.

---

## 🤖 What Could IRIS Do?

- **Auto-check hash integrity** of suspicious files and flag mismatches.
- **Validate signatures** of critical internal documents or email attachments.
- **Log hash values** in alert reports to prove whether files were modified.
- **Alert SOC teams** if a signature verification fails, offering suggestions for next steps.

---

*Logged by Operator 00rders – with IRIS assisting in cryptographic integrity and authenticity validation.*
