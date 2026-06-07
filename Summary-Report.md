# Azure 101 Lab - Summary Report

**Student:** Adebola Shopeju  
**Subscription:** Azure for Students  
**Date:** June 2026  

---

## 1. Resource Group Confirmation

- **Name:** rg-azure101-lagos
- **Region:** South Africa North
- **Subscription:** Azure subscription 1
- **Purpose:** Logical container for all lab resources enabling 
  centralized management, cost tracking, and easy deletion after submission

---

## 2. Region Selection

**Chosen Region:** South Africa North (Johannesburg)

**Reasoning:**
- Closest Azure region to Lagos, Nigeria
- Minimizes network latency for end users in West Africa
- Supports all required services: Virtual Machines, Storage, SQL
- Contains multiple availability zones for redundancy

**Other regions considered:**
- West Europe — further away, higher latency
- East US — lowest cost but highest latency from Nigeria
- South Africa North selected as best balance of proximity and services

---

## 3. Shared Responsibility Model — IaaS

**Resource Deployed:** Storage Account (stazure101ae24) — IaaS/PaaS

**Microsoft's Responsibility:**
- Physical datacenter security, power, cooling, hardware
- Hypervisor and host operating system
- Network infrastructure and physical storage durability
- Platform availability and uptime SLA (99.9%)

**My Responsibility:**
- Access control via RBAC in Microsoft Entra ID
- Data encryption configuration (at rest and in transit)
- Network Security Group rules and firewall settings
- Backup strategy and data retention policies
- Application-layer security and secret management

**Example:** Azure secures the physical servers my storage runs on.
I must configure who can access the storage account using RBAC 
and ensure secure transfer is enabled for all connections.

---

## 4. Service Model Comparison

| Model | Who Manages | Azure Example | My Responsibility |
|---|---|---|---|
| IaaS | You manage OS upward | Virtual Machines | OS, apps, data, security |
| PaaS | Provider manages platform | Azure SQL, App Service | Data and application only |
| SaaS | Provider manages everything | Microsoft 365 | Just using the service |

---

## 5. Cost Management

- Accessed Cost Management + Billing to monitor spending
- Created budget: `my-lab-budget` — $10 limit, resets monthly
- Alert configured at 80% ($8) to warn before limit reached
- All resources deleted post-submission to avoid ongoing charges
- Total lab cost: less than $0.05

---

## 6. Identity and Access Management

- Explored Microsoft Entra ID (formerly Azure Active Directory)
- Reviewed Role-Based Access Control (RBAC) principles
- RBAC allows assigning roles like Owner, Contributor, Reader
- Principle of least privilege: give users only the access they need
- Tenant ID confirmed: 182a4a26-0404-4317-a227-0825b5285abb
