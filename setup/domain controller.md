# Domain Controller Setup

## Overview
This document outlines the steps taken to setup and promote the windows server 2022 virtual machine as a domain controller for the Active Directory environment.

## Creating the Virtual Machine
To create the VM I did the following:
- Created a new VM on VirtualBox
- Set a folder to store it in
- Selected the ISO image that I downloaded earlier and chose the Standard Evaluation (Desktop Edition) option
- Gave it a username and password
- Set the base memory to 5GB, the CPUs to 2, and the disk memory to 80GB

## Before promoting to Domain Controller
Since the domain controller relies on DNS for a lot of functions necessary for its successful operation, it must have a static address given to it. I used the internal network option for the VM's so they are on their own simulated network to decrease any DNS or DHCP conflicts with my home router.

I set the static IP address to 10.0.0.10 and the with a range of 10.0.0.0/24 by doing the following:
- Go to settings -> Network -> Change adapter options -> right-click the adapter -> click on internet protocol version 4 and then click properties
- Select "use the following ip address" and fill out the following
    - IP address
    - Subnet mask
    - Default gateway
- Set the Preferred DNS server to the same IP address you used in the field above since the domain controller will use itself as its DNS

## Adding Active Directory role and promoting to Domain Controller
I went to the server manager and clicked on add roles and features, then added the Active Directory Domain Services role by following the prompts. After that installed, it prompted me to promote the server to a domain controller, and give it a root domain name, which I did and named it homelab.local.

The Domain Controller is now fully set up and ready to be joined to.