---
title: "DNS"
---
Themes: [[Networking]], 

# DNS
DNS is like the phone book of the internet, it resolves IP addresses into human-readable domain names.

Invented by [[Paul Mockapetris]]

![[Pasted image 20220713091157.png]]
Starts at the end of a domain and works its way forward through the domain extension levels

![[Pasted image 20220713091314.png]]
Different companies are responsible for different parts of the domain

![[Pasted image 20220713092054.png]]
*How a domain is resolved*

The more domain names there are, the slower the process gets, the server companies need to add more servers and distribute the load to keep speeds up

# Threats
- The integrity of DNS records is extremely important
- [[DDoS]] attacks on the networks or server hardware could take down a domain server
- BGP (Border Gateway Protocol) is a critical system - Facebook went down due to a problem with BGP

Resources
- https://en.wikipedia.org/wiki/Paul_Mockapetris
- https://www.iana.org/domains/root/servers
- https://root-servers.org/