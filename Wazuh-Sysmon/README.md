# Wazuh & Sysmon Integration

Integrated a Windows 10 endpoint with Wazuh SIEM and Sysmon for endpoint monitoring.

### Detected Events
- Sysmon Event ID 1 — Process Creation
- Sysmon Event ID 11 — File Creation
- Sysmon Event ID 3 — Network Connection

### Result
Wazuh successfully received and generated an alert for Sysmon Event ID 11.

### Tools
Wazuh | Sysmon | PowerShell
### Evidence

![Wazuh Agent Active](Images/Wazuh_Endpoint_Agent_003_Active.png)

![Sysmon Event ID 1 - Process Creation](Images/Threat_Hunting_Sysmon_EventID_1_ProcessCreate.png)

![Sysmon Event ID 11 - File Creation](Images/Threat_Hunting_Sysmon_EID11_FileCreate.png)
![Wazuh Alert - Sysmon Event ID 11](Images/Wazuh_Alert_Sysmon_EventID_11_FileCreate.png)
