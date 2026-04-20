## Day 1 - Nmap Basics

## Objective
To understand how to use Nmap to discover open ports and identify services running on a system.

## Commands Used
- nmap 127.0.0.1
- nmap -sV 127.0.0.1
- nmap -p- 127.0.0.1

## Explanation of Commands
- Basic scan (nmap): Identifies open ports on the target system.
- -sV: Detects the version of services running on open ports.
- -p-: Scans all 65535 ports instead of the default top ports.

## Observations and Analysis
- Port 22 is open and running SSH, which allows remote access to the system. This can be a target for brute-force attacks or exploitation if weak credentials or vulnerabilities exist.
- Port 80 is open and running HTTP, meaning a web server is active. This could expose web applications that may be vulnerable to attacks such as SQL injection or cross-site scripting (XSS).

## Key Takeaways
- Open ports represent possible entry points into a system.
- Service detection helps identify what is running behind each port.
- Full port scanning can reveal services that are not found in default scans.

## Next Steps
- Learn how to identify vulnerabilities in detected services.
- Practice scanning other machines in a controlled lab environment.
