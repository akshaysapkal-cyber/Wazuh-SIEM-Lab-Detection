# Wazuh SOC Lab

## Overview
This project is a simple SOC lab built using Wazuh SIEM to simulate real-world attack detection.

The lab includes:
- Kali Linux (Attacker)
- Windows (Target)
- Ubuntu (Wazuh SIEM)

The goal is to perform attacks and analyze how Wazuh detects them.

## Lab Setup

- Ubuntu – Wazuh Server (Monitoring & Detection)
- Windows – Target System
- Kali Linux – Attacker Machine

## Setup Guide

Detailed setup steps are available here:

- [wazuh installation](setup/wazuh-installation.md) Step-by-step guide to install and configure the Wazuh server on Ubuntu
- [agent setup](setup/windows-agent-setup.md) Instructions to install and connect the Wazuh agent on the Windows target system.

## Attack Simulation
The following attacks were performed:

1. Nmap Scan (Reconnaissance)
2. Brute-force Attack (Authentication)
3. Reverse Shell (Remote Access)

Detailed steps:
- [nmap attack](attack-simulation/nmap.md) Performed network scanning using nmap to identify open ports and services
- [bruteforce attack](attack-simulation/brute-force.md) Multiple login attempts using Hydra tool against the RDP
- [reverse shell attack](attack-simulation/reverse-shell.md) Established unauthorized remote access from target system using Metasploit Framework

## Detection & Analysis
Wazuh was used to monitor logs and detect suspicious activity.

Example:
- Multiple Failed login attempts detected
- Security alerts were triggered on the Wazuh dashboard
- Suspicious command execution activity was logged

Detailed analysis:
- [nmap detection](detection/nmap-detection.md) Port scanning activity was detected through multiple connection attempts across different ports, indicating reconnaissance behavior
- [bruteforce detection](detection/brute-force-detection.md) Multiple failed authentication attempts were detected, indicating a potential brute-force attack
- [reverse-shell detection](detection/reverse-shell-detection.md) Suspicious command execution and unusual outbound connections were detected, indicating possible reverse shell activity

## Screenshots
All screenshots are available in the [SS](screenshots/) folder and inside respective documentation files.

## 🎯 Key Learning
- Understanding how SIEM detects attacks
- Log monitoring and alert analysis
- Basic SOC workflow

## Conclusion
This project demonstrates how real-world attacks can be detected using Wazuh SIEM.
It helped in understanding the role of a SOC analyst in monitoring and responding to security events.

## Disclaimer
This project is created for educational and ethical purposes only.
All activities were performed in a controlled lab environment.
No real systems were harmed or targeted.

