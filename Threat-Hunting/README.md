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
PowerShell spawned `cmd.exe` using a bypassed execution policy and executed `whoami` with output redirected to a temporary file.
This behavior was treated as suspicious in the lab because of the process chain and execution context and was investigated as potential reconnaissance behavior.

### Conclusion
The activity was identified as potentially suspicious and would require further investigation in a real environment.
