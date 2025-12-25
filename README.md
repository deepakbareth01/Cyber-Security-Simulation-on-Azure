# Azure Cloud SOC & SIEM Laboratory

## 🛡️ Project Overview
This project demonstrates the implementation of a functional Security Operations Center (SOC) in a cloud environment using **Microsoft Azure** and **Wazuh SIEM**. The goal was to simulate real-world cyber attacks and implement security hardening to defend the infrastructure.

## 🏗️ Environment Details
- **Cloud Provider:** Microsoft Azure
- **Resource Group:** Cyber-Project-RG
- **Virtual Network:** 10.0.0.0/16
- **Machines:** - **Web-Server (Ubuntu 24.04):** Monitored by Wazuh agent.
  - **Attacker-VM:** Used for simulating Brute Force attacks.

## ⚔️ Attack Simulation (Red Team)
- **Tool used:** Nmap & SSH Brute Force scripts.
- **Discovery:** Performed port scanning to identify open services (Port 22, Port 80).
- **Execution:** Simulated a brute force attack resulting in **2,754 authentication failures** captured by the SIEM.

## 🛡️ Defense & Hardening (Blue Team)
- **SIEM Monitoring:** Integrated Wazuh to detect and alert on brute force attempts in real-time.
- **SSH Hardening:** Disabled password-based authentication (`PasswordAuthentication no`) in `/etc/ssh/sshd_config`.
- **Verification:** Confirmed that attackers can no longer attempt password-based logins, significantly reducing the attack surface.

## 📊 Final Results
The project successfully demonstrated the full lifecycle of a cyber-attack: from initial scanning to detection and final mitigation through systematic hardening.

---
**Full Project Report:** [Download majorr project.pdf](./majorr%20project.pdf)
