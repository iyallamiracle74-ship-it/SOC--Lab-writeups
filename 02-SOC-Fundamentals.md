### TryHackMe: SOC Fundamentals  
**Path:** Junior Security Analyst  
**Date:** Apr 28, 2026  
**Focus:** SOC Structure, People, Process, Technology & Alert Triage

#### 1. What is a SOC?
**SOC = Security Operations Center**  
A dedicated facility operated by specialized security teams. The main objectives are to build a baseline for detection and to respond to cybersecurity incidents.

#### 2. Core Purpose: Detection & Response
The primary focus of a SOC is **Detection and Response**.

**Detection includes:**
1. **Detect Vulnerabilities** – Identifying weaknesses in systems before attackers exploit them
2. **Detect Unauthorized Activity** – Example: An attacker uses stolen employee credentials to log into company systems
3. **Detect Policy Violations** – Identifying when security rules and procedures are broken. A security policy is a set of rules created to protect the company against threats.

**Response** – Actions taken to support and contain an incident after detection.

#### 3. The Three Pillars: People, Process, Technology

**People** – Security solutions generate numerous alerts, creating “noise.” Skilled analysts are needed to separate real threats from false positives.

**SOC Team Structure:**
1. **CISO** – Chief Information Security Officer, executive level
2. **SOC Manager** – Head of the SOC team, provides direction and support
3. **Tier 1 SOC Analyst** – First line of defense. Monitors alerts, performs initial triage, escalates true positives to Tier 2
4. **Tier 2 SOC Analyst** – Conducts deeper investigation and analysis of escalated incidents
5. **Tier 3 SOC Analyst** – Most experienced. Handles advanced threats, forensics, threat hunting
6. **Security Engineer** – Deploys, configures, and maintains security solutions/tools
7. **Detection Engineer** – Creates and tunes security rules, detection logic, and alerts

**Process** – Standardized workflows ensure consistent incident handling. Tier 1 focuses on **Alert Triage using the 5 W’s:**

1. **What** – What caused the incident? What activity triggered the alert?
2. **When** – When was it detected? Date and time
3. **Where** – Where was the malicious activity detected? Which host/IP?
4. **Who** – Who was involved? Source user/host or who detected it
5. **Why** – Why did it happen? Was it malicious or authorized?

After investigation: **Reporting & Incident Report**, plus **Forensics** if needed.

**Technology** – Tools that enable SOC operations:
1. **SIEM** – Security Information & Event Management. Collects and correlates logs from multiple sources. Provides detection capabilities in a SOC environment.
2. **EDR** – Endpoint Detection & Response. Gives SOC teams detailed, real-time and historical visibility into device activities.
3. **Firewall** – Security device that monitors incoming and outgoing network traffic.
4. **IDS/IPS** – Intrusion Detection/Prevention Systems for network threats.
5. **XDR** – Extended Detection & Response across multiple layers.
6. **SOAR** – Security Orchestration, Automation & Response for workflow automation.

#### 4. Hands-On Lab: Port Scan Alert Triage
**Scenario:** As a Tier 1 SOC Analyst, received alert for port scanning activity. Accessed SIEM to view associated logs and answer the 5 W’s. Vulnerability Assessment team notified SOC they were running an authorized port scan from host `10.0.0.8`.

**Investigation using 5 W’s:**
- **What:** Port scan activity triggered the alert
- **When:** June 12, 2014, 5:24 PM
- **Where:** Destination host IP `10.0.0.8`
- **Who:** Source host name `Nessus` scanner
- **Why:** Intended scan by internal team, not malicious

**Result:** Confirmed false positive. Alert closed after verification.  
**Flag:** `THM{0003000-intro-to-soc}`

#### 5. Skills Demonstrated
- Alert Triage using 5 W’s methodology
- SIEM log analysis
- Distinguishing authorized vs malicious activity
- Incident documentation and closure
- Understanding SOC tools: SIEM, EDR, Firewall

#### 6. Key Takeaway for Interviews
Tier 1 analysts use People, Process, and Technology to turn noisy alerts into clear answers. The 5 W’s framework ensures I collect complete context before escalating. Not every alert is an attack — verification prevents wasted Tier 2 time.
