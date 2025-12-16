# Overview
This document will outline the configuration decisions I made for the clients in the environment

## Workstation Configuration
- Windows 11 Pro
- Generic product key: VK7JG-NPHTM-C97JM-9MPGT-3V66T
- Workstation name: ClientX (X being the number workstation it was when it was created)
- Default account name: admin
- 4GB Ram
- 2 CPUs
- 40GB Storage

## Network
- I set the network to an internal network, meaning it will be in its own network within VirtualBox and will not have access to the public internet.
- I set the static IP address to 10.0.0.2X (X being the same X in the workstation name), the mask to 255.255.255.0, left the gateway blank (since we're running it on an internal network in VirtualBox), and set the DNS to 10.0.0.10 (the IP address of the domain controller)
