# Overview
This document explains how the network is setup for the Active Directory environment.

## Network Architecture
VirtualBox give each workstation an option to choose what kind of adapter it has. The options are:
- NAT
- Bridged Adapter
- Internal Network
- Host-Only Adapter
- Generic Driver
- NAT Network
- Cloud Network (EXPERIMENTAL)
- Not attached

For my environment, I chose the internal network adapter for every workstation and made sure the name matched for them all.

## DNS
The DNS server will be the IP address of the domain controller since it uses itself for name resolution. Each workstations static DNS server will be set to 10.0.0.10 so it can successfully join the domain.

## IP Addressing Scheme
I will be using the IP range of 10.0.0.0/24 (10.0.0.0 - 10.0.0.255) for my environment, keeping 10.0.0.0 - 10.0.0.20 reserved (excluding 10.0.0.10 for the domain controller) for future important reservations.

| **Workstation** | **Role** | **IP Address** | **DNS Server** |
|-----------------|----------|----------------|----------------|
| DC1 | Domain Controller | 10.0.0.10 | 127.0.0.1              |
| Client1 | Client Workstation | 10.0.0.21 | 10.0.0.10         |
| Client2 | Client Workstation | 10.0.0.22 | 10.0.0.10         |

## Domain & Forest Information
Forest name: homelab.local

Domain name: homelab.local

NetBIOS: HOMELAB

## Firewall & Security Boundaries
Windows Defender Firewall enabled on all systems.
