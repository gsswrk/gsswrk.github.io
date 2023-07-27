---
layout: post
title: cheatsheets
date: 2023-07-27 13:01 -0700
---

<h2>BROWSER TOOLS:</h2>

- DNSDUMPSTER<br> <https://dnsdumpster.com/><br>
my favorite dns tool.  <br>

- SHODAN<br> <https://www.shodan.io/><br>
great for threat hunting and footprinting a target.<br>

- CYBERCHEF<br> <https://gchq.github.io/CyberChef><br>
great tool when working with encoded data. download and run locally if handling sensitive data.<br>

- WHOIS<br> <https://search.arin.net/><br>
useful but i prefer to use the whois command from terminal</p>


<h2>CMD CHEATSHEET:</h2>

<p><h4>reverse DNS lookup</h4>
&nbsp;dig -x 8.8.8.8 +short<br>
&nbsp;response: dns.google</p>

<p><h4>look up DNS records</h4>
&nbsp;&nbsp;dig dns.google +nostats +nocomments +nocmd<br>
&nbsp;&nbsp;&nbsp;&nbsp;;dns.google.                    IN      A<br>
&nbsp;&nbsp;&nbsp;&nbsp;dns.google.             0       IN      A       8.8.4.4<br>
&nbsp;&nbsp;&nbsp;&nbsp;dns.google.             0       IN      A       8.8.8.8</p>

<p><h4>Reverse a base64 string</h4>
&nbsp;echo *base64_string* | pythom -m base64 -d</p>

<p><h4>Nmap subnet scan</h4>
scan results exported to a file called "out.txt". then filter out the online hosts and display in the terminal<br>
&nbsp;&nbsp;nmap -sn -oG out.txt 192.168.1.0/24 && grep -i up out.txt<br>
&nbsp;&nbsp;&nbsp;&nbsp;Host: 192.168.1.1 ()    Status: Up<br>
&nbsp;&nbsp;&nbsp;&nbsp;Host: 192.168.1.2 ()    Status: Up<br>
&nbsp;&nbsp;&nbsp;&nbsp;Host: 192.168.1.9 ()    Status: Up<br>
&nbsp;&nbsp;&nbsp;&nbsp;Host: 192.168.1.18 ()   Status: Up<br>
&nbsp;&nbsp;&nbsp;&nbsp;Host: 192.168.1.24 ()   Status: Up<br>
&nbsp;&nbsp;&nbsp;&nbsp;Host: 192.168.1.26 ()   Status: Up<br>
&nbsp;&nbsp;&nbsp;&nbsp;Host: 192.168.1.28 ()   Status: Up<br>
&nbsp;&nbsp;&nbsp;&nbsp;Host: 192.168.1.29 ()   Status: Up<br>
&nbsp;&nbsp;&nbsp;&nbsp;Host: 192.168.1.38 ()   Status: Up<br>
&nbsp;&nbsp;&nbsp;&nbsp;Host: 192.168.1.57 ()   Status: Up<br>
&nbsp;&nbsp;&nbsp;&nbsp;Host: 192.168.1.69 ()   Status: Up<br>
&nbsp;&nbsp;&nbsp;&nbsp;Host: 192.168.1.79 ()   Status: Up<br>
&nbsp;&nbsp;&nbsp;&nbsp;Host: 192.168.1.82 ()   Status: Up</p>

<p><h4>use netcat to scan a range of ports on a host</h4>
&nbsp;&nbsp;nc -z -v 178.79.152.114 1-100<br>
&nbsp;&nbsp;&nbsp;&nbsp;nc: connect to 178.79.152.114 port 1 (tcp) failed: No route to host<br>
&nbsp;&nbsp;&nbsp;&nbsp;nc: connect to 178.79.152.114 port 2 (tcp) failed: No route to host<br>
&nbsp;&nbsp;&nbsp;&nbsp;nc: connect to 178.79.152.114 port 3 (tcp) failed: No route to host<br>
&nbsp;&nbsp;&nbsp;&nbsp;nc: connect to 178.79.152.114 port 4 (tcp) failed: No route to host</p>

<p><h4>nslookup</h4>
if you just type "nslookup" and hit enter you will get the '>' prompt, you can now copy and paste a list of ip addresses to
get the respective dns quickly. You can also change which dns server is used to perform the lookup by typing “server”
followed by the new dns server IP.</p>

<h4>ipcalc</h4>
– quick way to find out what’s in a subnet

<h4>nmap</h4>
– get info about host and check if ports are open

<h4>dig</h4>
– Get reverse dns record

<h4>nc</h4>
– quick and easy way to see if a port is accepting connections or being blocked

<h4>curl</h4>
– these flags means that it will ignore SSL cert issues, follow redirects and send the verbose output to a file called “output.txt” for later review.

<h4>wget</h4>
– Good for pulling files from remote locations. Can also be an alternative to curl.

<h4>whois</h4>
– Find out who owns a public IP
