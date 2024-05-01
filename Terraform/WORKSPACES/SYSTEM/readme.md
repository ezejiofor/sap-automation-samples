# System  samples #

This folder contains sample system configurations.

- DEV-NOEU-SAP01-EQ2
- DEV-NOEU-SAP01-WIN
- QA-NOEU-SAP02-Q00
- QA-NOEU-SAP02-Q01
- QA-NOEU-SAP02-Q02
- PRD-NOEU-SAP03-P00
- PRD-NOEU-SAP03-P01
- PRD-NOEU-SAP03-P02

## DEV-NOEU-SAP01-EQ2 ##

This configuration deploys a system with the following components:

SID: X00

| Component                            | Virtual Machine Name              | Hostname        | Location        | Count | Details                                        |
| ------------------------------------ | --------------------------------- | ----------------| --------------- | ----- | ---------------------------------------------- |
| Resource Group                       | DEV-NOEU-SAP01-EQ2                | northeurope      |                 |       |                                                |
|                                      |                                   |                 |                 |       |                                                |
| Virtual Machine (database)           | DEV-NOEU-SAP01-EQ2_x00dhdb00l0### | x00dhdb00l###   | northeurope      | 1     | E20dsv4, Disks: 4 P10 (data), 3 P6 (log) , P15 (sap), P20 (backup), P20 (shared) |
| Virtual Machine (scs)                | DEV-NOEU-SAP01-EQ2_x00scs00l###   | x00scs00l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (primary app)        | DEV-NOEU-SAP01-EQ2_x00app00l###   | x00app00l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (app)                | DEV-NOEU-SAP01-EQ2_x001pp01l###   | x00app01l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
|                                      |                                   |                 |                 |       |                                                |
| Load Balancer (database)             | DEV-NOEU-SAP01-EQ2_db-alb         | northeurope      |                 |       |                                                |
| Load Balancer (scs)                  | DEV-NOEU-SAP01-EQ2_scs-alb        | northeurope      |                 |       |                                                |
|                                      |                                   |                 |                 |       |                                                |
| Proximity Placement Group            | DEV-NOEU-SAP01-EQ2-z1-ppg         | northeurope      |                 |       | One Proximity Placement Group per zone         |
| Availability set                     | DEV-NOEU-SAP01-EQ2_z1_app-avset   | northeurope      |                 |       | One Availability set per zone                  |

## DEV-NOEU-SAP01-WIN ##

This configuration deploys a Windows system zone with the following components:

SID: WIN

| Component                            | Virtual Machine Name              | Hostname        | Location        | Count | Details                                        |
| ------------------------------------ | --------------------------------- | ----------------| --------------- | ----- | ---------------------------------------------- |
| Resource Group                       | DEV-NOEU-SAP01-WIN                | northeurope      |                 |       |                                                |
|                                      |                                   |                 |                 |       |                                                |
| Virtual Machine (database)           | DEV-NOEU-SAP01-WIN_windb00w###    | windb00w###     | northeurope      | 1     | E14sv4, Windows Server 2022, Disks: 4 P10 (data), 1 P15 (log) , P6 (sap) |
| Virtual Machine (scs)                | DEV-NOEU-SAP01-WIN_winscs00w###   | x00scs00w###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (primary app)        | DEV-NOEU-SAP01-WIN_winapp00w###   | winapp00w###    | northeuropee      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (app)                | DEV-NOEU-SAP01-WIN_winapp01w###   | winapp01w###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
|                                      |                                   |                 |                 |       |                                                |
| Load Balancer (database)             | DEV-NOEU-SAP01-WIN_db-alb         | northeurope      |                 |       |                                                |
| Load Balancer (scs)                  | DEV-NOEU-SAP01-WIN_scs-alb        | northeurope      |                 |       |                                                |
|                                      |                                   |                 |                 |       |                                                |
| Proximity Placement Group            | DEV-NOEU-SAP01-WIN-z1-ppg         | northeurope      |                 |       | One Proximity Placement Group per zone         |
| Availability set                     | DEV-NOEU-SAP01-WIN_z1_app-avset   | northeurope      |                 |       | One Availability set per zone                  |

## QA-NOEU-SAP02-Q00 ##

This configuration deploys a Redhat 8.4 system using Azure Files NFS for shared files with the following components:

SID: Q00

| Component                            | Virtual Machine Name              | Hostname        | Location        | Count | Details                                        |
| ------------------------------------ | --------------------------------- | ----------------| --------------- | ----- | ---------------------------------------------- |
| Resource Group                       | QA-NOEU-SAP02-Q00                 | northeurope      |                 |       |                                                |
|                                      |                                   |                 |                 |       |                                                |
| Virtual Machine (database)           | QA-NOEU-SAP02-Q00_q00dhdb00l###   | q00dhdb00l###   | northeurope      | 1     | E20dsv4, Disks: 4 P10 (data), 3 P6 (log) , P15 (sap), P20 (backup), P20 (shared) |
| Virtual Machine (scs)                | QA-NOEU-SAP02-Q00_q00scs00l###    | q00scs00l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (primary app)        | QA-NOEU-SAP02-Q00_q00app00l###    | q00app00l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (app)                | QA-NOEU-SAP02-Q00_q001pp01l###    | q00app01l###    | northeuropee      | 1     | D4sv3, Disks: P10 (sap)             |
|                                      |                                   |                 |                 |       |                                                |
| Load Balancer (database)             | QA-NOEU-SAP02-Q00_db-alb          | northeurope      |                 |       |                                                |
| Load Balancer (scs)                  | QA-NOEU-SAP02-Q00_scs-alb         | northeurope      |                 |       |                                                |
|                                      |                                   |                 |                 |       |                                                |
| Proximity Placement Group            | QA-NOEU-SAP02-Q00-z1-ppg          | northeurope      |                 |       | One Proximity Placement Group per zone         |
| Availability set                     | QA-NOEU-SAP02-Q00_z1_app-avset    | northeurope      |                 |       | One Availability set per zone                  |
|                                      |                                   |                 |                 |       |                                                |
| Storage Account                      | qanoeusap02q00sapmnt              | northeurope      |                 |       | Storage account used for sapmnt share          |

## QA-NOEU-SAP02-Q01 ##

This configuration deploys a highly available Redhat 8.4 system using Azure Files NFS for shared files with the following components:

SID: Q01

| Component                            | Virtual Machine Name              | Hostname        | Location        | Count | Details                                        |
| ------------------------------------ | --------------------------------- | ----------------| --------------- | ----- | ---------------------------------------------- |
| Resource Group                       | QA-NOEU-SAP02-Q00                 | northeurope      |                 |       |                                                |
|                                      |                                   |                 |                 |       |                                                |
| Virtual Machine (database, primary)  | QA-NOEU-SAP02-Q01_q01dhdb00l###   | q01dhdb00l###   | northeurope      | 1     | E20dsv4, Disks: 4 P10 (data), 3 P6 (log) , P15 (sap), P20 (backup), P20 (shared) |
| Virtual Machine (database,secondary) | QA-NOEU-SAP02-Q01_q01dhdb01l###   | q01dhdb01l###   | northeurope      | 1     | E20dsv4, Disks: 4 P10 (data), 3 P6 (log) , P15 (sap), P20 (backup), P20 (shared) |
| Virtual Machine (scs, ASCS)          | QA-NOEU-SAP02-Q01_q01scs00l###    | q01scs00l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (scs, ERS)           | QA-NOEU-SAP02-Q01_q01scs01l###    | q01scs01l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (primary app)        | QA-NOEU-SAP02-Q01_q01app00l###    | q01app00l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (app)                | QA-NOEU-SAP02-Q01_q001pp01l###    | q01app01l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
|                                      |                                   |                 |                 |       |                                                |
| Load Balancer (database)             | QA-NOEU-SAP02-Q01_db-alb          | northeurope      |                 |       |                                                |
| Load Balancer (scs)                  | QA-NOEU-SAP02-Q01_scs-alb         | northeurope      |                 |       |                                                |
|                                      |                                   |                 |                 |       |                                                |
| Proximity Placement Group            | QA-NOEU-SAP02-Q01-z1-ppg          | northeurope      |                 |       | One Proximity Placement Group per zone         |
| Availability set                     | QA-NOEU-SAP02-Q01_z1_app-avset    | northeuropeee      |                 |       | One Availability set per zone                  |
|                                      |                                   |                 |                 |       |                                                |
| Storage Account                      | qanoeusap02q00sapmnt              | northeurope      |                 |       | Storage account used for sapmnt share          |

## QA-NOEU-SAP02-Q02 ##

This configuration deploys a highly available SUSE 15 SP 3 system using Azure Files NFS for shared files with the following components:

SID: Q02

| Component                            | Virtual Machine Name              | Hostname        | Location        | Count | Details                                        |
| ------------------------------------ | --------------------------------- | ----------------| --------------- | ----- | ---------------------------------------------- |
| Resource Group                       | QA-NOEU-SAP02-Q00                 | northeurope      |                 |       |                                                |
|                                      |                                   |                 |                 |       |                                                |
| Virtual Machine (database, primary)  | QA-NOEU-SAP02-Q02_q02dhdb00l###   | q02dhdb00l###   | northeurope      | 1     | E20dsv4, Disks: 4 P10 (data), 3 P6 (log) , P15 (sap), P20 (backup), P20 (shared) |
| Virtual Machine (database,secondary) | QA-NOEU-SAP02-Q02_q02dhdb01l###   | q02dhdb01l###   | northeurope      | 1     | E20dsv4, Disks: 4 P10 (data), 3 P6 (log) , P15 (sap), P20 (backup), P20 (shared) |
| Virtual Machine (scs, ASCS)          | QA-NOEU-SAP02-Q02_q02scs00l###    | q02scs00l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (scs, ERS)           | QA-NOEU-SAP02-Q02_q02scs01l###    | q02scs01l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (primary app)        | QA-NOEU-SAP02-Q02_q02app00l###    | q02app00l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (app)                | QA-NOEU-SAP02-Q01_q001pp01l###    | q02app01l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
|                                      |                                   |                 |                 |       |                                                |
| Load Balancer (database)             | QA-NOEU-SAP02-Q01_db-alb          | northeurope      |                 |       |                                                |
| Load Balancer (scs)                  | QA-NOEU-SAP02-Q01_scs-alb         | northeurope      |                 |       |                                                |
|                                      |                                   |                 |                 |       |                                                |
| Proximity Placement Group            | QA-NOEU-SAP02-Q01-z1-ppg          | northeuropee      |                 |       | One Proximity Placement Group per zone         |
| Availability set                     | QA-NOEU-SAP02-Q01_z1_app-avset    | northeurope      |                 |       | One Availability set per zone                  |
|                                      |                                   |                 |                 |       |                                                |
| Storage Account                      | qanoeusap02q00sapmnt              | northeurope      |                 |       | Storage account used for sapmnt share          |

## PRD-NOEU-SAP03-P00 ##

This configuration deploys a Redhat 8.4 system using Azure NetApp Files for shared files with the following components:

SID: P00

| Component                            | Virtual Machine Name              | Hostname        | Location        | Count | Details                                        |
| ------------------------------------ | --------------------------------- | ----------------| --------------- | ----- | ---------------------------------------------- |
| Resource Group                       | PRD-NOEU-SAP03-P00                | northeurope      |                 |       |                                                |
|                                      |                                   |                 |                 |       |                                                |
| Virtual Machine (database)           | PRD-NOEU-SAP03-P00_p00dhdb00l###  | p00dhdb00l###   | northeurope      | 1     | E20dsv4, Disks: 4 P10 (data), 3 P6 (log) , P15 (sap), P20 (backup), P20 (shared) |
| Virtual Machine (scs)                | PRD-NOEU-SAP03-P00_p00scs00l###   | p00scs00l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (primary app)        | PRD-NOEU-SAP03-P00_p00app00l###   | p00app00l###    | northeuropee      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (app)                | PRD-NOEU-SAP03-P00_p001pp01l###   | p00app01l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
|                                      |                                   |                 |                 |       |                                                |
| Load Balancer (database)             | PRD-NOEU-SAP03-P00_db-alb         | northeurope      |                 |       |                                                |
| Load Balancer (scs)                  | PRD-NOEU-SAP03-P00_scs-alb        | northeurope      |                 |       |                                                |
|                                      |                                   |                 |                 |       |                                                |
| Proximity Placement Group            | PRD-NOEU-SAP03-P00-z1-ppg         | northeurope      |                 |       | One Proximity Placement Group per zone         |
| Availability set                     | PRD-NOEU-SAP03-P00_z1_app-avset   | northeurope      |                 |       | One Availability set per zone                  |

## PRD-NOEU-SAP03-P01 ##

This configuration deploys a highly available SUSE 15 SP3  system using Azure NetApp Files for shared files with the following components:

SID: P01

| Component                            | Virtual Machine Name              | Hostname        | Location        | Count | Details                                        |
| ------------------------------------ | --------------------------------- | ----------------| --------------- | ----- | ---------------------------------------------- |
| Resource Group                       | PRD-NOEU-SAP03-P00                | northeurope      |                 |       |                                                |
|                                      |                                   |                 |                 |       |                                                |
| Virtual Machine (database, primary)  | PRD-NOEU-SAP03-P01_p01dhdb00l###  | p01dhdb00l###   | northeurope      | 1     | E20dsv4, Disks: 4 P10 (data), 3 P6 (log) , P15 (sap), P20 (backup), P20 (shared) |
| Virtual Machine (database,secondary) | PRD-NOEU-SAP03-P01_p01dhdb01l###  | p01dhdb01l###   | northeurope      | 1     | E20dsv4, Disks: 4 P10 (data), 3 P6 (log) , P15 (sap), P20 (backup), P20 (shared) |
| Virtual Machine (scs, ASCS)          | PRD-NOEU-SAP03-P01_p01scs00l###   | p01scs00l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (scs, ERS)           | PRD-NOEU-SAP03-P01_p01scs01l###   | p01scs01l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (primary app)        | PRD-NOEU-SAP03-P01_p01app00l###   | p01app00l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (app)                | PRD-NOEU-SAP03-P01_p001pp01l###   | p01app01l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
|                                      |                                   |                 |                 |       |                                                |
| Load Balancer (database)             | PRD-NOEU-SAP03-P01_db-alb         | northeuropeee      |                 |       |                                                |
| Load Balancer (scs)                  | PRD-NOEU-SAP03-P01_scs-alb        | northeurope      |                 |       |                                                |
|                                      |                                   |                 |                 |       |                                                |
| Proximity Placement Group            | PRD-NOEU-SAP03-P01-z1-ppg         | northeurope      |                 |       | One Proximity Placement Group per zone         |
| Availability set                     | PRD-NOEU-SAP03-P01_z1_app-avset   | northeurope      |                 |       | One Availability set per zone                  |

## PRD-NOEU-SAP03-P02 ##

This configuration deploys a highly available Red Hat 8.2 system using Azure NetApp files for shared files with the following components:

HANA Data and HANA log volumes are on Azure NetApp Files (ANF).
SID: P02

| Component                            | Virtual Machine Name              | Hostname        | Location        | Count | Details                                        |
| ------------------------------------ | --------------------------------- | ----------------| --------------- | ----- | ---------------------------------------------- |
| Resource Group                       | PRD-NOEU-SAP03-P00                | northeurope      |                 |       |                                                |
|                                      |                                   |                 |                 |       |                                                |
| Virtual Machine (database, primary)  | PRD-NOEU-SAP03-P02_q02dhdb00l###  | p02dhdb00l###   | northeurope      | 1     | E20dsv4, Disks: 4 P10 (data), 3 P6 (log) , P15 (sap), P20 (backup), P20 (shared) |
| Virtual Machine (database,secondary) | PRD-NOEU-SAP03-P02_q02dhdb01l###  | p02dhdb01l###   | northeurope      | 1     | E20dsv4, Disks: 4 P10 (data), 3 P6 (log) , P15 (sap), P20 (backup), P20 (shared) |
| Virtual Machine (scs, ASCS)          | PRD-NOEU-SAP03-P02_q02scs00l###   | p02scs00l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (scs, ERS)           | PRD-NOEU-SAP03-P02_q02scs01l###   | p02scs01l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (primary app)        | PRD-NOEU-SAP03-P02_q02app00l###   | p02app00l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
| Virtual Machine (app)                | PRD-NOEU-SAP03-P01_q001pp01l###   | p02app01l###    | northeurope      | 1     | D4sv3, Disks: P10 (sap)             |
|                                      |                                   |                 |                 |       |                                                |
| Load Balancer (database)             | PRD-NOEU-SAP03-P01_db-alb         | northeurope      |                 |       |                                                |
| Load Balancer (scs)                  | PRD-NOEU-SAP03-P01_scs-alb        | northeurope      |                 |       |                                                |
|                                      |                                   |                 |                 |       |                                                |
| Proximity Placement Group            | PRD-NOEU-SAP03-P01-z1-ppg         | northeurope      |                 |       | One Proximity Placement Group per zone         |
| Availability set                     | PRD-NOEU-SAP03-P01_z1_app-avset    | northeurope      |                 |       | One Availability set per zone                  |
