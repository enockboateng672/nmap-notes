# Day 4 – Understanding Network Services

Today I focused on understanding the meaning of services discovered during Nmap scans. I learned that open ports are not just numbers, but represent actual programs (services) running on a system.

A port is a communication endpoint on a computer. It acts like a “door” into a system, and each port is associated with a specific service. Ports range from 1 to 65535.

A service is a program running on a system that listens on a port and responds to requests. For example, a web server runs on port 80 and a file server runs on port 21. This means that if a port is open, a service is running behind it.

There are three important port states. An open port means the service is active and reachable. A closed port means no service is running. A filtered port means the service may exist but access is blocked, usually by a firewall.

FTP (File Transfer Protocol) runs on port 21. It is used to transfer files between computers. A client connects to a server and files can be uploaded or downloaded. However, it can be insecure because it may allow anonymous login and sometimes sends credentials in plain text. This makes it a potential entry point if poorly configured.

HTTP (HyperText Transfer Protocol) runs on port 80 and is used to serve websites. A browser sends a request and the server responds with a webpage. This is one of the most important services because it is commonly targeted in attacks. It can be vulnerable to issues like SQL injection and cross-site scripting, and may expose sensitive data.

DNS (Domain Name System) runs on port 53. It is used to convert domain names into IP addresses. When a user enters a website name, DNS returns the corresponding IP address. It can sometimes leak useful information about a system and is used during reconnaissance.

MSRPC (Microsoft Remote Procedure Call) runs on port 135. It allows communication between Windows services. It helps identify that a system is running Windows and may expose system-level vulnerabilities.

RDP (Remote Desktop Protocol) runs on port 3389. It allows a user to remotely access a computer’s desktop. If login credentials are obtained, it gives full control of the system. Because of this, it is a major target for attackers, especially through brute-force attempts.

From this, I learned that each open port represents a running service, and each service is a potential entry point into a system. Some services are more important to focus on than others, especially HTTP and RDP.

I also learned that scanning alone is not enough. Understanding what each service does is what helps in deciding the next step during testing.

Now, when I see an open port, I ask myself what service is running, what it does, and whether it can be attacked.

This day helped me move from just running tools to actually understanding the results of a scan, which is important in cybersecurity.
