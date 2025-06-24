# 05 — Authentication, Authorization & Accounting (AAA)

## 🧩 Context  
The AAA framework is a security cornerstone that defines how users are verified, what they’re allowed to do, and how their actions are tracked. Every secure environment — from VPNs to internal corporate systems — relies on these principles.

## 🔧 What I Learned

- **Identification**: Claiming an identity (e.g., entering a username).
- **Authentication**: Proving that identity (e.g., entering a password, using MFA).
- **Authorization**: Determining what resources a verified user can access (based on roles, attributes, or groups).
- **Accounting**: Logging user activity — who accessed what, when, and how long.

### Supporting Concepts:

- **AAA Servers**: Handle centralized authentication (e.g., RADIUS or TACACS+ used in VPN concentrators).
- **Digital Certificates**: Used in internal networks to verify device identities (especially in enterprise environments).
- **Certificate Authority (CA)**: Central authority responsible for issuing and validating digital certificates.
- **Attribute-Based Access Control (ABAC)**: A scalable way to group users and assign permissions based on shared characteristics (e.g., job role or department).

## 🔒 Why It Matters

- Prevents unauthorized access by enforcing strict identity verification.
- Allows fine-tuned control over what users or systems can do.
- Logs everything for auditing, compliance, and post-incident investigations.

## 🛠 Real-World Application Scenario  
Your VPN login at work fails on your personal phone but works on your work-issued laptop. The VPN concentrator uses an AAA server that cross-checks your login credentials and device certificate — and your phone doesn’t have a valid certificate issued by the internal Certificate Authority. This is by design to prevent unauthorized endpoints from accessing sensitive systems.

---

## 🤖 What Could IRIS Do?

- **Parse AAA logs** to detect failed login attempts or suspicious behavior across users and devices.
- **Verify certificate status** and expiration for endpoints tied to the internal network.
- **Auto-suggest authorization model optimizations** (e.g., flag overly permissive group access).
- **Alert SOC operators** to failed authentication spikes or unauthorized resource access.

---

*Logged by Operator 00rders – with IRIS monitoring access control hygiene and identity-based behaviors.*
