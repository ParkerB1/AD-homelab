# Client1 Setup

## Overview
This document outlines the steps taken to create a virtual machine that will act as a client desktop in the Active Directory environment. It will address the machine configurations as well as steps to join the machine to the domain.

This document can be repeated multiple times to simulate an environment with multiple desktops.

## Creating the Virtual Machine
To create the VM I did the following:
- Created a new VM on VirtualBox
- Set a folder to store it in
- Selected the ISO image that I download earlier and chose the Standard Evaluation (Desktop Edition) option
- Gave it a username and password
- Set the base memory to 4GB, the CPUs to 2, and the disk memory to 40GB

## Joining the client to the domain
Joining the client the domain is very easy. You will need administrator credentials for the domain and the name of the domain to do so.
- Go to settings
- Scroll down on the System settings and click About at the bottom
- Under the Device specifications, there will be a link there that says Domain or workgroup
- Click that link and follow the steps to join the machine to the domain
- Enter the administrator credentials when prompted

The computer is now part of the active directory domain and can be administered from the domain controller.
