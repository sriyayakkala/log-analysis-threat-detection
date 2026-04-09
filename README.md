# log-analysis-threat-detection
Basic log analysis project to identify suspicious login activity and brute force attacks
# Log Analysis & Threat Detection (SOC Mini Project)

# Overview
This project demonstrates basic Security Operations Center (SOC) skills by analyzing authentication logs to detect suspicious activities such as failed login attempts and brute force attacks.

# Objective
- Identify failed and successful login patterns  
- Detect brute force attack behavior  
- Understand how SIEM tools correlate logs and generate alerts  

# Analysis Performed

### 1. Failed Login Detection
- Multiple failed login attempts were observed for user **admin**
- Repeated failures from the same IP indicate suspicious activity

### 2. Brute Force Pattern Identification
- Rapid sequence of failed logins followed by success
- This suggests a **possible brute force attack**

### 3. Suspicious Login Behavior
- Successful login after multiple failures is a red flag
- Requires further investigation in real SOC environments
  
# SOC Concepts Applied
- Log analysis  
- Event correlation  
- Alert triage  
- Incident identification
  
# Conclusion
The analysis shows how repeated failed login attempts can indicate a brute force attack. In a real SOC environment, this activity would trigger alerts and require escalation for further investigation.

# Learning Outcome
- Improved understanding of authentication logs  
- Gained hands-on experience in detecting suspicious patterns  
- Learned basic SOC workflow for incident detection  
