01 — Physical Security Controls (Security+ Focused)  
🧩 Scenario

I listened to Professor Messer’s Security+ video on physical security controls during a stealth-mode study session while working retail. I intentionally focused on identifying **only the devices and concepts most likely to show up on the CompTIA Security+ exam**, filtering out overly intuitive or low-value facts like "lighting deters intruders."

🔧 What I Did

🎥 Watched: “Physical Security Controls” by Professor Messer (Security+ SY0-601)  
🎯 Maps to: CompTIA Objective 3.5 – “Implement physical controls to secure assets.”

🧠 What I Learned

These are the physical security devices and methods most likely to be tested:

#### 🚪 **Barricades & Bollards**
- *Prevent vehicle-based threats* and control access to buildings or areas.

#### 🚧 **Access Control Vestibules** (aka “Mantraps”)
- One door must close before the next opens.
- *Prevents tailgating and unauthorized entry.*

#### 🎛️ **Alarms & Sensors**
- Motion detectors, door sensors, and glass break sensors detect unauthorized access attempts.

#### 🔐 **Badges, Smart Cards, Biometrics**
- Used for identity verification and access enforcement at entry points.
- Multi-factor when combined with PINs or passwords.

#### 📷 **Video Surveillance (CCTV)**
- Records activity; often integrated with motion detection or access logs.
- Useful for deterrence *and* post-incident review.

#### 🔄 **Key Management**
- Controlled distribution of physical keys and fobs.
- Includes key control logs and limited duplication policies.

#### 🛡️ **Guards**
- Human presence as an active deterrent and first-line detection mechanism.

#### 🔒 **Cable Locks & Locking Cabinets**
- Prevent unauthorized physical access to mobile devices or servers.

#### 🚪 **Door Access Controls**
- Electronic locks (e.g., magnetic or smart locks) that log entry data and allow scheduled access.

#### ☢️ **Faraday Cages / Shielding**
- Block wireless or electromagnetic signal leakage, especially for secured environments.

🔒 Why It Matters

Even the most secure network is vulnerable to **physical access attacks** (e.g., plugging in rogue devices, stealing drives). Understanding these physical layers is essential for implementing full defense-in-depth.

💼 Real-World Scenario

A SOC analyst notices unexpected data exfiltration. Upon review, footage shows a third-party contractor entering through a propped door. This was a failure of both the door access control system and surveillance review protocols. Physical security gaps led to a digital breach.

🤖 What Could IRIS Do?

Cross-reference building access logs with login timestamps to detect suspicious patterns.
Parse badge entry logs and highlight after-hours activity.
Maintain a physical access inventory for incident response.
Logged by Operator 00rders, supported by IRIS — your SOC copilot.
