# Brute-force Attack Detection

## Objective
- To identify multiple failed login attempts on the target system.

## Detection
During the attack, several failed login attempts were generated on the Windows machine. These events were captured by Wazuh and appeared as authentication failure alerts in the dashboard.

## Where to Check
- Open Wazuh Dashboard
- Go to **Security Events / Dashboard**
- Search for terms like `failed login` or filter using the attacker IP

![bruteforcedetect](https://github.com/akshaysapkal-cyber/Wazuh-SIEM-Lab-Detection/blob/main/Screenshots/detection/bruteforcedetect.png?raw=true)

## What I Observed
- Multiple login failures occurred within a short time
- All attempts were targeting the same user account
- The activity clearly indicated password guessing behavior

## Explanation
This type of activity is commonly seen in brute-force attacks where multiple passwords are tried to gain access. Wazuh detects this by monitoring authentication logs and highlighting repeated failures.
