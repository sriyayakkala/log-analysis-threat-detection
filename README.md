 # Windows Event Log Analysis & Threat Detection Lab

## Project Overview
Simulated an end-to-end brute-force attack investigation on a Windows environment. Ingested raw security logs into a SIEM workflow to trace initial credential guessing, system entry, and post-exploitation persistence.

## Technical Scope & Event IDs
* Event ID 4625: Failed Logon (LogonType 10 = Remote Desktop / RDP)
* Event ID 4624: Successful Logon
* Event ID 4720: Local User Account Created (`backdoor_admin`)
* Event ID 4728: Account Added to Global/Local Security Group (`Administrators`)

## Detection Queries & Logic
### 1. Identify Brute-Force Spikes (SPL Logic)
`index=wineventlog EventCode=4625 | stats count BY src_ip, TargetUserName | where count > 3`

### 2. Confirm Compromise
Cross-referenced source IP `185.220.101.5` against successful Event ID 4624 logs to confirm breached access.

## Containment & Remediation Workflow
1. Isolate target host (`WIN-DC01`) from network segment.
2. Disable compromised `Administrator` account and purge unauthorized `backdoor_admin` account.
3. Block external source IP `185.220.101.5` at perimeter firewall.
4. Escalate incident report to Tier-2 IR team.
