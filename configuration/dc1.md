# Overview
This document will outline the configuration decisions I made for the Domain Controller in the environment

## Workstation configuration
- Windows Server 2022
- workstation name: DC1
- default account name: admin
- 5GB ram
- 2 CPUs
- 80GB storage

## Network
- I set the network to an internal network, meaning it will be in its own network within VirtualBox and will not have access to the public internet.
- I set the static IPv4 address to 10.0.0.10, the mask to 255.255.255.0, left the gateway blank (since we're running it on an internal network in VirtualBox), and set the DNS to 10.0.0.10

## Roles
Once the server was setup properly workstation and network wise, I promoted it to the domain controller using these steps:
- In server manager, click Manage - Add roles and features
- Choose role-based installation
- Select the server
- Check "Active Directory Domain Services (AD DS)
- click next until the install button comes up and install the role
- After the installation, you'll see a notification in Server Manager to promote this server to a domain controller. Click it and follow the wizzard.
