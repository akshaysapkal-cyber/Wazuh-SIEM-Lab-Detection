# Nmap Scan Detection

## Objective
- To detect port scanning activity performed on the target system.

## What Was Detected
- Wazuh generated alerts indicating potential port scanning activity.
- Multiple connection attempts were observed across different ports.

## Where to Find It
- Open Wazuh Dashboard
- Navigate to **Security Events / Dashboard**
- Search using keywords like: `scan`, `nmap`, or filter by source IP

![nmapdetect](https://github.com/akshaysapkal-cyber/Wazuh-SIEM-Lab-Detection/blob/main/Screenshots/detection/Nmap%20scan%20detect.png?raw=true)

## Key Observation
- The attacker machine sent multiple requests to different ports in a short time.
- This behavior is typical of reconnaissance activity.

## Explanation
- Port scanning is used by attackers to identify open services.
- Wazuh detected this behavior based on unusual connection patterns and generated alerts.
