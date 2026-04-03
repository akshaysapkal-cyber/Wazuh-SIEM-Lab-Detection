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

- [wazuh installation](setup/wazuh-installation.md)
- [agent setup](setup/windows-agent-setup.md)

## Attack Simulation
The following attacks were performed:

1. Nmap Scan (Reconnaissance)
2. Brute-force Attack (Authentication)
3. Reverse Shell (Remote Access)

Detailed steps:
- [nmap](attack-simulation/nmap.md)
- [bruteforce](attack-simulation/brute-force.md)
- [reverse shell](attack-simulation/reverse-shell.md)

## Detection & Analysis
Wazuh was used to monitor logs and detect suspicious activity.

Example:
- Failed login attempts detected
- Security alerts generated in dashboard

Detailed analysis:
- [nmap detection](detection/nmap-detection.md)
- [bruteforce detection](detection/brute-force-detection.md)
- [reverse-shell detection](detection/reverse-shell-detection.md)

## Screenshots
All screenshots are available in the [](screenshots/) folder and inside respective documentation files.

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

