# Home SOC Lab – SIEM Monitoring & Threat Detection

## Overview

This project is a hands-on Security Operations Center (SOC) lab that I built using Wazuh, Ubuntu Server, and Windows 11 virtual machines. The goal was to create a security monitoring environment where I could collect endpoint logs, detect suspicious activity, and investigate security events.

I configured Wazuh to monitor a Windows endpoint and practiced investigating authentication failures, file integrity changes, and process execution events.

## Lab Architecture

**Environment:**
- Ubuntu Server – Wazuh Manager
- Windows 11 – Wazuh Agent
- Wazuh Dashboard – Security monitoring and event investigation
- Sysmon – Detailed Windows process monitoring
- VirtualBox – Virtual machine environment

**Architecture:**

Windows 11 VM → Wazuh Agent → Ubuntu Wazuh Manager → Wazuh Dashboard

## Implementation

### 1. SIEM Deployment and Configuration
- Installed and configured Wazuh Manager on Ubuntu.
- Deployed the Wazuh agent on a Windows 11 virtual machine.
- Connected the Windows endpoint to the Wazuh manager.
- Verified agent connectivity and log collection.

### 2. Windows Authentication Monitoring
- Monitored Windows authentication events through Wazuh.
- Generated failed login attempts to test security monitoring.
- Used Wazuh Threat Hunting to locate and review authentication failures.
- Examined event details to understand potential unauthorized login activity.

### 3. File Integrity Monitoring (FIM)
- Configured Wazuh to monitor a designated Windows directory.
- Enabled real-time monitoring and file change reporting.
- Tested file creation, modification, and deletion.
- Reviewed file hashes and content differences in the Wazuh dashboard.

### 4. Sysmon Process Monitoring
- Installed Sysmon on the Windows endpoint.
- Configured the Wazuh agent to collect Sysmon operational logs.
- Monitored process creation events (Event ID 1).
- Examined executable paths, command-line arguments, parent processes, and user accounts.

### 5. Process Investigation
- Investigated a SecEdit.exe process creation event.
- Examined its PowerShell parent process and command-line arguments.
- Identified that the command exported local security policy settings.
- Documented the findings and considered whether the activity was expected.

## Skills Demonstrated

- SIEM Configuration and Monitoring
- Wazuh
- Windows Event Log Analysis
- File Integrity Monitoring
- Endpoint Monitoring
- Sysmon
- Authentication Event Analysis
- Process Investigation
- Basic Incident Investigation
- Linux and Windows Administration
- Virtual Machine Configuration

## Project Evidence

Screenshots and investigation notes are included in the repository to demonstrate the lab configuration, monitoring capabilities, and investigation results.

## Conclusion

This project gave me hands-on experience setting up a SIEM environment and investigating endpoint security events. It helped me understand how SOC analysts use centralized logging and monitoring tools to identify and investigate potentially suspicious activity.
