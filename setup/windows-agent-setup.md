# Wazuh Windows Agent Setup

## Step 1: Add Agent in Wazuh Dashboard
1. Open the Wazuh Dashboard.
2. Navigate to **Agents**.
3. Click on **Add Agent**.
4. Select **Windows**.
5. Fill in the required details:
   - Wazuh Server Address (IP or hostname)
   - Agent Name
   - Optional settings if required
6. Once all the details are filled, there is no separate Save button.  
  
After adding the details, the dashboard will generate:
- An installation command (Invoke-WebRequest)
- A command to start the agent service

![wazuh](https://github.com/akshaysapkal-cyber/Wazuh-SIEM-Lab-Detection/blob/main/Screenshots/wazuh/Wazuh%20Agent%20config.png?raw=true)

## Step 2: Install Wazuh Agent Using Generated Command
1. Copy the installation command provided in the dashboard.
2. Open **PowerShell as Administrator** on the target Windows system.
3. Paste and execute the command.

This command will:
- Download the Wazuh agent (.msi)
- Install the agent
- Automatically configure it with the provided server details

![invoke](https://github.com/akshaysapkal-cyber/Wazuh-SIEM-Lab-Detection/blob/main/Screenshots/wazuh/Wazuh%20invoke.png?raw=true)

## Step 3: Start the Wazuh Agent Service

After installation, run the following command in PowerShell:

```powershell
NET START Wazuh Svc  
```
![net start](https://github.com/akshaysapkal-cyber/Wazuh-SIEM-Lab-Detection/blob/main/Screenshots/wazuh/wazuh%20net%20start.png?raw=true)
