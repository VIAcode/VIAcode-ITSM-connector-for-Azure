# VIAcode ITSM connector for Azure user guide
This guide is based on version of the ITSM Connector for Azure **1.1**.

<!-- TOC -->

<!-- TOC END -->

## Overview

Thank you for choosing VIAcode ITSM connector for Azure. This document will help you start using connector to monitor and track issues with your resources and services in Azure.

Here you can see overview table of all supported features by VIAcode ITSM connector for Azure. 



| Feature                         | Backward synchronization (VIMS to Azure) | Detection time                                               | Prerequisite                  | Supported ITSM tool |
| ------------------------------- | ---------------------------------------- | ------------------------------------------------------------ | ----------------------------- | ------------------- |
| Azure Monitor Alerts            | yes                                      | All signals after connector installation                     |                               | VIMS                |
| Budget Alerts                   | -                                        | All alerts in subscription with "Active" state               |                               | VIMS                |
| Security Center Alerts          | yes                                      | All active Security Center Alerts                            | Standard tier must be enabled | VIMS                |
| Advisor Recommendations         | -                                        | All new and updated Recommendations after connection installation |                               | VIMS                |
| Security Center Recommendations | -                                        | All new and updated Recommendations after connection installation |                               | VIMS                |




## ? Azure Monitor Alerts
#### Intro
#### Features overview table
##### Options
- Only new created alerts detected
#### Use Case.  Generate Azure Metric Alert and get it in VIMS
#### Use Case.  Generate Azure Activity Log  Alert and get it in VIMS

### Backward sync  for (ITSM system to Azure)


## ? Azure Cost Management Alerts
#### Intro
##### Options 
- Only new created alerts detected
- 
#### Use Case. Create Budget and get it in VIMS

## ? Azure Advisor Recommendations
#### Intro
#### Use Case. Create Cost Recommendation and get it in VIMS

## ? Azure Security Center Recommendations


## ? Azure Security Center Alerts 

## Features
### Sync Azure Signals button

The [Sync Azure Signals] button allows you sync active Security Alerts and Advisor recommendations created prior ITSM connector installation in your subscription.



## Frequently asked questions

### How many subscriptions supports ITSM connector? 

**Answer:** One ITSM connector can monitor one subscription.  In order to monitor more subscriptions you need install new connector to each and connect to an ITSM tool. One ITSM tool support monitoring as much subscriptions as your performance tier allows. 

Currently supported ITSM tool: VIMS. 

