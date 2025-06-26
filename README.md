🔐 AWS Auto-Defense: Dynamic Threat Detection and Blocking System
📌 Overview
This project enhances security in AWS public cloud environments by developing an automated system that detects and blocks malicious access attempts in real-time. Using CloudWatch Logs, Python scripting, and Network Access Control Lists (ACLs), the system actively monitors activity and dynamically blocks attacker IPs to prevent brute-force, DoS, and resource exhaustion attacks.

🚀 Key Features
Real-time analysis of EC2 login attempts using AWS CloudWatch

Automatic IP extraction and blocking for unauthorized admin access

Dynamic rule updates in Network ACLs to neutralize threats

Tested using Hydra brute-force tool to simulate attacks

Seamless integration with AWS WAF, CloudWatch, and custom Python scripts

🛡️ How It Works
An EC2 instance is launched in a public subnet.

The instance is accessed using PuTTY for remote SSH login.

Hosting files are securely transferred from the local system to the EC2 instance using WinSCP.

If an attacker initiates a brute-force attempt (e.g., via Hydra):

Login attempts are logged in AWS CloudWatch.

A Python script monitors and analyzes these logs.

Upon detection of malicious patterns:

The attacker’s IP address is extracted.

A new Network ACL rule is dynamically added to block the IP.

This blocks further access attempts, mitigating potential damage.

🧰 Technologies Used
AWS CloudWatch – Centralized log monitoring

AWS WAF & Network ACLs – Security enforcement

Python – Automated log analysis and rule management

Hydra – Brute-force attack simulation

PuTTY – Secure remote access to EC2 instances

WinSCP – File transfer between local machine and cloud server
