# Wazuh SOC Lab Deployment

## Overview

This document outlines the steps used to deploy the Wazuh SIEM platform in a home lab environment using Ubuntu Server and Docker.

The goal of this deployment was to create a small SOC-style monitoring environment capable of collecting logs, displaying alerts, and allowing investigation of system activity.

## 1. Prepare Server Host

The Wazuh server was deployed on a repurposed Mac mini running Ubuntu Server.

Basic preparation steps included:

- Create a bootable Ubuntu Server USB installer
- Boot the Mac mini from USB
- Replace the previous operating system with Ubuntu Server
- Complete initial setup
- Update system packages

Example:

```bash
sudo apt update
sudo apt upgrade
```

## 2. Install Docker

Wazuh was deployed using Docker containers.

Docker installation example:

```bash
sudo apt install docker.io
```

Verify installation:

```bash
docker --version
```

## 3. Deploy Wazuh

The Wazuh Docker deployment was used to launch the following components:

- Wazuh Manager
- Wazuh Indexer
- Wazuh Dashboard

Containers were started and verified using:

```bash
docker ps
```

Once running, the Wazuh dashboard became accessible through a web browser.

## 4. Access the Wazuh Dashboard

The dashboard allows visualization of alerts, logs, and monitored systems.

From the workstation, the dashboard was accessed through the server's IP address.

Example:

```bash
https://SERVER-IP
```

## 5. Generate Test Activity

Activity was generated from the testing machine using tools such as:

- Nmap
- basic network commands
- system activity on monitored endpoints

This allowed logs and events to appear inside the Wazuh dashboard.

## 6. Verify Monitoring

Successful deployment was confirmed by observing:

- system logs
- endpoint activity
- dashboard alerts
- connected agents

These events demonstrate the visibility provided by a SIEM platform.

## Outcome

This deployment created a functioning SOC-style lab environment capable of monitoring system activity and displaying events in the Wazuh dashboard.
