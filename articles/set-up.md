---
title: Set up Supply Chain Insights
description: This topic describes the requirements and instructions for signing up for and setting up Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 11/02/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---

# Set up Supply Chain Insights

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

This topic describes the requirements and instructions for signing up for and setting up Microsoft Dynamics 365 Supply Chain Insights.

## Sign up for the public preview

You can sign up for the public preview release on the [Supply Chain Insights page](https://dynamics.microsoft.com/supply-chain-insights/). Supply Chain Insights uses a gated process to enroll new public preview users. Once you sign up, you will be invited to onboard on a rolling basis. Other customers may be invited to onboard if an invitation is sent from a company that is already a public preview user. Users that signed up or were invited by a public preview user will receive an email with details on how to register. 

## Prerequisites

- Supply Chain Insights is currently available only in the English, German, and simplified Chinese languages.
- Supply Chain Insights supports only the most recent and second most recent versions of the Microsoft Edge, Chrome, Firefox, and Safari browsers. Please make sure that WebGL is also activated in your browser's settings.
- An Azure Active Directory (Azure AD) tenant is required. A tenant represents an organization in Azure AD and lets you manage user access to Azure resources to ensure controlled access to your data. If your business already has an Azure AD tenant, contact your Azure AD tenant administrator or IT department, and have them sign up for Supply Chain Insights.

    > [!NOTE]
    > You can also follow the steps in [Quickstart: Create a new tenant in Azure Active Directory](/fraud-protection/provision-azure-tenant#create-and-provision-a-new-tenant-in-azure-ad) to create and provision a new Azure AD tenant.

## Get started

After you receive an email invitation to join Supply Chain Insights as a user, follow these steps to get started.

1. Use the link provided in your email or go to [https://sci.dynamics.com/](https://sci.dynamics.com/).
1. Choose where your data will be stored. Data can be stored only in the United States for the public preview release, but there are plans to expand the list. 
1. Enter a company name and a team name. The combination must be unique. 
1. Once your tenant is provisioned, accept the request for access to your location. This access will be used to offer better suggestions as you search for locations in the next two steps.
1. Search for and select your company location.
1. Search for and select your vendor and customer locations. You can enter multiple locations.
1. Select **Get Started**.
1. Follow these steps to provide additional information to Supply Chain Insights. This information will help the application deliver accurate insights to you.

    1. [Import your data](ingest-data.md).
    1. Complete your [Company profile](company-profile.md).
    1. [Create your supply chain network](partners.md).
