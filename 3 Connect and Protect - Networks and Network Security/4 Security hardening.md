## Overview

Security hardening: Strengthening a system to reduce its vulnerabilty and attack surface.
Attack surface: All the potential vulnerabilities.

Conducted on:
- Hardware
- OS
- Applications
- Networks
- Databases
- Physical space

Examples of hardening procedures are:
- Patches(software updates)
- Device/app configuration changes
- Disabling unused apps/services
- Reducing access permissions
- Regular penetration testing 

## OS hardening

- OS refers to the interface between computer hardware and the user

### OS hardening practices

Regular interval tasks:

- Patch updates
- Hardware and software disposal
- Delete unused software apps
- Backups

One-off(updated as needed):

- Secure encryption
- Strong password policy

### Baseline configuration

> A baseline configuration is a documented set of specifications within a system that is used as a basis for future builds, releases, and updates.

## Brute Force Attacks 

- Trial-and-error process of discovering private information
- Types:
  - Simple brute force attacks: guess log-in credentials
  - Dictionary attacks: list of commonly used passwords and stolen credentials from previous breaches
    
### Assessing Vulnerabilities 

- Virtual Machines: Testing and exploring apps virtually
- Sandbox environments:Testing environments that allow execution separate from your network i.e. testing patches, identifying and addressing bugs, detecting vulnerabilities
  
### Preventing brute force attacks

- Salting & hashing
- MFA / 2FA
- CAPTCHA / reCAPTCHA
- Strong password policies

## Network hardening

Regular interval tasks:

- Firewall rule maintenance
- Network log analysis
- Patch updates
- Server backups

One-off:

- Port filtering on firewalls
- Network access privileges
- Network segmentation i.e. Using isolated subnets / security zones
- Encryption usinglatest standards

### Devices to Secure Network

- Firewalls (stateless, stateful, next generation) 
- Intrusion detection system (IDS): Monitors traffic, alerts to possible intrusion.
- Intrusion prevention system (IPS): Monitors traffic, actively stops the activity.
- Full packet capture devices
- SIEM system: Collects and analyses (aggregated) log data i.e. Chronicle, Splunk

## Cloud hardening

Considerations:

- Identity access management (IAM): managing digital identities / authorisations.
- Configuration
- Attack surface
- Zero-day attacks
- Visibility & tracking i.e. network admin, flow logs & tools like packet mirroring

Shared responsibility model:

- CSPs responsible for securing cloud infrastructure i.e. data centers, hypervisors, host operating systems
- Clients responsible assets and processes stored and operated on cloud i.e. service configurations

Hardening techniques:

- IAM
- Hypervisors
  - Type 1 runs on host computer hardware, usually used by cloud service providers.
  - Type 2 runs on host computer software.
- Baselining
- Cryptography
- Cryptographic erasure i.e. crypto shredding
- Key management 
