# VIAcode ITSM connector for Azure for VIMS deployment and configuration guide
This guide is based on version **1.1** of VIAcode ITSM Connector for Azure for VIMS.

<!-- TOC -->

- [Before you begin](#before-you-begin)
  - [Deploy](#deploy)
    - [VIAcode Managed Service customers](#viacode-managed-service-customers)
    - [Not VIAcode Managed Service customers](#not-viacode-managed-service-customers)
    - [Pricing](#pricing)

- [Configuration of VIAcode ITSM connector for Azure for VIMS](#configuration-of-viacode-itsm-connector-for-azure-for-VIMS)
  - [Basics](#basics)
  - [VIAcode Incident Management System](#viacode-incident-management-system)
  - [Review and create](#review-and-create)
  - [Alert state backward synchronization](#alert-state-backward-synchronization)
    - [Overview](#overview)
    - [How to setup](#how-to-setup)
- [Uninstallation of VIAcode ITSM connector for Azure](#uninstallation-of-viacode-itsm-connector-for-azure)
  - [Deletion Notes](#deletion-notes)
  - [Steps to Remove Application and Managed Resource Group](#steps-to-remove-application-and-managed-resource-group)  
  
- [Technical details](#technical-details)
  - [Supported alert types](#supported-alert-types)
- [How-to guide](#how-to-guide)
<!-- TOC END -->



## Before you begin

Verify that your account user type is not Guest in the chosen tenant.

- Sign in to the [Azure Portal](https://portal.azure.com/).
- Select "Azure Active Directory", select "Users".

![Guest type account](./media/guestAccount.png)

[Guest](https://docs.microsoft.com/azure/active-directory/b2b/user-properties) accounts have limited permissions. Deployment under a guest account will fail.

## Deploy

### VIAcode Managed Service customers

If you are a VIAcode Managed Service customer then to install VIAcode ITSM connector for Azure open Azure Portal and click Create a resource.

![Create a resource](./media/createAResource.png)

Type VIAcode in a "Search services and marketplace" box and press Enter.

---
**NOTE**

Do not select VIAcode ITSM connector for Azure from dropdown.

---

![Create a resource](./media/createAResourceSearch.png)

You will see panel with text "You have Private Offers available" and "View Private Offers + Plans" hyperlink besides.
Click on it.

![View Private Offers + Plans](./media/viewPrivateOffers.png)

Find VIAcode ITSM connector for Azure and click on it.

![Private Offers + Plans](./media/privateOffers.png)

Select subscription to install connector to and click Create.

![Create](./media/privateCreate.png)

### Not VIAcode Managed Service customers

- [Navigate](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/viacode_consulting-1089577.viacode-itsm-connector-for-azure) to Microsoft Azure Marketplace and find "VIAcode ITSM connector for Azure" offer.
![Azure Market Place](./media/azureMarketPlaceConnector.png)

- Press "Get it now" button.
- Press "Continue".

You will be taken to Azure Portal to complete installation:
![Azure Portal](./media/azurePortalOfferProfileConnector.png)

- Press "Create".

### Pricing

The total cost of running VIAcode ITSM connector for Azure is a combination of the selected software plan and cost of the Azure infrastructure on which you will be running it. The Azure infrastructure cost might vary with regards to the region, type of subscription and other discounts.

## Configuration of VIAcode ITSM connector for Azure for VIMS

## Basics

![Basics](./media/basicsSettingsConnector.png)

- Choose a subscription to deploy the managed application.
- Create a new Resource Group.
- Select a region.
- Provide a name for your application's managed resource group.
- Press "Next : Settings >" button.

## VIAcode Incident Management System

You have to specify VIAcode Incident Management System hostname (FQDN) and administrator user credentials.
ITSM Connector will automatically create new VIMS user. All tickets are created on behalf of this user.
To create user we need to know Administrators credentials, Organisation Name and Role for new user.

![Azure AD Integration](./media/connectorSettingsVIMS.png)

- Set VIAcode Incident Management System hostname.
- Set admin user login ("admin" by default).
- Set admin user password ("admin" by default).
- Set Organisation name ("Customer" by default).
- Set Role ("Connector" by default).
- Press "Next : Review + create >" button.

## Review and create

![Review + create](./media/reviewPlusCreateConnector.png)

- Agree to the terms and conditions.
- Press "Create" button.

## Alert state backward synchronization

### Overview

VIAcode ITSM connector for Azure provides an alert state backward synchronization mechanism. It enables automatic state synchronization of the VIMS incidents and Azure Alerts.

### How to setup

In order to configure alert state synchronization please provide VIAcode ITSM connector for Azure Managed App with Contributor Role for subscription VIAcode ITSM connector for Azure is deployed to in Azure Portal.

- Click on the installed managed application.
- Select 'Application Permissions (preview)' blade.
![App permissions blade](./media/managedAppPermissions1.png)
- Click "Add."
![Add](./media/managedAppPermissions2.png)
  - Select 'Contributor' role.
  - Check that Connector's subscription is selected.
  - "OK."
![OK](./media/managedAppPermissions3.png)

## Uninstallation of viacode ITSM connector for azure

### Deletion notes
Installation of VIAcode ITSM for Azure requires 2 resource groups:

- The First one for the application itself (Managed Application location).
- The Second is for the managed resources that the application requires (e.g. "mrg-viacode-itsm-z-`<id>`").

### Steps to Remove Application and Managed Resource Group
**Step 1:**
Go to Resource Group where the Managed Application installed (application named "VIAcode-ITSM-connector-for-Azure").

**Step 2:**
Select this Application and click "Delete" button, confirm the deletion by typing "Yes" on the sidebar, then click "Delete".
Deletion the Managed Application will consequently delete the second resource group and all of its content.

![Delete_itsm-z](./media/Delete_itsm-z_confirmation.PNG)

**Step 3:** (optional)
If the First Resource Group is empty - only Managed Application was stored there - you should also delete this Resource Group as well.



## How-to guide
For more information about VIAcode ITSM connector features and use cases please read ["VIAcode ITSM connector for Azure for VIMS user guide"](ITSM_connector_VIMS_user_guide.md)



[TOC]


