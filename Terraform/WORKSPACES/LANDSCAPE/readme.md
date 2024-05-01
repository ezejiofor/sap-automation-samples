# Workload Zone samples #

This folder contains three Workload zone sample configurations.

- DEV-NOEU-SAP01-INFRASTRUCTURE
- QA-NOEU-SAP02-INFRASTRUCTURE
- PRD-NOEU-SAP03-INFRASTRUCTURE

## DEV-NOEU-SAP01-INFRASTRUCTURE ##

This configuration deploys a Workload zone with the following components:

| Component                            | Name                            | Location        | Notes                                          |
| ------------------------------------ | ------------------------------- | --------------- | ---------------------------------------------- |
| Resource Group                       | DEV-NOEU-SAP01-INFRASTRUCTURE   | northeurope      |                                                |
|                                      |                                 |                 |                                                |
| Virtual Network                      | DEV-NOEU-SAP01-vnet             | northeurope      | Address space:     10.110.0.0/16               |
| Subnet (database)                    | DEV-NOEU-SAP01_db-subnet        | northeuropee      | Address space:     10.110.96.0/19              |
| Subnet (application)                 | DEV-NOEU-SAP01_app-subnet       | northeurope      | Address space:     10.110.32.0/19              |
| Subnet (web)                         | DEV-NOEU-SAP01_web-subnet       | northeurope      | Address space:     10.110.128.0/19             |
| Subnet (admin)                       | DEV-NOEU-SAP01_admin-subnet     | northeurope      | Address space:     10.110.0.0/19               |
| Route table                          | DEV-NOEU-SAP01_route-table      | northeurope      |                                                |
| Network security group (database)    | DEV-NOEU-SAP01_dbSubnet-nsg     | northeurope      |                                                |
| Network security group (application) | DEV-NOEU-SAP01_appSubnet-nsg    | northeurope      |                                                |
| Network security group (web)         | DEV-NOEU-SAP01_webSubnet-nsg    | northeurope      |                                                |
| Network security group (admin)       | DEV-NOEU-SAP01_appSubnet-nsg    | northeurope      |                                                |
|                                      |                                 |                 |                                                |
| Key Vault                            | DEVNOEUSAP01user###             | northeurope      | '###' Is a random identifier                   |
|                                      |                                 |                 |                                                |
| Storage Account                      | devnoeusap01diag###             | northeurope      | Storage account used for Virtual Machine diagnostic logs. '###' Is a random identifier                   |
| Storage Account                      | devnoeusap01witness###          | northeurope      | Cloud witness storage account used for Windows High Availability. '###' Is a random identifier                   |

## QA-NOEU-SAP02-INFRASTRUCTURE ##

This configuration deploys a Workload zone with the following components:

| Component                            | Name                            | Location        | Notes                                          |
| ------------------------------------ | ------------------------------- | --------------- | ---------------------------------------------- |
| Resource Group                       | QA-NOEU-SAP02-INFRASTRUCTURE    | northeuropee      |                                                |
|                                      |                                 |                 |                                                |
| Virtual Network                      | QA-NOEU-SAP02-vnet              | northeurope      | Address space:     10.111.0.0/16               |
| Subnet (database)                    | QA-NOEU-SAP02_db-subnet         | northeurope      | Address space:     10.111.96.0/19              |
| Subnet (application)                 | QA-NOEU-SAP02_app-subnet        | northeurope      | Address space:     10.111.32.0/19              |
| Subnet (web)                         | QA-NOEU-SAP02_web-subnet        | northeurope      | Address space:     10.111.128.0/19             |
| Subnet (admin)                       | QA-NOEU-SAP02_admin-subnet      | northeurope      | Address space:     10.111.0.0/19               |
| Route table                          | QA-NOEU-SAP02_route-table       | northeurope      |                                                |
| Network security group (database)    | QA-NOEU-SAP02_dbSubnet-nsg      | northeuropee      |                                                |
| Network security group (application) | QA-NOEU-SAP02_appSubnet-nsg     | northeurope      |                                                |
| Network security group (web)         | QA-NOEU-SAP02_webSubnet-nsg     | northeurope      |                                                |
| Network security group (admin)       | QA-NOEU-SAP02_appSubnet-nsg     | northeurope      |                                                |
|                                      |                                 |                 |                                                |
| Key Vault                            | QANOEUSAP02user###              | northeurope      | '###' Is a random identifier                   |
|                                      |                                 |                 |                                                |
| Storage Account                      | qanoeusap02diag###              | northeurope      | Storage account used for Virtual Machine diagnostic logs. '###' Is a random identifier                   |
| Storage Account                      | qanoeusap02witness###           | northeurope      | Cloud witness storage account used for Windows High Availability. '###' Is a random identifier                   |
| Storage Account                      | qanoeusap02install              | northeurope      | NFS Share for installation media. Will be used across all SIDS | |
| Storage Account                      | qanoeusap02transport            | northeurope      | NFS Share for transport. Will be used across all SIDS | |

## PRD-NOEU-SAP03-INFRASTRUCTURE ##

This configuration deploys a Workload zone with the following components:

| Component                            | Name                            | Location        | Notes                                          |
| ------------------------------------ | ------------------------------- | --------------- | ---------------------------------------------- |
| Resource Group                       | PRD-NOEU-SAP03-INFRASTRUCTURE   | northeuropee      |                                                |
|                                      |                                 |                 |                                                |
| Virtual Network                      | PRD-NOEU-SAP03-vnet             | northeurope      | Address space:     10.112.0.0/16               |
| Subnet (database)                    | PRD-NOEU-SAP03_db-subnet        | northeurope      | Address space:     10.112.96.0/19              |
| Subnet (application)                 | PRD-NOEU-SAP03_app-subnet       | northeurope      | Address space:     10.112.32.0/19              |
| Subnet (web)                         | PRD-NOEU-SAP03_web-subnet       | northeurope      | Address space:     10.112.128.0/19             |
| Subnet (admin)                       | PRD-NOEU-SAP03_admin-subnet     | northeurope      | Address space:     10.112.0.0/19               |
| Subnet (ANF)                         | PRD-NOEU-anf-subnet             | northeurope      | Address space:     10.112.64.0/27              |
| Route table                          | PRD-NOEU-SAP03_route-table      | northeurope      |                                                |
| Network security group (database)    | PRD-NOEU-SAP03_dbSubnet-nsg     | northeurope      |                                                |
| Network security group (application) | PRD-NOEU-SAP03_appSubnet-nsg    | northeurope      |                                                |
| Network security group (web)         | PRD-NOEU-SAP03_webSubnet-nsg    | northeuropee      |                                                |
| Network security group (admin)       | PRD-NOEU-SAP03_appSubnet-nsg    | northeurope      |                                                |
|                                      |                                 |                 |                                                |
| Key Vault                            | PRDNOEUSAP03user###             | northeurope      | '###' Is a random identifier                   |
|                                      |                                 |                 |                                                |
| Storage Account                      | prdnoeusap03diag###             | northeurope      | Storage account used for Virtual Machine diagnostic logs. '###' Is a random identifier                   |
| Storage Account                      | prdnoeusap03witness###          | northeurope      | Cloud witness storage account used for Windows High Availability. '###' Is a random identifier                   |
|                                      |                                 |                 |                                                |
| NetApp Account                       | PRD-NOEU-SAP03_netapp_account   | northeurope      |                                                |
| NetApp Capacity Pool                 | PRD-NOEU-SAP03_netapp_pool      | northeurope      |                                                |
| NetApp Volume                        | PRD-NOEU-SAP03_install          | northeurope      | Volume for installation media. Will be used across all SIDS |
| NetApp Volume                        | PRD-NOEU-SAP03_transport        | northeurope      |                                                |
|                                      |                                 |                 |                                                |
| Virtual Machine                      | PRD-NOEU-SAP03_wz-vm00          | northeurope      | Utilisy VM, use it for SAPGUI etc.              |
