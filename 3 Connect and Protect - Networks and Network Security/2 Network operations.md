## Network protocols

These describe the order of delivery and structure of data. Typical protocols used when accessing a website:

- TCP (Transmission Control Protocol): Establish comms using the handshake.
- ARP (Address Resolution Protocol): Determine MAC address of next destination.
- HTTPS (Hypertext Transfer Protocol Secure): The actual request & response, encrypted with SSL/TLS.
- DNS (Domain Name System): Convert URLs into IPs.

## Categories of network protocols

- Communication
  - ARP
  - TCP
  - UDP
  - HTTP(S)
  - DNS
  - SSH
  - Email
    - POP3 (Post office protocol)
    - IMAP (Internet message access protocol)
    - SMTP (Simple mail transfer protocol)
- Management
  - SNMP (used for monitoring & managing devices on network)
  - ICMP (used to communicate data transmission errors)
  - DHCP (used to configure devices)
- Security
  - HTTPS
  - SFTP

## IP addresses

- Private
  - 10.0.0.0-10.255.255.255
  - 172.16.0.0-172.31.255.255
  - 192.168.0.0-192.168.255.255
- Public
  - 1.0.0.0-9.255.255.255
  - 11.0.0.0-126.255.255.255
  - 128.0.0.0-172.15.255.255
  - 172.32.0.0-192.167.255.255
  - 192.169.0.0-233.255.255.255

## Common ports

- DHCP: UDP port 67 (servers) / UDP port 68 (clients)
- ARP: none
- Telnet: TCP port 23
- SSH: TCP port 22
- POP3: TCP/UDP port 110 (unencrypted) / TCP/UDP port 995 (encrypted, SSL/TLS)
- IMAP: TCP port 143 (unencrypted) / TCP port 993 (encrypted, SSL/TLS)
- SMTP: TCP/UDP Port 25 (unencrypted)
- SMTPS: TCP/UDP port 587 (encrypted, TLS)

## IEEE 802.11 (Wi-Fi)

- IEEE: Institute of Electrical and Electronics Engineers
- 802.11: Suite of protocols used in wireless comms

### Wi-Fi security

- WEP: Wired Equivalent Privacy, developed in 1999, mostly unused now.
- WPA: Wi-Fi Protected Access, developed in 2003, added better encryption (TKIP (Temporal Key Integrity Protocol)), integrity checks, but still has vulnerabilities.
- WPA2: Released in 2004, uses AES (Advanced Encryption Standard), CCMP (Counter Mode Cipher Block Chain Message Authentication Code Protocol(!)), is considered standard.
  - Personal: Suited for home networks, easy to implement, password needs to be entered on each device.
  - Enterprise: Suites for business networks, harder to implement, but more control over individual access and users don't access network key.
- WPA3: More secure, better encryption, still growing in usage.

## Firewalls

Network security device that monitors traffic to/from your network. Can include things like port filtering.

### Types

- Hardware firewall inspects each packet before it enters a network.
- Software firewall does the same thing, but is just installed on server / PC.
- Cloud-based firewall is a software firewall hosted in the cloud.

### States

- Stateful: Keeps track of data flowing through, proactively filters our threats.
- Stateless: Operated based on predefined rules, doesn't look or analyse information. Less secure.
- Next generation firewall (NGFW): Stateful, plus deep packet inspection, intrusion protection, connection with cloud-based threat intelligence services

## VPNs
- A network security service that changes your public IP address and hides your virtual location. Encrypts data, hides location, changes IP, encapsulates data, etc. - Encapsulation wraps sensitive data inside other data packets, that is then unwrapped at the other end.
- Remote access and site-to-site VPNs: Former typical for individual users and latter for enterpirises extending their network to other networks and locations. 

VPN protocols:

1. WireGuard: High speed, advanced encryption, designed to be simple to set up, newer, open source.
2. IPSec: More widely supported, more complex, but also more widely tested / adopted.

## Network segmentation

- Security zones: Segment of network protecting internal network from wider internet. E.g. untrusted guest wifi.
- Subnetworks: Network might have subnets to isolate departments etc.

### Security zones

- Uncontrolled zone: Any network outside org's control, e.g. internet.
- Controlled zone: Subnet that protects internal network from uncontrolled zones.
  - DMZ: Demilitarized zone, public facing services that can access the internet like web servers, DNS servers, proxy servers, email and file servers.
  - Internal network: Private internal-only servers and data.
  - Restricted zone: Highly confidential information only for certain employees.

Typically you'd have internet -> firewall -> DMZ -> firewall -> internal -> firewall -> restricted.

### Subnetting

- Subdivision of a network into logical groups called subnets

### CIDR

Classless Inter-Domain Routing, creating subnets by applying subnet masks to IP addresses. For example `198.51.100.0/24` = `198.51.100.0` - `198.51.100.255`.

## Proxy servers

A server that fulfils requests of a client by forwarding the request to other servers. Can be used to hide private network IP address. Uses temporary memory so, can also cache a little to reduce external contacts.

Types:

- Forward proxy: Regulates and restricts a user's access to the internet. Hides IP address and approves requests.
- Reverse proxy: Regulates and resticts the internet's access to an internal server.
- Email proxy: Filters spam emails by verifying sender's address. 

## Feedback

Continuing to ramp up the data density, great! The reading adds extra detail to the videos, and ensures people who prefer reading info (me) can learn.
