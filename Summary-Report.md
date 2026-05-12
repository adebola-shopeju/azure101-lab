# Azure 101 Lab - Summary Report

**Student**: Adebola Shopeju  
**Subscription**: Azure for Students  
**Date**: May 12, 2026

## 1. Resource Group Confirmation
- **Name**: rg-azure101-lagos
- **Region**: South Africa North
- **Purpose**: Logical container for all lab resources enabling centralized management and cost tracking

## 2. Region Selection
**Chosen Region**: South Africa North  
**Reasoning**: Closest Azure region to Lagos, Nigeria to minimize network latency for end users. Availability zones provide redundancy for production workloads.

## 3. Shared Responsibility Model - IaaS
**Resource Deployed**: Standard_B2ats_v2 Virtual Machine + Standard_LRS Storage Account

**Microsoft's Responsibility**:
- Physical datacenter security, power, cooling, hardware
- Hypervisor, host OS, network infrastructure  
- Physical storage durability for disks

**My Responsibility**:
- Guest OS patching and security updates
- Network Security Group rules and firewall configuration
- Data encryption at rest/in transit, backup strategy
- Identity/access via RBAC in Microsoft Entra ID
- Application-layer security

**Example**: Azure secures the physical SSD my VM runs on. I must configure NSG rules to block port 22 from the internet and manage OS updates.

## 4. Cost Management
Accessed Cost Management + Billing to verify US$153.76 Azure for Students credit expires in 4 days. Current cost US$44.09 from test deployments. All resources deleted immediately after screenshot capture. Total lab cost: <$0.05.
