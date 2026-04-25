### TryHackMe Lab: Intro to SOC – Alert Triage
**Path:** Junior Security Analyst  
**Date:** Apr 24, 2026  
**Focus:** Defensive Security / Blue Team / SOC Tier 1 Operations  

#### 1. Learning Objectives
- Understand the core responsibilities of a Junior SOC Analyst
- Practice basic alert triage workflow: Identify → Investigate → Escalate → Contain
- Use a simulated alert dashboard to analyze malicious activity

#### 2. Key Concepts
**Cybersecurity** = Protecting data, systems, and networks by detecting threats and applying the right response procedures to keep them secure.  

**Junior SOC Analyst duties include:**
1. Reviewing and monitoring security alerts in a SIEM/dashboard
2. Investigating alerts to determine if they are true positives or false positives
3. Escalating confirmed incidents to senior analysts/IR team
4. Collaborating with other teams to contain threats
5. Continuous learning on new attack techniques and defense strategies

#### 3. Hands-On Lab: Alert Dashboard Investigation
**Scenario:** Investigated suspicious activity flagged in the SOC alert queue.

**Steps Taken:**
1. Accessed the alert dashboard and reviewed triggered alerts
2. Identified malicious indicator: IP address `221.181.185.159` flagged for suspicious activity
3. Escalated the alert to Tier 2 analyst: **Will Griffin**
4. Simulated containment by blocking the malicious IP on the firewall

**Results:**
- **Malicious IP Identified:** `221.181.185.159`
- **Escalated To:** Will Griffin, Tier 2 Analyst
- **Containment Confirmation:** `THM{until-we-meet-again}` returned after firewall block

#### 4. Skills Demonstrated
- Alert Triage & Analysis
- Incident Escalation Procedure
- Basic Firewall Containment Concepts
- Documentation & Reporting

#### 5. MITRE ATT&CK Mapping
While not specified in lab, this type of activity relates to **T1071 Application Layer Protocol** and **T1566 Phishing** initial access vectors often seen in SOC alerts.

#### 6. Key Takeaway
Tier 1 SOC work follows a clear process: Detect → Analyze → Escalate → Contain. Even simulated alerts reinforce the muscle memory needed for real SOC shifts.
