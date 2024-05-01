# Deployer samples #

This folder contains a sample deployer configuration.

## MGMT-NOEU-DEP00-INFRASTRUCTURE ##

This configuration deploys a deployer with the following components:


| Component                            | Virtual Machine Name                  | Location        | Details                                                       |
| ------------------------------------ | ------------------------------------- | ----------------| ------------------------------------------------------------- |
| Resource Group                       | MGMT-NOEU-DEP00-INFRASTRUCTURE        | northeurope      |                                                               |
|                                      |                                       |                 |                                                               |
| Virtual Network                      | MGMT-NOEU-DEP00-vnet                  | northeurope      | Address space:     10.170.20.0/24                             |
| Subnet (management)                  | MGMT-NOEU-DEP00_deployment-subnet     | northeurope      | Address space:     10.170.20.64/28                            |
| Subnet (firewall)                    | AzureFirewallSubnet                   | northeurope      | Address space:     10.170.20.0/26                             |
| Subnet (bastion)                     | AzureBastionSubnet                    | northeurope      | Address space:     10.170.20.128/26                           |
| Subnet (webapp)                      | AzureWebappSubnet                     | northeurope      | Address space:     10.170.20.80/28                            |
| Route table                          | MGMT-NOEU-DEP00_route-table           | northeurope      |                                                               |
| Network security group               | MGMT-NOEU-DEP00_deployment-nsg        | northeurope      |                                                               |
|                                      |                                       |                 |                                                               |
| Firewall                             | MGMT-NOEU-DEP00_firewall              | northeurope      |                                                               |
| Firewall public IP                   | MGMT-NOEU-DEP00_firewall-pip          | northeurope      |                                                               |
|                                      |                                       |                 |                                                               |
| Bastion                              | MGMT-NOEU-DEP00_bastion-host          | northeurope      |                                                               |
| Bastion public IP                    | MGMT-NOEU-DEP00_bastion-pip           | northeuropee      |                                                               |
|                                      |                                       |                 |                                                               |
| Key Vault                            | MGMTNOEUDEP00user###                  | northeurope      |                                                               |
|                                      |                                       |                 |                                                               |
| Virtual Machine (deployer)           | MGMT-NOEU-DEP00_mgmtnoeudep00deploy00 | northeurope      | Standard D4ds v4, Ubuntu 20.04                                |
|                                      |                                       |                 |                                                               |
| Application Service Plan             | mgmt-noeu-app-service-plan###         | northeurope      |                                                               |
| Application Service                  | mgmt-noeu-sapdeployment###            | northeurope      |                                                               |
