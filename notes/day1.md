# Day 1 - Learning Nmap

Today I practiced using Nmap to scan my own machine (127.0.0.1) to understand how port scanning works.

## What I did
I ran:
- nmap 127.0.0.1
- nmap -sV 127.0.0.1
- nmap -p- 127.0.0.1

## What I found
All the ports I scanned were closed.

- The basic scan checked 1000 common ports → all closed
- The full scan checked all 65535 ports → all closed
- No services were detected

## What this means
Since all ports are closed, there are no services running on my machine that are accessible over the network.

This means:
- No entry points for network attacks
- The system has a very small attack surface

## What I learned
- Nmap is used to discover open ports and services
- Open ports = possible entry points
- Closed ports = nothing is listening
- The -sV flag only works when ports are open
- The -p- flag is useful to check all ports, not just common ones

## My thoughts
At first I expected to see open ports like SSH or HTTP, but my system had none. This showed me that scanning localhost is safe but not always useful for finding vulnerabilities.

## Next step
I need to scan a real machine with active services to see meaningful results.
