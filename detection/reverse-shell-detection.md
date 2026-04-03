# Reverse Shell Detection

## Objective
- To identify suspicious activity indicating remote access to the target system.

## Detection
After executing the payload on the Windows machine, a connection was established back to the Kali system. This activity was captured by Wazuh as suspicious process execution and network behavior.

## Where to Check
- Open Wazuh Dashboard
- Go to **Security Events / Discover**
- Look for events related to PowerShell, unusual processes, or outbound connections

![reverseshell](https://github.com/akshaysapkal-cyber/Wazuh-SIEM-Lab-Detection/blob/main/Screenshots/detection/Reverse%20Shell.png?raw=true)

## What I Observed
- A new process was executed on the Windows system
- The system initiated an outbound connection to the attacker machine
- This behavior was not normal for regular system activity

## Explanation
This indicates a reverse shell, where the target system connects back to the attacker and provides remote access. Such activity is a strong indicator of system compromise.

Wazuh helps detect this by monitoring process execution and unusual network connections.

This activity may require immediate investigation as it indicates possible unauthorized access.
