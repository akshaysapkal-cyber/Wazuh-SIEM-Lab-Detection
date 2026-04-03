# Brute-force Attack (Authentication)

## Objective
- To simulate multiple failed login attempts on the target system using SMB service.

## Step 1: Identify Target IP
```bash
ipconfig
```
Finds the IP address of the Windows target machine.

(Add screenshot: Windows IP address)

## Step 2: Perform Brute-force Attack from Kali
```bash
hydra -l <Target username> -P /usr/share/wordlists/rockyou.txt smb://<Target ip>
```
Attempts multiple password combinations on the SMB service.

(Add screenshot: hydra attack running)

## Step 3: Observe Failed Login Events
Multiple failed login attempts are generated on the Windows system and logged in Wazuh.
Shows how authentication failures are detected.

(Add screenshot: Wazuh alerts or logs)

## What Happened
- The attacker used a password list to try multiple login attempts.
- This generated repeated failed authentication events.

## SOC Relevance
* Brute-force attacks are common in real environments.
* Detecting repeated login failures helps identify unauthorized access attempts.
