# Azure Cloud Operations | Linux VM Deployment, Monitoring & Troubleshooting

A hands-on cloud administration project built using **Microsoft Azure, Ubuntu Linux, NGINX, Azure Monitor, and Azure CLI**.

This project demonstrates practical experience in deploying and managing cloud infrastructure, configuring secure remote access, hosting a web server, exploring infrastructure monitoring, and performing Linux and Azure CLI operations.

---

## Project Overview

Cloud infrastructure requires more than simply deploying virtual machines. Administrators must also manage network access, maintain services, monitor resource performance, and troubleshoot operational issues.

The objective of this project was to build and manage an Azure-based Linux environment while gaining practical experience with essential cloud administration tasks.

## Project Objectives

- Deploy and manage an Azure Linux Virtual Machine.
- Configure virtual networking and Network Security Groups.
- Establish secure SSH connectivity.
- Install and manage an NGINX web server.
- Explore Azure Monitor and VM performance metrics.
- Configure Azure Monitor Agent (AMA) and Data Collection Rules (DCR).
- Work with Log Analytics Workspace and alert configurations.
- Perform infrastructure management using Azure CLI.
- Practice Linux service management and troubleshooting.

## Architecture

The project follows this infrastructure design:

```text
                  Internet
                     |
                  Public IP
                     |
                    NSG
                     |
              Azure Virtual Network
                     |
              Ubuntu Linux VM
                     |
                  NGINX
                     |
             Azure Monitor Agent
                     |
             Data Collection Rule
                     |
             Log Analytics Workspace
                     |
                Azure Monitor
                     |
               Alert Rules
```


## Technology Stack

| Category | Technology |
|---|---|
| Cloud Platform | Microsoft Azure |
| Operating System | Ubuntu Linux 24.04 LTS |
| Virtualization | Azure Virtual Machine |
| Networking | Virtual Network, Subnet, NSG |
| Remote Access | SSH |
| Web Server | NGINX |
| Monitoring | Azure Monitor |
| Log Management | Log Analytics Workspace |
| Monitoring Agent | Azure Monitor Agent (AMA) |
| Data Collection | Data Collection Rules (DCR) |
| Infrastructure Management | Azure CLI |
| Version Control | Git & GitHub |

## Infrastructure Details

| Resource | Configuration |
|---|---|
| Resource Group | `rg-cloud-operations` |
| Virtual Machine | `vm-cloudops` |
| Region | East US |
| Operating System | Ubuntu 24.04 LTS |
| VM Username | `azureuser` |
| Virtual Network | `vnet-cloudops` |
| Log Analytics Workspace | `law-cloudops` |

*Note: Sensitive information such as private keys, credentials, and public IP addresses is intentionally excluded.*

## Project Implementation

### 1. Azure Infrastructure Deployment

Created and managed Azure resources using the Azure Portal and Azure CLI.

Key activities:
- Created and inspected the resource group.
- Worked with virtual network infrastructure.
- Configured network security resources.
- Deployed an Ubuntu Linux Virtual Machine.

### 2. Secure SSH Connectivity

Established remote access to the Azure Linux VM using SSH authentication and a private key.

Key activities:
- Retrieved the VM administrator username.
- Set appropriate private-key permissions.
- Connected to the VM remotely.
- Verified access to the Linux environment.

### 3. NGINX Web Server Deployment

Installed and configured NGINX on the Ubuntu virtual machine to host a web page.

Key activities:
- Installed the NGINX web server.
- Managed the NGINX service.
- Configured and accessed the hosted web page.
- Practiced service status checks and troubleshooting.

### 4. Azure Monitoring

Worked with Azure Monitor to explore virtual machine performance and infrastructure health.

Key activities:
- Explored VM performance metrics.
- Configured Azure Monitor Agent.
- Worked with Data Collection Rules.
- Connected monitoring components with a Log Analytics Workspace.
- Explored metric alert configurations.

### 5. Azure CLI Operations

Used Azure Cloud Shell and Azure CLI to inspect and manage infrastructure.

Example commands:

```bash
# List resources in the resource group
az resource list \
  --resource-group rg-cloud-operations \
  --output table

# Get virtual machine details
az vm show \
  --resource-group rg-cloud-operations \
  --name vm-cloudops \
  --show-details \
  --output table

# Check VM instance status
az vm get-instance-view \
  --resource-group rg-cloud-operations \
  --name vm-cloudops \
  --query "instanceView.statuses[].displayStatus" \
  --output table
```

### 6. Linux Troubleshooting

Practiced Linux administration commands and investigated service-related issues.

```bash
# Check the current user
whoami

# Check hostname
hostname

# Check NGINX service status
sudo systemctl status nginx

# Review recent NGINX logs
sudo journalctl -u nginx -n 20 --no-pager
```

## Project Screenshots

Screenshots provide visual evidence of the infrastructure deployment and implementation.

| Screenshot | Description |
|---|---|
| Resource Group | Azure resource organization |
| Virtual Network | Network infrastructure |
| Virtual Machine | Ubuntu VM deployment |
| SSH Connection | Secure remote access |
| NGINX Website | Web server deployment |
| Azure Monitor | VM performance monitoring |
| Log Analytics | Workspace configuration |
| Azure Monitor Agent | Agent configuration |
| Data Collection Rule | Data collection configuration |
| Alert Configuration | Azure monitoring alerts |

See the [`Screenshots`](Screenshots/](https://github.com/Qaniya/azure-cloud-operations/tree/29034518b8060fa712b5a9d49e408f017c28d92c/Screenshorts)) directory for available project evidence.

## Challenges & Learning

During this project, I gained practical experience with:

- Understanding Azure resource relationships.
- Troubleshooting SSH authentication issues.
- Differentiating Azure Cloud Shell from the actual Linux VM terminal.
- Managing Linux services through systemd.
- Understanding the relationship between Azure Monitor Agent, DCR, and Log Analytics.
- Using Azure CLI to inspect cloud resources.
- Investigating infrastructure and service-related issues.

## Skills Demonstrated

- Azure Virtual Machine Administration
- Linux System Administration
- Cloud Infrastructure Management
- Virtual Networking
- SSH Configuration
- NGINX Administration
- Azure Monitoring Fundamentals
- Log Analytics
- Azure CLI
- Troubleshooting

## Future Improvements

- Automate infrastructure deployment using Azure CLI or Infrastructure as Code.
- Implement automated backup and recovery.
- Configure more advanced monitoring and alert validation.
- Deploy a database service and connect it to the web      application. 
- Improve network security and access controls.
- Build a complete cloud operations dashboard.

