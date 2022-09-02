---
title: "DNS and Network Configurations"
---
Themes: [[Networking]], 

# DNS and Network Configurations

## DNS (Domain Name System)
- Internet devices have an IP address for an identifier e.g. `142.250.178.14`.
- IP addresses are hard to remember so we have hostnames e.g.
- `www.google.com`.
- DNS maps an IP address to a hostname, its like a phone book that maps phone numbers to business names.

- One hostname can have many IP addresses to distribute the load to multiple servers. E.g. having servers in multiple countries for lower latency and "decentralisation". 

- DNS is fairly decentralised so there's not one single point of failure.

- DNS is distributed to multiple servers that may control a separate TLD each. E.g. one for `.com`, one for `.org`, one for `.edu` etc.
- There are multiple levels, `www.bbc.co.uk` would go `uk->co`.
![Pasted image 20220228112603.png](Pasted%20image%2020220228112603.png)

- `www.` is just an identifier so people know that a hostname is for a website, it isn't actually needed when searching a URL.

## The Internet
The internet is a group of interconnected networks spanning the globe.
