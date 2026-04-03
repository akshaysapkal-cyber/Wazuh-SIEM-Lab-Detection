# Nmap Scan (Reconnaissance)

## Objective
- To identify open ports and services on the target system.

## Step 1: Run Nmap Scan from Kali
```bash
nmap -sS <Target ip>
```
Performs a TCP SYN scan on the target machine (Windows).

![NmapSyn](https://github.com/akshaysapkal-cyber/Wazuh-SIEM-Lab-Detection/blob/main/Screenshots/attack/NmapSyn.png?raw=true)

## Step 2: View Scan Results
The output shows open ports and services available on the target system.

## What Happened
- The attacker scanned the target system to gather information.
- Open ports indicate available services that can be targeted.

## SOC Relevance
- Reconnaissance is the first stage of an attack.
- Detecting scans helps identify potential threats early.
