# Alert Testing and Activity Generation

## Overview

After deploying Wazuh, test activity was generated within the lab environment to observe how events appear in the monitoring dashboard.

The goal was to simulate normal and suspicious activity and verify that logs were visible through the Wazuh interface.

---

## Test Activity Source

Activity was generated from the testing system:

- Device: Repurposed 2012 MacBook Pro
- Operating System: Ubuntu 22.04 LTS (Jammy Jellyfish)
- Security Tools: Kali Linux virtual machine

Tools used included:

- Nmap
- basic Linux network commands
- normal system activity

---

## Network Scan Example

A basic network scan was performed from the Kali virtual machine to observe how the environment responded.

Example command:

```bash
nmap -sS TARGET-IP
```

This type of scan attempts to discover open ports and services on the target system.

---

## Observing Events in Wazuh

After generating activity, the Wazuh dashboard was used to review logs and alerts.

Areas observed included:

- Security events
- System logs
- Endpoint activity
- Network behavior

The purpose was to understand how monitoring tools detect and display activity occurring in the environment.

---

## Why This Matters

Security analysts rely on SIEM platforms to identify suspicious activity and investigate events.

This exercise demonstrated:

- how activity in the environment generates logs
- how those logs appear inside Wazuh
- how analysts can begin investigating security events
