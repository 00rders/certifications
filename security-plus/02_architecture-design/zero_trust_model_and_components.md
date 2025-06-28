2.1 — Zero Trust Model & Core Components  
🧩 Scenario

During another passive study session at work, I listened to a Messer Security+ video on Zero Trust architecture. I wanted to absorb the mental model of “never trust, always verify” and learn how Zero Trust networks evaluate and enforce access requests using a flow of policy components.

🔧 What I Did

🎥 Watched: “Zero Trust” by Professor Messer (Security+ SY0-601)
🎯 Maps to: CompTIA Objective 2.1 – “Compare security implications of different architecture models.”

🧠 What I Learned

Zero Trust eliminates implicit trust — even inside the network.
Access is granted per request, based on identity, context, and policy.
Key components:
- **Policy Engine**: Decides access based on context/rules.
- **Policy Administrator**: Pushes decisions/configs to enforcement points.
- **Policy Enforcement Point (PEP)**: Actually allows or denies access.
These components work in a loop to ensure no trust without verification.

🔒 Why It Matters

Zero Trust is increasingly used in modern SOC environments and cloud infrastructure.
As a future analyst or architect, I need to understand how trust is brokered at the protocol level.
These components are often hidden behind automation — knowing how they work helps with debugging, logging, and enforcement visibility.

💼 Real-World Scenario

A remote employee requests access to a secure Git repo. The Policy Engine checks:
- Device compliance  
- Time of access  
- Geo-location  
It passes the decision to the Admin, which tells the PEP to allow access. If anything’s off — like an outdated device — access is denied instantly.

🤖 What Could IRIS Do?

Parse policy enforcement logs and tag violations per user/session.
Highlight weak points in access flow (e.g., PEP allowing access without recent re-verification).
Simulate Zero Trust posture in lab environments using conditional logic.
Logged by Operator 00rders, supported by IRIS — your SOC copilot.
