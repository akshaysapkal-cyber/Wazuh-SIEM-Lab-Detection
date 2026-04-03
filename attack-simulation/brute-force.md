# Brute-force Attack (Authentication)

## Objective
- To simulate multiple failed login attempts on the target system using RDP service.

## Step 1: Identify Target IP
```bash
ipconfig
```
Finds the IP address of the Windows target machine.

## Step 2: Perform Brute-force Attack from Kali
```bash
hydra -l <Target username> -P /usr/share/wordlists/rockyou.txt rdp://<Target ip>
```
Attempts multiple password combinations on the RDP service.

![brute force](https://github.com/akshaysapkal-cyber/Wazuh-SIEM-Lab-Detection/blob/main/Screenshots/attack/brute%20attack.png?raw=true)

## Step 3: Observe Failed Login Events
Multiple failed login attempts are generated on the Windows system and logged in Wazuh.
Shows how authentication failures are detected.
- [bruteforce detection](detection/brute-force-detection.md)

## What Happened
- The attacker used a password list to try multiple login attempts.
- This generated repeated failed authentication events.

## SOC Relevance
* Brute-force attacks are common in real environments.
* Detecting repeated login failures helps identify unauthorized access attempts.
