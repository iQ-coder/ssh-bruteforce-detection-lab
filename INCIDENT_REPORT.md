⚠️ This project was conducted in a controlled lab environment for educational and defensive security learning purposes only.




Incident ID

IR-SSH-001

Date

(Local lab simulation)

Environment

Attacker Machine: Kali Linux

Target Machine: Ubuntu Linux

Network: Isolated virtual lab

summary 
This incident report documents a simulated SSH brute-force attack conducted in a controlled laboratory environment. The purpose of this exercise was to analyze attacker behavior, identify detection indicators, and evaluate defensive controls related to SSH access.

Attack Vector

Service targeted: SSH (Port 22)

Attack type: Password brute-force

Tool used: Hydra (educational lab use)

 Time line of events 

 T0          Network connectivity verified via ICMP
 T1          Open ports identified using network scanning
 T2          Repeated SSH authentication failures observed
 T3          Successful login achieved due to weak credentials
 T4          Unauthorized system modifications performed
 T5          Logs reviewed and mitigation steps applied

Indicators of Compromise (IOCs)

Multiple failed SSH login attempts

Repeated authentication failures from a single IP

High-frequency login attempts in a short time window

Successful login following repeated failures




Evidence Collected

/var/log/auth.log showing failed and successful SSH logins

Network scan results identifying exposed services

Firewall configuration changes used for mitigation




Impact Assessment

Unauthorized access to system resources

Potential compromise of service integrity

Risk of service disruption or malicious persistence

Elevated privileges increase overall attack severity

Root Cause

Weak password-based SSH authentication

SSH service exposed to all network IP addresses

Lack of brute-force prevention mechanisms


Mitigation & Remediation

Restricted SSH access using UFW firewall rules

Limited SSH access to trusted IP addresses

Recommended disabling password authentication

Recommended use of SSH key-based authentication

Recommended deployment of Fail2Ban for brute-force prevention




Lessons Learned

Brute-force attacks are noisy and detectable

Log monitoring is critical for early detection

Defense-in-depth significantly reduces attack success

SSH hardening is essential for system security
