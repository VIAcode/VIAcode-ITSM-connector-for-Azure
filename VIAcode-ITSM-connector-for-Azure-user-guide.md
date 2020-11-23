# VIAcode ITSM connector for Azure user guide


<!-- TOC -->

<!-- TOC END -->

## Overview

This guide is based on a version of the ITSM Connector for Azure **1.1**. 

Thank you for choosing VIAcode ITSM connector for Azure. ITSM connector helps you keep under control different types of Azure signals in one single ITSM ticketing system. 

This document will help you start using the connector to monitor and track issues with your resources and services in Azure using ITSM ticketing system VIMS. 

Here you can see an overview table of all supported features in VIAcode ITSM connector for Azure. 



| Feature                         | Backward synchronization (VIMS to Azure) | Detection time                                               | Prerequisite                  | Supported ITSM tool | Options                                                      |
| ------------------------------- | ---------------------------------------- | ------------------------------------------------------------ | ----------------------------- | ------------------- | ------------------------------------------------------------ |
| Azure Monitor Alerts            | yes                                      | All signals since connector installation                     |                               | VIMS                |                                                              |
| Budget Alerts                   | -                                        | All alerts in subscription with "Active" state               |                               | VIMS                |                                                              |
| Security Center Alerts          | yes                                      | All active  Security Center Alerts since connector installation | Standard tier must be enabled | VIMS                | It is possible sync prior created active alerts with [Sync Azure signals]  option |
| Advisor Recommendations         | -                                        | All new and updated Recommendations since connection installation |                               | VIMS                | It is possible sync prior created recommendations with [Sync Azure signals]  option |
| Security Center Recommendations | -                                        | All new and updated Recommendations since connection installation |                               | VIMS                |                                                              |

## VIMS 

ITSM ticketing system VIMS (VIAcode Incident Management system) simplifies engineering effort on managing Azure signals by collecting different Azure issues in one single place. 

### Groups of signals

 By default, ticket on new active alerts (from Azure Monitor, Security Alerts, Budget Alerts)  will be created in "New incidents" group.   Notifications about Active Azure Advisor recommendations appear in "New recommendations" group. 

![vimsPanel](./media/vimsPanel.png)

###  Managing different subscriptions

One ITSM connector allows to monitor one subscription in VIMS.  

It is possible to monitor several subscriptions with same ITSM tool VIMS. For this, you need to install connector to each subscription and specify FQDN of same  ITSM ticketing system.

## ?Azure Monitor Alerts

#### Introduction

Azure Monitor Alerts (Metric, Log Analytics, Activity log etc.) will be automatically created in your ticketing system with detailed information about incidents since connector installation to the subscription. 

#### Use Case: Detect active Azure Metric Alert 



#####  Backward sync 

#### Use Case.  Generate Azure Activity Log  Alert and get it in VIMS

### 


## ? Azure Cost Management Alerts
#### Intro
##### Options 
- Only new created alerts detected
- 
#### Use Case. Create Budget and get it in VIMS

## ? Azure Advisor recommendations
#### Intro

Azure Advisor recommendations will be automatically created in your ticketing system with detailed information about incidents since connector installation to the subscription. 

#### Use Case. Create Cost Recommendation and get it in VIMS



#### Repeat Count

## ? Azure Security Center Recommendations


## ? Azure Security Center Alerts 

## Features
### Sync Azure signals

The [Sync Azure signals] button allows you obtain active Security Alerts and Advisor recommendations created in your subscription prior ITSM connector installation.

To get prior incidents and recommendations in your ITSM tool perform the following steps: 

**Step1**

Go to Resource Group where the Managed Application installed (application named "VIAcode-ITSM-connector-for-Azure"). 

**Step2**

Open the  managed application named "VIAcode-ITSM-connector-for-Azure"

**Step3**

Click [Sync Azure signals] button 

![syncAzureSignalsbtn](./media/syncAzureSignalsbtn.png)



**Step4**

Select types of signals to retrieve and click [Review+submit ] in Azure

![syncParameters-alerts-recommendations](./media/syncParameters-alerts-recommendations.png)



## Frequently asked questions

### How many subscriptions does ITSM connector support? 

**Answer:** 



