##DISCOVER AND UNDERSTAND SERVICES ON A TARGET MACHINE

##Task 1
nmap- tool/program
-Pn - tell the tool to ignore ping, scan anyway
-oN - tells where to save the scans

After the first scan using nmap -Pn <ip>, it gave me 1000 filtered tcp ports telling me packets were dropped so couldnt determine state of ports.

##Task 2
I tried to scan all the ports using 
nmap -Pn -p- <ip> which is a full scan and takes very long but it took much longer than it should and i found out there was a probem not with the machine but my kali wasnt connecting to the tryhackme machine via the vpn

i tried out with nmap -Pn -T4 --top-1000 <ip> for a smart scan and it still gave me filtered tcp ports confirming my theory so i checked with ifconfig tun0 and it gave me the ip of my system rather instead of the ip of the tryhackme vpn
so reaching the machine was not possible, so i will configure it well on my next try so it works well.

