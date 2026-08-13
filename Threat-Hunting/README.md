# Threat Hunting Lab

## Overview
A practical threat hunting lab using Wazuh and Sysmon to investigate Windows process and network activity.

## Objectives
- Investigate Windows process creation events.
- Analyze parent-child process relationships.
- Review command-line activity.
- Identify suspicious process execution.
- Review Sysmon network connection telemetry.

## Tools
- Wazuh
- Sysmon
- Windows 10
- PowerShell

## Investigation

### 1. Suspicious Process Chain

A PowerShell process spawned `cmd.exe` to execute `whoami` and redirect the output to a temporary file:

PowerShell → cmd.exe → whoami → File Output

### Evidence — Process Creation (Event 4688)

The event shows PowerShell spawning `cmd.exe` with a command that executes `whoami` and redirects the output to a temporary file.

![Suspicious Process Chain](Images/threat-hunting-process-chain.png)

### Analysis
PowerShell spawned cmd.exe using a bypassed execution policy and executed `whoami` with output redirected to a temp file.  
This behavior is commonly associated with reconnaissance or script‑based attacks, not normal administrative activity.

### Conclusion
The hunt confirms abnormal PowerShell activity that should be investigated further.
