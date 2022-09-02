---
title: "Networking"
---
# Network types
## PAN - Personal Area Network
Relatively short distance for communications e.g. Bluetooth, NFC, Zigbee
## LAN - Local Area Network
Typically restricted to one office or building
## WAN - Wide Area Network
Several LANs spread across the globe
## CAN - Campus Area Network
Several LANs spread across one campus
## CAN - Controller Area Network
Allow microcontrollers to communicate with each other without a host computer
## MAN - Metropolitan Area Network
Several LANs spanning a large area like a town
## Storage Area Network
High speed network of storage devices that can connect to other storage devices and servers

# Network topologies
![[Pasted image 20220711093651.png]]
## Bus topology
- Would use a "thicknet" backbone cable with "thinnet" cables running from the backbone to individual clients
- Thinnet was connected to thicknet via a T-piece connector
- Could only fit 30 devices maximum
### Images
![[Pasted image 20220711094328.png]]
![[Pasted image 20220711094522.png]]

# Cabling
![[Pasted image 20220711111353.png]]
![[Pasted image 20220711111513.png]]
# MAC addresses
- First half is the manufacturer ID, second half is the individual device ID
![[Pasted image 20220711105150.png]]
- MAC addresses don't have to be *completely* unique, as long as there's not more than one of the same on the same network it should be fine

- It is possible to change your MAC address to hide on a network as another device. You would receive a copy of every packet intended for the real device. Can also be used to get onto a network that uses MAC address filtering.
- Can bypass WiFi time restrictions.
# IP addresses
https://networkengineering.stackexchange.com/questions/5825/why-192-168-for-local-addresses

## IPv4
![[Pasted image 20220713111255.png]]

## IPv6
![[Pasted image 20220713131151.png]]
![[Pasted image 20220713115159.png]]
- Made up of 8 pairs of hexadecimal numbers
![[Pasted image 20220713130430.png]]
![[Pasted image 20220713130448.png]]
- A MAC address is made up of 6 pairs of hex numbers, an IPv6 address is made up of 8 pairs of hex numbers, so `ff:fe` is placed in the centre to make up the number of bits

# Address Resolution Protocol (ARP)
Standard method for finding a host's hardware (MAC) address based on its network layer (IP) address
# Sockets
- A socket is one endpoint of a 2-way communication link between 2 programs running on  a network
- A socket has a port number so that TCP/UDP can identify it
- Its a combination of a protocol, an IP address and a port number - `192.168.0.10:44`
![[Pasted image 20220715092513.png]]
# Ports
- Ports 0-1,023 are the System ports ("Well known range") e.g. 80, 443, 22 - most already in use
- Ports 1,024-49,151 are the User ports
- Ports 49,152-65,535 are the Dynamic ports - freely available to use, often picked randomly - the IANA range