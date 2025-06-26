# AWS-Public-Instance-Protection

🔐 AWS Auto-Defense: Dynamic Threat Detection and Blocking System
📌 Overview
This project aims to enhance security in AWS public cloud environments by developing an automated system that detects and blocks unauthorized access attempts in real-time. Using CloudWatch Logs, Python scripting, and Network Access Control Lists (ACLs), this system actively monitors activity and dynamically updates subnet rules to prevent threats like brute-force attacks and resource exhaustion.

🚀 Key Features
Real-time log analysis of EC2 instances using AWS CloudWatch

Automatic IP blocking for attackers attempting unauthorized admin access

Integration with Hydra attack simulation to test system robustness

Dynamic rule creation in Network ACLs to prevent future attack vectors

Leverages AWS WAF, CloudWatch, and Python scripts for automated mitigation

🛡️ How It Works
An EC2 instance is hosted in a public subnet.

If a brute-force tool (e.g., Hydra) is used to attempt unauthorized admin login:

Login attempts are captured and logged in AWS CloudWatch.

The logs are continuously monitored and analyzed using a Python script.

Upon detecting suspicious activity:

The attacker’s IP address is extracted.

A new Network ACL rule is dynamically created to block the IP.

This prevents further access attempts, reducing the risk of DoS attacks or resource abuse.

🧰 Technologies Used
AWS CloudWatch – Log collection and monitoring

AWS WAF & Network ACLs – Threat mitigation

Python – Scripting for log analysis and rule automation

Hydra – Attack simulation for testing
