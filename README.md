# Enterprise Network & Security Architecture on Microsoft Azure

## Project Overview
Designed and implemented a segmented enterprise network environment using Microsoft Azure. The project demonstrates department-level network isolation, secure communication policies and network security verification.

## Architecture

- Azure Virtual Network: EnterpriseVNet01
- Address Space: 10.0.0.0/16
- IT Subnet: 10.0.3.0/24
- HR Subnet: 10.0.1.0/24
- Finance Subnet: 10.0.2.0/24

## Azure Resources
- 1 Azure Virtual Network
- 3 Subnets
- 3 Network Security Groups
- 3 Ubuntu Virtual Machines
- Azure Network Watcher

## Security Implementation

- Configured department-specific Network Security Groups.
- Allowed IT subnet communication with HR and Finance.
- Blocked HR-to-Finance communication.
- Blocked Finance-to-HR communication.
- Deployed private virtual machines without public IP addresses.

## Security Testing

Used Azure Network Watcher IP Flow Verify to validate inbound TCP traffic policies.

| Test | Result |
|---|---|
| IT → HR | Allowed |
| IT → Finance | Allowed |
| HR → Finance | Denied |
| Finance → HR | Denied |

All four IP Flow Verify tests returned the expected results.

## Technologies Used
- Microsoft Azure
- Azure Virtual Network
- Network Security Groups
- Ubuntu Linux
- Azure Virtual Machines
- Azure Network Watcher
- TCP/IP and Subnetting

## Learning Outcomes
- Enterprise network segmentation
- Azure networking fundamentals
- Network security rule configuration
- Private IP addressing
- Network traffic verification

## Project Status
Implemented and security-tested.
