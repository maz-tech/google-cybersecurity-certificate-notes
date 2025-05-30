## Types of attack

### Network interception attacks

- Intercept network traffic and steal information, or interfere with transmission 
- e.g. packet sniffing: use of hardware or software to capture and inspect data

### Backdoor attacks

- Weaknesses intentionally left by programmers snf sys/network admins that bypass access control mechanisms, or installed by a hacker after the initial intrusion.

## Possible impacts on an org

- Financial (loss of revenue, reparation costs, litigation/settlment costs, fines)
- Reputation
- Public safety (e.g. government hacked)

## Dos Attacks

- Flooding network or server with network traffic
- DDOS: Uses mutliple devices or servers in diff locations to flood network

## Common DoS attacks

- SYN flood attack: Simulates lots of initial "synchronise" packets from the TCP/IP handshake, using up all the ports on the server. Simulates a TCP connection and floods server with SYN packets
- ICMP, Internet Control Message Protocol, flood attack (status update protocol): Repeatedly send ICMP packets to server, server has to respond to all.
- Ping of death: Sending a device/system a malformed/oversized packet (especially ICMP) can cause a server to crash. Hacker sends a system an ICMP packet that is bigger than 64KB.

## Network protocol analyser

- AKA Packet Sniffer/ Packet Analyser
- A tool designed to capture and analyse data within a network
- Examples:
  - SolarWinds NetFlow Traffic Analyzer
  - ManageEngine OpManager
  - Azure Network Watcher
  - Wireshark
  - tcpdump

### tcpdump

-  command-line network protocol analyzer.
-  Low memory, low CPU, opensource library
-  Textbased, Linux and macOS compatible
-  Prints info on each packet i.e timestamp, source IP & port, destination IP & port
  ![image](https://github.com/user-attachments/assets/a06ea55f-2d49-4784-b051-e6c57bf37da9)
- Uses: establish baseline, detect & id malicious traffic, create customised alerts, locate unauthorised instant messaging, traffic, or WAPs
- Used maliciously to gain info
  
## Network Attack Tactics & Defense
### Packet sniffing

- Malicious actors may use sofware apps or hardware devices to look into data packets
- Passive: Data packets read in transit.
- Active: Data packets manipulated in transit.
- VPN / HTTPS protects from this.

### IP spoofing

- An attacker changes the source IP of a data packet to impersonate an authorized system and gain access to a network.
- Common attacks:
  - On-path attack: Malicious actor places themselves in the middle, and intercepts/alters data. AKA Man-in-the-middle attack
  - Replay attack: Malicious actor intercepts and delays/repeats a data packet another time.
  - Smurf attack: Combination of DDoS and Spoofing attack. An attacker sniffs an authorised user's IP address and floods it with packets.
- Defense:
  -   Encryption i.e. using TLS
  -   Firewalls
