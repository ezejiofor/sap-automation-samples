# SAP Library samples #

This folder contains a SAP Library configuration sample

## MGMT-NOEU-SAP_LIBRARY ##

This configuration deploys a Workload zone with the following components:

| Component                            | Name                            | Location        | Notes                                          |
| ------------------------------------ | ------------------------------- | --------------- | ---------------------------------------------- |
| Resource Group                       | MGMT-NOEU-SAP_LIBRARY           | northeurope      |                                                |
|                                      |                                 |                 |                                                |
| Storage Account                      | mgmtnoeusaplib###               | northeurope      | Storage account used SAP installation media. '###' Is a random identifier                   |
| Storage Account                      | mgmtnoeutfstate###              | northeurope      | Storage account used Terraform state file. '###' Is a random identifier                   |
|                                      |                                 |                 |                                                |
| DNS                                  | sap.contoso.net                 | northeurope      |                                                |
