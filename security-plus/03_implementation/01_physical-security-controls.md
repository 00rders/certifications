### 📘 Notes — Physical Security Controls  
**CompTIA Security+ Objective: 3.4 — Given a scenario, implement physical security controls**

---

### 🧠 Core Concepts

**Physical security** defends personnel, equipment, and data against **physical threats**, including:
- Theft or unauthorized access
- Environmental hazards (fire, water, heat)
- Insider threats or sabotage
- Social engineering techniques (tailgating, shoulder surfing)

Unlike logical or technical controls, physical security relies on:
- Environmental design
- Physical hardware
- Human enforcement

---

### 🧱 Categories of Physical Security Controls

#### 1. **Perimeter Security**
- Fences, lighting, signage, gates
- Purpose: Deter and delay unauthorized access
- Often supported by security patrols and boundary monitoring

#### 2. **Access Control Mechanisms**
- Key cards, biometrics (fingerprint, retina), security guards, ID badges
- Restricts access based on identity
- Often enforced through multi-factor authentication (badge + PIN)

#### 3. **Barriers and Entry Management**
- Mantraps, turnstiles, bollards, safes, server cabinet locks
- Used to enforce **one-person-at-a-time entry** and protect sensitive physical assets

#### 4. **Surveillance and Monitoring**
- CCTV, IP cameras, motion sensors, glass break sensors, alarms
- Provides visibility and deterrence
- Enables real-time response and forensic review

#### 5. **Environmental and Safety Controls**
- Fire suppression: sprinklers, halon/clean agent systems
- HVAC: temperature and humidity controls
- Flood sensors, power backups (UPS, generators)
- Protects equipment from **non-malicious threats** like fire, overheating, or water damage

---

### 🔐 Why It Matters in Security

- Physical access can **bypass digital protections** — attackers with physical access can:
  - Steal hardware
  - Plug in rogue devices (e.g., malicious USBs)
  - Clone badge credentials
- Many major breaches started with **simple physical oversights**
- Strong physical security is foundational to **defense-in-depth** models

---

### 💼 Real-World SOC Example

> An intruder tailgates into a secure data center during a shift change.  
> They drop a rogue Raspberry Pi behind a desk and walk out unnoticed.  
> Thanks to **motion detection**, **CCTV logging**, and a **policy-enforced mantrap**, the device is spotted during routine review.  
> The SOC team pulls access logs and correlates badge activity, identifying the breach and preventing further compromise.

---

*Logged by 00rders*
