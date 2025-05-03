## Introduction 

- OS: Interface btwn hardware and the user 
- Importance: Allow multiple apps to run & access external devices, enable comm btwn humans and computers
- Legacy OS: Outdated but still being used 
  
## Common operating systems

- Windows: Introduced 1985, closed source.
- macOS: Introduced 1984, partially open source.
- Linux: Introduced 1991, fully open source.
- ChromeOS: Introduced 2011, partially open source, derived from:
  - Chromium OS: Fully open source.
- Android: Introduced 2008, fully open source.
- iOS: Introduced 2007, partially open source.

## How OS works

### Booting the computer 

- Turn on machine, BIOS or UEFI chip activated & loads a bootloader, then bootloader loads the operating system.
  - BIOS: Basic Input/Output System
  - UEFI: Unified Extensible Firmware Interface (introduced 2007, more security)
- BIOS/UEFI are microchips that contain loading instructions for the computer.
- Bootloader is a software that boots the OS (from last instruction of the BIOS/UEFI)


### Completing task

- User> Application> OS> Hardware(i.e CPU, hard drive)> OS> Application> User
  ![image](https://github.com/user-attachments/assets/7b4ed0bc-e2a1-44a7-bcca-e915db3f8721)
- OS handles resource and memory management to ensure the limited capacity of the computer system is used where it is needed most.


## Virtualization

- Virtualization: using softeare to create virtual representations of phisical machines
- Virtual Machine: Virtual version of a physical computer (virtual CPU, storage, etc.)
- Can run VMs using the physical hardware of a computer, dividing resources of host computer such as RAM.
- Hypervisor: Software that manages virtual machines
- Kernel-based Virtual Machine (KVM) is an open source hypervisor built into Linux kernel.
- Can also have virtual servers, virtual networks, etc.

### Benefits of Virtual Machines 

- Security: Can provide an isolated environment(sandbox) on the physical host machine, providing layer of security. Not to be trusted fully.
- Efficiency: Can open multiple virtual machines at once and switch easily between them, streamlining security tasks.
- 

## Feedback

An odd conflict between the absolute basics "what does an OS do" and more advanced "here's how VM virtualization works"! Also needed to play all content at 1.5x.
