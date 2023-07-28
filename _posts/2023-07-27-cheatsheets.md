---
layout: post
title: cheatsheets
date: 2023-07-27 13:01 -0700
---

## BROWSER TOOLS:

* DNSDUMPSTER - my favorite dns tool.  
<https://dnsdumpster.com/>


* SHODAN - great for threat hunting and footprinting a target.  
<https://www.shodan.io/>


* CYBERCHEF - great tool when working with encoded data. download and run locally if handling sensitive data.  
<https://gchq.github.io/CyberChef>


* WHOIS - useful but i prefer to use the whois command from terminal.  
 <https://search.arin.net/>




## CMD CHEATSHEET:  

* Reverse DNS lookup  
```bash
dig -x 8.8.8.8 +short  
  dns.google  
```

* look up DNS records  
```bash
dig dns.google +nostats +nocomments +nocmd  
    ;dns.google.                    IN      A  
    dns.google.             0       IN      A       8.8.4.4  
    dns.google.             0       IN      A       8.8.8.8  
```

* Reverse a base64 string  
```bash
echo *base64_string* | pythom -m base64 -d  
```

* Nmap subnet scan  
scan results exported to a file called "out.txt". then filter out the online hosts and display in the terminal  
```bash
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
```

* use netcat to scan a range of ports on a host  
```bash
nc -z -v 178.79.152.114 1-100  
    nc: connect to 178.79.152.114 port 1 (tcp) failed: No route to host  
    nc: connect to 178.79.152.114 port 2 (tcp) failed: No route to host  
    nc: connect to 178.79.152.114 port 3 (tcp) failed: No route to host  
    nc: connect to 178.79.152.114 port 4 (tcp) failed: No route to host  
```

* `nslookup`  
if you just type `nslookup` and hit enter you will get the '>' prompt, you can now copy and paste a list of ip addresses to
get the respective dns quickly. You can also change which dns server is used to perform the lookup by typing “server”
followed by the new dns server IP.

* `ipcalc`  
– quick way to get the size of a subnet

* `whois`  
– Find out who owns a public IP

* `curl`  
