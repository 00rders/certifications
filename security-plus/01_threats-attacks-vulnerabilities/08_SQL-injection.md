### 📘 Notes — SQL Injection (SQLi)  
**CompTIA Security+ Objective: 1.2 — Identify common types of vulnerabilities and their characteristics**

---

### 🧠 Core Concepts

#### 🧨 What Is SQL Injection?
**SQL Injection (SQLi)** is a web application attack where malicious SQL code is inserted into input fields to manipulate the backend database.

It allows attackers to:
- Read sensitive data they shouldn't access
- Modify or delete database contents
- Execute administrative operations
- Bypass authentication or extract credentials

---

### 💉 How SQL Injection Works

- Web applications send user input to the database via **SQL queries**.
- If the input is **not sanitized or validated**, attackers can inject SQL commands that modify the query logic.

#### 🧪 Example:

SELECT * FROM users WHERE username = 'admin' AND password = '123';

Injected with:

' OR '1'='1

Becomes:

SELECT * FROM users WHERE username = '' OR '1'='1';

> ✅ Always true — allows bypass of login without valid credentials.

---

### 🧭 Types of SQL Injection

| Type                   | Description                                         |
|------------------------|-----------------------------------------------------|
| **Classic/Inline SQLi**| Injected directly into a vulnerable input field     |
| **Blind SQLi**         | No visible error — attacker infers data from behavior |
| **Error-based SQLi**   | Server error messages reveal query structure/data   |
| **Union-based SQLi**   | Combines multiple SELECT statements to extract more data |

---

### 🛡️ Prevention and Mitigation

| Defense Technique       | Description |
|-------------------------|-------------|
| **Parameterized Queries (Prepared Statements)** | Use variables instead of directly injecting user input into SQL |
| **Input Validation**    | Filter/validate input for illegal characters |
| **Stored Procedures**   | Abstract query logic away from user input |
| **Least Privilege**     | DB accounts used by apps should have limited rights |
| **Error Handling**      | Suppress verbose DB errors to avoid leakage |

> 🔐 *Never trust client input. Always sanitize and separate data from code.*

---

### ⚠️ Why It Matters in Security

- SQLi is one of the **OWASP Top 10** most critical web app risks
- Common in legacy applications or poorly coded login/search fields
- Can result in:
  - Full database compromise
  - Data exfiltration (PII, credentials, financials)
  - Permanent data loss or corruption

---

### 💼 Real-World SOC Example

> A threat actor triggers a login form alert with strange characters (`' OR 1=1 --`).  
> SOC analysis shows that the app fails to use prepared statements.  
> IRIS could detect repetitive failed inputs, analyze input strings for SQL patterns, and cross-reference with OWASP rules to escalate the alert.

---

### ✅ CompTIA Objective Mapping

- **1.2 — Vulnerabilities**
  - Input validation issues  
  - Injection-based attacks  
  - Database exploitation  
  - Web app weaknesses (forms, parameters, auth bypass)

---

**Logged by 00rders**
