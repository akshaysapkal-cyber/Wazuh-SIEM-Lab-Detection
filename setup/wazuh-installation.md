# Wazuh Installation (Ubuntu)

## Step 1: Update System
``` sudo apt update ``` 
``` sudo apt upgrade ```
Updates system packages to the latest version.
## Step 2: Download Wazuh Installation Script
``` curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh ```
Downloads the official Wazuh installation script.
![download wazuh with curl](https://github.com/akshaysapkal-cyber/Wazuh-SOC-Lab-Detection/blob/main/Screenshots/Installation/curl%20download%20wazuh.png?raw=true)

## Step 3: Install Wazuh
``` sudo bash wazuh-install.sh -a ```
Installs Wazuh manager, indexer, and dashboard.

## Step 4: Get Login Credentials
After installation, credentials will be displayed in the terminal.
Saves the username and password for dashboard login.

![Credential](https://github.com/akshaysapkal-cyber/Wazuh-SOC-Lab-Detection/blob/main/Screenshots/Installation/wazuh%20installed.png?raw=true)

## Step 5: Access Wazuh Dashboard
Open browser and visit:
```
https://<Ubuntu-IP>
```
Opens the Wazuh web interface.

## Step 6: Login to Dashboard
- Username: admin
- Password: (from installation output)

Access the Wazuh dashboard.

![Dashboard wazuh](https://github.com/akshaysapkal-cyber/Wazuh-SOC-Lab-Detection/blob/main/Screenshots/Installation/wazuh%20ui.png?raw=true)
