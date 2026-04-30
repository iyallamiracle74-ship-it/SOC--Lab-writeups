### TryHackMe: Cyber Kill Chain
**Path:** Junior Security Analyst  
**Date:** Apr 30, 2026  
**Focus:** Understanding Attack Lifecycle for Defensive Mapping

#### 1. The 7 Stages of the Cyber Kill Chain
Lockheed Martin’s model breaks an attack into 7 steps. If we stop any step, we break the chain.

1. **Reconnaissance** – Attacker researches the target.  
   *Example:* Googling employees, scanning for open ports.  
   *SOC Defense:* Threat intel, OSINT monitoring, block port scans.

2. **Weaponization** – Attacker creates malware/payload.  
   *Example:* Building malicious Word doc with macro.  
   *SOC Defense:* Not much here — happens on attacker’s machine.

3. **Delivery** – Attacker sends payload to victim.  
   *Example:* Phishing email, malicious USB, compromised website.  
   *SOC Defense:* Email security gateway, web proxy, user training. **Most alerts fire here.**

4. **Exploitation** – Malicious code runs on victim system.  
   *Example:* User opens doc, macro runs, exploits unpatched Office.  
   *SOC Defense:* EDR, patch management, endpoint hardening.

5. **Installation** – Malware installs persistence on the host.  
   *Example:* Drops backdoor, creates registry run key, installs RAT.  
   *SOC Defense:* EDR alerts on new services, app whitelisting, AV.

6. **Command & Control (C2)** – Malware calls home to attacker.  
   *Example:* Beacon to attacker IP/domain every 60s.  
   *SOC Defense:* Firewall blocks bad IPs, DNS filtering, SIEM detects beaconing.

7. **Actions on Objectives** – Attacker completes goal.  
   *Example:* Steal data, encrypt for ransomware, destroy systems.  
   *SOC Defense:* DLP, backups, network segmentation, IR plan.

#### 2. How I Use This as Tier 1 SOC Analyst
When I get an alert, I map it to a Kill Chain stage to decide urgency:

| Stage | Priority | Action |
| --- | --- | --- |
| **Delivery/Exploitation** | P1 Critical | Stop now. Isolate host, block sender |
| **Installation/C2** | P2 High | Already compromised. Investigate spread |
| **Reconnaissance** | P3 Low | Log, monitor, threat hunt later |
| **Actions on Objectives** | P0 Breach | Escalate to IR immediately |

#### 3. Key Takeaway for Interviews
**"The earlier we break the Kill Chain, the cheaper the incident."**  
My job in Tier 1 is to catch attacks at Delivery or Exploitation before they reach Installation. That’s why fast triage using the 5 W’s matters.

#### 4. Skills Demonstrated
- Attack lifecycle mapping
- Defensive control alignment to attacker TTPs  
- Alert prioritization based on Kill Chain stage
