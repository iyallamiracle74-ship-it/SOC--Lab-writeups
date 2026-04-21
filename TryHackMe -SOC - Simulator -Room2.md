# TryHackMe: SOC Simulator - Room 2
**Date:** April 2026  
**Tools:** Splunk, Alert Triage, Log Analysis  
**Skills:** Incident Response, False Positive Identification, Alert Documentation

## Objective
Investigate alerts in a simulated SOC environment and determine if escalation is required based on evidence.

## Key Findings
1. Triaged multiple SOC alerts including authentication failures and suspicious process execution
2. Used Splunk to correlate login events with source IPs to distinguish between scans and actual attacks
3. Identified false positive alerts based on absence of successful authentication or follow-on activity
4. Documented true positive findings with supporting log evidence for escalation per SOC procedure

## MITRE ATT&CK
T1110 - Brute Force  
T1059.001 - PowerShell

## Takeaway
Practiced core SOC workflow: validate alert → investigate with logs → document findings → escalate or close. Learned how log correlation reduces noise and prevents alert fatigue.
