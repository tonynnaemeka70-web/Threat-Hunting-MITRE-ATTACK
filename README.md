 Threat Hunting Using MITRE ATT&CK

Project Overview
This project demonstrates a hands-on threat hunting exercise using Sysmon telemetry mapped to the MITRE ATT&CK framework.  
The goal is to identify suspicious behaviors on a Windows 10 endpoint and correlate them to known adversary techniques.

Objectives
 Deploy and configure Sysmon for endpoint visibility
 Collect and analyze Windows event telemetry
 Develop threat hunting hypotheses based on MITRE ATT&CK
 Identify suspicious process execution and network activity
 Document findings with supporting evidence

 Tools & Technologies
Sysmon (Sysinternals)
Windows 10
MITRE ATT&CK Framework
Event Viewer
PowerShell
Kali Linux(attack simulation)
Ubuntu SIEM(log analysis environment)

Lab Environment
Component | Description 
Endpoint | Windows 10 
Monitoring | Sysmon 
Attacker | Kali Linux 
Analysis | Ubuntu SIEM
Logs | Windows Event Logs

Threat Hunting Hypothesis
Hypothesis:  
An attacker may attempt to execute encoded PowerShell commands to evade detection.

MITRE Technique 
T1059.001 – Command and Scripting Interpreter: PowerShell

Investigation Steps
1. Installed and configured Sysmon
2. Generated suspicious PowerShell activity
3. Filtered Sysmon Event ID 1 (Process Creation)
4. Analyzed command-line arguments
5. Correlated findings with MITRE ATT&CK

Evidence

Screenshots of Sysmon events are stored in the screenshots directory and include:

 Process creation events
 Network connection telemetry
 Encoded PowerShell execution

Key Findings
 Encoded PowerShell execution was detected
Sysmon successfully captured process and network activity
Behavior matched MITRE ATT&CK technique T1059.001

Lessons Learned
Sysmon provides high-fidelity endpoint telemetry
Proper filtering is essential due to high event volume
MITRE ATT&CK improves structured threat hunting

Future Improvements
Integrate logs into SIEM (Wazuh / ELK)
Create automated detection rules
Expand hunting to lateral movement techniques

Author
Tony Nnaemeka  
Cybersecurity Analyst | SOC | Blue Team
