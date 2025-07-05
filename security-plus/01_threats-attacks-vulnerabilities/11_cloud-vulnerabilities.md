### 📘 Notes — Cloud Vulnerabilities  
**CompTIA Security+ Objective: 1.2 — Identify common types of vulnerabilities and their characteristics**

---

### 🧠 Core Concepts

#### ☁️ What Are Cloud Vulnerabilities?
Cloud vulnerabilities are weaknesses in the configuration, management, or architecture of cloud services that can be exploited to compromise systems or data.

> ⚠️ Public cloud services are often exposed to the internet by design—this increases the **attack surface** and demands strict security controls.

---

### 🌐 Why Cloud is a Prime Target

- **Global Access**: Cloud services are reachable from anywhere, making brute-force or scanning attacks easier.
- **Shared Responsibility Model**: Cloud providers secure the infrastructure; customers must secure their workloads (configs, permissions, apps).
- **Misconfigurations**: One of the most common causes of breaches—e.g., leaving storage buckets or databases open to the public.
- **Cloud Service Complexity**: APIs, access keys, and dynamic scaling introduce more vectors to secure.

---

### 🚨 Common Cloud Attack Vectors

| Vulnerability/Attack         | Description |
|-----------------------------|-------------|
| **Public Exposure**          | Misconfigured storage (e.g. open S3 buckets) or services accessible without authentication |
| **Insecure APIs**            | Poorly secured APIs allow attackers to exploit functions or gain unauthorized access |
| **Stolen Credentials**       | If access keys or tokens are leaked, attackers can take full control of cloud assets |
| **SQL Injection in Cloud Apps** | Exploiting cloud-hosted web apps to exfiltrate or alter backend data |
| **DDoS Attacks**             | Overloading cloud-hosted services to cause downtime |
| **Privilege Mismanagement**  | Granting overly broad permissions or not segmenting roles in cloud accounts |

---

### 🧑‍💻 Real-World SOC Example

A company hosts its application backend in AWS with a public-facing API and stores user data in an S3 bucket. Due to a misconfigured bucket policy, the data is publicly accessible. An attacker discovers the exposed endpoint using a scanning tool and downloads confidential files. The organization suffers a data breach, reputational damage, and regulatory fines.

---

### 🛡️ Risk-Based Strategy

- Audit and monitor cloud permissions regularly  
- Use IAM roles with least-privilege access  
- Implement logging, alerting, and centralized monitoring (e.g. AWS CloudTrail, Azure Monitor)  
- Use Web Application Firewalls (WAFs) and API gateways  
- Protect against DDoS with rate limiting and auto-scaling policies  
- Rotate credentials and monitor for secret/key leaks  

---

### 📌 CompTIA Mapping

- Cloud misconfigurations  
- SQL injection on hosted services  
- Availability threats via DDoS  
- Shared responsibility model  
- Insecure API exposure  
- Credential management in cloud systems  

---

**Logged by 00rders**
