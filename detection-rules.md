# Detection Logic (Basic SIEM Rules)

#Rule 1: Brute Force Detection
IF:
- 3 or more failed login attempts  
- From same IP  
- Within short time  

THEN:
- Trigger alert: "Possible Brute Force Attack"
  
#Rule 2: Suspicious Login Success
IF:
- Multiple failed logins  
- Followed by successful login  

THEN:
- Trigger alert: "Compromised Account Risk"
