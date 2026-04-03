# Windows Agent Setup

## Step 1: Add Agent in Wazuh Dashboard
- Go to **Agents**
- Click **Add Agent**
- Select **Windows**
- Enter Wazuh server IP

Registers a new Windows agent in Wazuh.

(Add screenshot: agent creation screen)

## Step 2: Download Wazuh Agent
Download the Windows agent (.msi) from the Wazuh dashboard.
Downloads the agent installer for Windows.
<pre>https://packages.wazuh.com/4.x/windows/wazuh-agent-4.7.0-1.msi</pre>
(Add screenshot: download option)

## Step 3: Install Agent on Windows
- Run the downloaded .msi file
- Enter Wazuh server IP when prompted
- Complete installation

Installs Wazuh agent on the target system.

(Add screenshot: installation process)

## Step 4: Start Agent Service
```bash
net start wazuh
```
Starts the Wazuh agent service on Windows.

(Add screenshot: service started)

## Step 5: Verify Agent Connection

- Go back to Wazuh dashboard
- Check agent status → Active

Confirms the agent is successfully connected.

(Add screenshot: agent active status)

---
