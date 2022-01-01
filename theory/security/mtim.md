# types of attacks

## MITM

- intervention between two parties
- message is intercepted and passed as authenticated

- passive &/or active

## Notable attacks

- belkin 2003,
  - router firmware impersonated the server in order to present the end user with an ad

- DigiNotar, 03/09/2011
  - dutch certificate authority for the dutch government was breached in order to forge certificates**
  - target was 300k iranian gmail accounts
  - DigiNotar certs were blacklisted and the company bankrupted

- lenovo superfish, 2014
  - similar to the belkin mitm where preloaded application injected ads into the browser

## types

### Active
  
- masquerade
- message tampering
- repudiation
- replay

#### denial of service

##### volume based attacks

- udp flood
  - user datagram protocol
  - can overwhelm a firewall
  - steps:
    - server checks for ports listening
    - if no ports are available, a ICMP port is sent to notify that the dest was unreachable
  - this attack can crowd, block real requests
  - real requests can get filtered out in the noise
  - source ip is typically spoofed

  - mitigation:
    - limit the ICMP packet rate
    - server-level mitigation can't fix bottlenecks from a saturated firewall state table

- spoofed packet flood
- ICMP flood, aka ping flood

##### protocol attacs

- SYN flood
- fragmented packet attacks
- ping of death
- smurf DDos

- ARP cache poisoning
- DNS cache poisoning

### Passive

- release of messages

### traffic analysis

- wifi eavesdropping

### hijacking

- email
- session

### spoofing

- ip
- dns
- https

- ssl stripping

----

## glossary

- firewall state table
  - a table used by stateful firewalls to analyze traffic
  - compares current and previous traffic
  - records the following
    - tcp streams
    - udp datagrams
    - icmp messages
  - can apply a status/state
  - also known as dynamic packet filetering
  - streamlines allowed packet streams to increase efficiancy
  - keepalive messages are sent to maintain the state (session?)

- public key certificate

  - en.wikipedia.org/wiki/Public_key_certificate
  - electronic doc proving ownership of a pubkey
  - used in email encryption, code signing, e-signature systems

  -

## trust models

- Chain of trust
  - a schema which assumes trust based on the validation of multiple components or steps

- Web of trust
  - used in PGP, GnuPG, OpenPGP
  - establishes authenticity of the id/pubkey bind
  - decentralized trust model
  - 1992, phil zimmermann
  - this requires emergence, or a large number of authenticated interactions between users to validate cert binds
  - en.wikipedia.org/wiki/Web_of_trust