---
title: "Dark Web"
---
Themes: [[Networking]], 

# Dark Web
## The web has *layers*
![Pasted image 20220721091415.png](images/Pasted%20image%2020220721091415.png)
- The surface is indexed sites that can be found by search engines
- The deep web is the sites that aren't indexed by search engines, much larger than the surface web
- The bottom is parts of the internet that require specific software to access
![Pasted image 20220721091912.png](images/Pasted%20image%2020220721091912.png)

## Onion Routing
![Pasted image 20220721092943.png](images/Pasted%20image%2020220721092943.png)
- Data is protected with multiple layers of encryption, like an onion
### The Onion Routing Project (TOR)
- Tor is just the technology behind the dark web
- The TOR browser is the most popular browser used to access the dark web

- The Tor client will pick a random path to the destination server, this is so the route through the network is different every time - hard to track, not impossible though
- The network can be exploited to deanonymize users, but this is very costly to carry out

- The first node that you travel through can see your real IP (unless using a VPN), but the data is encrypted so they can't see what you are doing
- The site can see the data but the client paths through at least 3 nodes so it can't see your real IP address, if the site doesn't care about anonymity (like Facebook) they won't go through 3 nodes
- Anywhere in the middle can't see either

### Dark web sites (Tor hidden services)
- The service has no knowledge of the IP address of any visitor
- Visitors have no idea of the IP address
- Tor sites have a `.onion` domain extension and often have obfuscated addresses `tnhafie5wfu6qjby2ucxiedh.onion`
- The addresses are generated from the key used to encrypt the site

![Pasted image 20220721095800.png](images/Pasted%20image%2020220721095800.png)

Hosting a site on Tor is much cheaper than on the clearnet because you don't need to buy a domain, you can also host the site personally because your IP address is anonymous

v3 onion addresses are 56 characters long which are harder to brute force than v2 (16 characters)

### Tor bridges
- Bridges are a workaround for when your ISP blocks Tor
- Could use a VPN instead but the Tor network is slow enough as it is so it can become unusable
> "Generally speaking, we don't recommend using a VPN with Tor unless you're an advanced user who knows how to configure both in a way that doesn't compromise your privacy - Tor FAQs"

### Options for accessing Tor
![Pasted image 20220721101713.png](images/Pasted%20image%2020220721101713.png)
TAILS is anti-forensic, the moment you power the system down, all traces of it are gone, all data is tunnelled through Tor. Using it on a USB will leave no footprint

### Decentralisation
Tor is meant to be and is very decentralised however in terms of the geographical location of nodes, many of them are in Europe. Many of the European nodes are using the same ISP

# Resources
- https://en.wikipedia.org/wiki/Clearnet_%28networking%29
- https://www.worldwidewebsize.com/
- https://paste.sr.ht/~sircmpwn/13c1951014a256e9f551296a129bf6d10e9303dc
- https://thehiddenwiki.org/
- https://blog.torproject.org/v2-deprecation-timeline/
- https://www.reddit.com/r/TOR/comments/bxzdh1/onion_v2_vs_v3/
- https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN
- https://tormap.void.gr/
- https://torflow.uncharted.software/
- foxacid
- egotistical giraffe
- ed25519
- https://en.wikipedia.org/wiki/Freenet
- https://en.wikipedia.org/wiki/Usenet



- anarchist's cookbook - **ILLEGAL**
- https://en.wikipedia.org/wiki/The_Anarchist_Cookbook
- https://en.wikipedia.org/wiki/List_of_books_banned_by_governments
- https://en.wikipedia.org/wiki/Rights_of_Man
