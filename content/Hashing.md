---
title: "Hashing"
---
Themes: [[Cryptography]], 

# Hashing
- Hashes map data of any size to data of fixed size
- Input is the "message"
- Output is the "digest"

True cryptographic hashes cannot be inverted
- Cannot recover data from a hash
- Cannot modify message without altering the digest
- Two different messages can't create the same digest (no collisions)

# Collision example
With MD5 these two images have the same hash: `253dd04e87492e4fc3471de5e776bc3d`
![ship|500](https://s3-eu-west-1.amazonaws.com/md5collisions/ship.jpg)
![plane|500](https://s3-eu-west-1.amazonaws.com/md5collisions/plane.jpg)
