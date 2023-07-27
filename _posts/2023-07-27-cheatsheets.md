---
layout: post
title: cheatsheets
date: 2023-07-27 13:01 -0700
---

BROWSER TOOLS:
- DNSDUMPSTER – https://dnsdumpster.com/
my favorite dns tool.  
- SHODAN - https://www.shodan.io/
great for threat hunting and footprinting a target.
- CYBERCHEF - gchq.github.io/CyberChef
great tool when working with encoded data. download and run locally if handling sensitive data.
- WHOIS - https://search.arin.net/
useful but i prefer to use the whois command from terminal


CMD CHEATSHEET:

<p>reverse DNS lookup<br>
  dig -x 8.8.8.8 +short<br>
  response: dns.google</p>

<p>look up DNS records<br>
  dig dns.google +nostats +nocomments +nocmd<br>
    ;dns.google.                    IN      A<br>
    dns.google.             0       IN      A       8.8.4.4<br>
    dns.google.             0       IN      A       8.8.8.8</p>

  Quick way to reverse a base64 string
    ECHO *BASE64_STRING* | PYTHOM -M BASE64 -D

  subnet scan results exported to a file called "out.txt". then filter out the online hosts and display in the terminal 
    nmap -sn -oG out.txt 192.168.1.0/24 && grep -i up out.txt
      Host: 192.168.1.1 ()    Status: Up
      Host: 192.168.1.2 ()    Status: Up
      Host: 192.168.1.9 ()    Status: Up
      Host: 192.168.1.18 ()   Status: Up
      Host: 192.168.1.24 ()   Status: Up
      Host: 192.168.1.26 ()   Status: Up
      Host: 192.168.1.28 ()   Status: Up
      Host: 192.168.1.29 ()   Status: Up
      Host: 192.168.1.38 ()   Status: Up
      Host: 192.168.1.57 ()   Status: Up
      Host: 192.168.1.69 ()   Status: Up
      Host: 192.168.1.79 ()   Status: Up
      Host: 192.168.1.82 ()   Status: Up

  use netcat to scan a range of ports on a host  
    nc -z -v 178.79.152.114 1-100
      nc: connect to 178.79.152.114 port 1 (tcp) failed: No route to host
      nc: connect to 178.79.152.114 port 2 (tcp) failed: No route to host
      nc: connect to 178.79.152.114 port 3 (tcp) failed: No route to host
      nc: connect to 178.79.152.114 port 4 (tcp) failed: No route to host

  nslookup
    if you just type "nslookup" and hit enter you will get the '>' prompt, you can now copy and paste a list of ip addresses to get the respective dns quickly. You can also change which dns server is used to perform the lookup by typing “server” followed by the new dns server IP.

IPCALC – quick way to find out what’s in a subnet

NMAP – get info about host and check if ports are open

DIG – Get reverse dns record

NC – quick and easy way to see if a port is accepting connections or being blocked

CURL – these flags means that it will ignore SSL cert issues, follow redirects and send the verbose output to a file called “output.txt” for later review.

WGET – Good for pulling files from remote locations. Can also be an alternative to curl.

WHOIS – Find out who owns a public IP


