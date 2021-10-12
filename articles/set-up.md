---
title: Set up Supply Chain Insights
description: This topic provides requirements and instructions for using and setting up Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 10/12/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---

# Set up Supply Chain Insights

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

This topic provides requirements and instructions for using and setting up Microsoft Dynamics 365 Supply Chain Insights.

## Public preview enrollment

There are two ways to sign up for the public preview of Dynamics 365 Supply Chain Insights. The first is to sign up from the [Supply Chain Insights home page](https://dynamics.microsoft.com/supply-chain-insights/). The second method is by signing up through an invitation sent from a company that is already a public preview user. Companies who sign up using either method will then be contacted by email from the Supply Chain Insights team with information on how register as a public preview user.

## Prerequisites

- Supply Chain Insights is currently only available in the English, German, and Chinese languages.
- Supply Chain Insights only supports the most recent and second most recent versions of the Edge, Chrome, Firefox, and Safari browsers.
- An Azure Active Directory (Azure AD) tenant is required. A tenant represents an organization within Azure AD and is a way to manage user access to Azure resources to ensure controlled access to your data. If your business already has an Azure AD tenant, contact your Azure AD tenant administrator or IT department to have them sign up for Supply Chain Insights. Otherwise, during the Supply Chain Insights sign-up process you will be prompted to create an Azure AD tenant if your business does not already have one. 

>[!NOTE]
>You can also follow the steps in [Quickstart: Create a new tenant in Azure Active Directory](/fraud-protection/provision-azure-tenant#create-and-provision-a-new-tenant-in-azure-ad) to create and provision a new Azure tenant.

## Get started

After receiving an email invitation to join Supply Chain Insights as a user, follow these steps to get started.

1. Go to [sci.dynamics.com](https://sci.dynamics.com/) and follow the prompts to create and/or provision your Azure AD tenant. 
1. Accept the popup request asking for access to your location, which will be used to offer better suggestions as you search for locations in the next two steps.
1. Search for and select your company location. 
1. Search for and select your vendor location(s). 
1. Select **Get Started**. 
1. Complete the following three steps to provide the application with more information to deliver you accurate insights:
    1. [Import your data](ingestion.md).
    1. Complete your [Company profile](company-profile.md).
    1. [Create your supply chain network](partners.md).
