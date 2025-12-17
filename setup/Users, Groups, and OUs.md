# Users, Groups, and Organizational Units (OUs)

## Overview
This document will list the users, groups, and OUs to demonstrate the structure of the environment.

## Users
Users are individual user accounts that can log in to computers on the domain. You create new groups by right clicking in any OU, click New, then click User.

## Groups
Groups are a collection of users that are used to give permissions to multiple users by giving the permissions to the group. You create new groups by right clicking in any OU, click New, then click Group.


## Organizational Units
OUs are logical containers used to organize objects in the domain and apply group policies. You create new OUs by right clicking the domain name in Active Directory Users and Computers, click New, then click Organizational Unit.

## Structure
**Naming convention:** department.role

I will be using the AGDLP standard which is Accounts -> Global -> Domain Local -> Permissions. This means Accounts (users/computers) will be in global gropus, global groups will be added to Domain Local groups, and Domain Local groups will be given the permissions.

homelab.local

OUs
- Users
  - IT
  - HR
  - Finance
  - Sales
- Computers
  - Workstations
    - Client1
    - Client2
  - Servers
- Groups
  - GRP_IT
  - GRP_HR
  - GRP_Finance
  - GRP_Sales
