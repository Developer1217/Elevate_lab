Task-4
Setup and Use a Firewall on Windows/Linux

🔐 Firewall Configuration on Windows & Linux
Welcome to the Firewall Configuration Project where I demonstrate how to use firewall tools in Linux (UFW) and Windows Defender Firewall to control network traffic with basic rules such as blocking or allowing specific ports.

🎯 Objective
Configure a firewall on both Linux and Windows
Block and allow specific ports (e.g., block Telnet port 23, allow SSH port 22)
Test the applied firewall rules
Understand how a firewall filters traffic
🛠 Tools Used
Platform	Tool
Linux	UFW (Uncomplicated Firewall)
Windows	Windows Defender Firewall
Both	Telnet Client (for testing)

Step 1: Open Firewall Configuration Tool

Option 1 (GUI):

Press Win + R → type control → Enter.

Go to System and Security → Windows Defender Firewall.

Click “Advanced settings” on the left.
This opens the Windows Firewall with Advanced Security window.

Option 2 (Command Line):

Open Command Prompt as Administrator
(Start → type "cmd" → right-click → Run as administrator)

Use netsh commands.

Step 2: List Current Firewall Rules

Run in Command Prompt (Admin):

netsh advfirewall firewall show rule name=all


This lists all inbound and outbound rules.

Step 3: Block Inbound Traffic on Port 23 (Telnet)

To block inbound Telnet connections, run:

netsh advfirewall firewall add rule name="Block Telnet" dir=in action=block protocol=TCP localport=23


✅ This rule prevents anyone from connecting to your system on port 23.

Step 4: Test the Rule

You can test locally or from another machine:

Try connecting using Telnet:

telnet 127.0.0.1 23


You should see “Connecting To 127.0.0.1...Could not open connection” (blocked).

Step 5: (Optional for Linux Only — skip in Windows)
Step 6: Remove the Test Rule

To restore the original state:

netsh advfirewall firewall delete rule name="Block Telnet"


##🗒️ Additional Notes
firewall_commands.txt contains all Linux commands used.
All screenshots are labeled clearly and sorted into folders.
This project helps develop basic firewall management skills and network security understanding.
