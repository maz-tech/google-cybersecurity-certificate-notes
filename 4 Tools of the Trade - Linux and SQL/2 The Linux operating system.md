## History

- UNIX OS was already in use.
- Linux Torvalds working on Linux kernel, wanted to improve it, make it open source, more accessible.
- Richard Stallman working on GNU, OS based on UNIX.
- Combined efforts made Linux.

## Factoids

- Linux licensed under GNU public license.
- Over 600 distributions developed, each includes the same kernel, but different utilities, package manager, installer, UI.
- Uses in security:
  - Examining logs
  - Verifying access and authorization in IAM system

## Linux Architecture Components

- User: The person using the computer. Multiple can use at once.
- Applications: Program that performs a specific task. In Linux, apps often installed with a package manager (helps install, manage,remove).
- Shell: Command line interpreter (interprets commands typed)
- Filesystem Hierarchy Standard (FHS): organises data. Defines how directories, directory contents, and other storage is organized.
- Kernel: Manages processes and memory. Talks to hardware.
- Hardware: Physical components (Peripheral and internal).
  - Peripheral: monitors, printers, keyboard, mouse.
  - Internal: CPU (executes program instructions), RAM (short-term memory), Hard drive (Long-term memory). 

## Linux Distributions ("Distros")

- Different Linux distributions contain different preinstalled programs, user interfaces, etc., but same kernel. 
- Distributions include the kernel, utilities, a package management system, and an installer.
- There are parent distros and distros derived from other distros
  
  ### Parent & Derived Distros
  
From Debian (uses package manager dpkg: `.deb`, and/or package management tool APT: Advanced Package Tool):

- KALI LINUX: Designed for pen tests and digital forensics, widely used in offensive cybersecurity.
- Ubuntu: User friendly distro, lots of community resources.
- Parrot: Similar to Kali Linux, but has a friendly GUI.

From Red Hat (uses package manager RPM: Red Hat Package Manager, and/or package management tool YUM: Yellowdog Updater Modified):

- Red Hat Enterprise Linux: Subscription based, dedicated support team, for enterprise use.
- CentOS: Similar to Red Hat, but similar and without support.

## KALI LINUX 
- Should be used in virtual machine to prevent damage. VM can revert to previous state.
- Pen testing tools in KALI LINUX:
  - Metasploit (look for/exploit vulnerabilities in machines)
  - Burp Suite (test for weaknesses in web apps)
  - John the Ripper (to guess passwords)

Digital forensic tools:

- tcpdump
- Wireshark
- Autopsy

## Shell

Variations:

- bash: Bourne-Again Shell (default in most)
- csh: C Shell
- ksh: Korn Shell
- tcsh: Enhanced C Shell
- zsh: Z Shell

## Feedback

Labs are great! First time using qwiklabs, it all went super smoothly. This is the first time it feels like you're actually REQUIRED to understand the content, not just parrot it.
