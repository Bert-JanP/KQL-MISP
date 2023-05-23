# KQL-MISP
This repository is a KQL MISP implementation. The goal of this repository is to share queries which implement MISP feeds which can be used for detection or enrichment of incidents. No additional sources are needed besides an environment in which you can run KQL. This implementation can be used in Sentinel, Defender For Endpoint and other Log Analytics sources that fit your needs. 

MISP is a "*A threat intelligence platform for sharing, storing and correlating Indicators of Compromise of targeted attacks, threat intelligence, financial fraud information, vulnerability information or even counter-terrorism information.*" [MISP](https://www.misp-project.org/).

The architecture used is shown below, where this repository provides the pulling of the data from MISP and translates that information into a KQL query. 

![Overview KQL MISP](Images/KQL%20MISP.png "Overview KQL MISP")

## NOTE!! This repo is still under development!!

The repository is still under development and is not finished (yet). I have already made this repository public so that everyone can already benefit from the available queries. The queries might not be complete, if you miss inforamtion please let me know so that can be adjusted. 

# Implementation
The queries in this repository are divided into two categories:
- Sentinel (& Log Analytics)
- Defender For Endpoint

The files in each folder represent the queries that can be used to leverage a MISP feed, the query can be copied an be used to create a detection on to hunt for specific activities. The reason why there are two different categories is the difference between the KQL syntax in Sentinel and MDE and the different tables that to search for IOCs. 


# Table usage

Sentinel and Defender For Endpoint use different tables. In Defender For Endpoint, only tables within the MDE licence are used. In Sentinel more tables are used. If you do not have a table you can simply delete the section of that table and the query will run. The section below lists all tables that are used. 

## Sentinel
- DeviceNetworkEvents
- DeviceFileEvents

## Defender For Endpoint
- DeviceNetworkEvents
- DeviceFileEvents

# To do
The following items are at least on the to do list, since this project is still under development. 

- Add all feeds MDE
- Add all feeds Sentinel
- Query pack sentinel

## Contributions

Contributions to this repository are appreciated! If you have a query which already uses a MISP feed which has not been implemented yet, then feel free to add it to the right folder. If you identify any errors in the queries please reach out, in order for them to be fixed. 