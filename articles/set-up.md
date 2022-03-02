---
title: Set up Supply Chain Insights
description: This topic describes the requirements and instructions for signing up for and setting up Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 03/02/2022
ms.topic: article
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global

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
- Supply Chain Insights supports only the most recent and second most recent versions of the Microsoft Edge, Chrome, Firefox, and Safari browsers. Also, ensure that WebGL is activated in your browser's settings.
- An Azure Active Directory (Azure AD) tenant is required. A tenant represents an organization in Azure AD and lets you manage user access to Azure resources to ensure controlled access to your data. You can sign up for a free [Microsoft 365 trial](https://www.microsoft.com/microsoft-365/try) that includes an Azure AD tenant. We recommend using a personal email address to sign up for the free trial instead of a school or work account to guarantee that the email is not already associated with an Azure AD tenant. You should then use the email address that is associated with your Microsoft 365 trial to sign up for Supply Chain Insights.
    > [!NOTE]
    > Free trials end after one month and require credit card information to help ensure that you don't experience any interruptions when your trial ends. Your credit card won't be billed until the end of the trial period. You can cancel at any time during the trial period by selecting **Turn off recurring billing** on your [Microsoft account](https://go.microsoft.com/fwlink/p/?LinkID=401325&CLCID=0x409&culture=en-us&country=US) page.
- If your company is already a Power Platform user, check your administrator setting to make sure that every user in the tenant can create trial environments. [Control environment creation and management - Power Platform | Microsoft Doc](https://docs.microsoft.com/en-us/power-platform/admin/control-environment-creation) contains two approaches for changing the setting. You can either go through the Microsoft Power Platform admin center to let every user in the tenant create trial environments or use their PowerShell instructions. If you use the PowerShell instructions, change the `DisableEnvironmentCreationByNonAdminUsers` setting to `$false` instead of `$true`. This setting can be changed back to `true` once you've onboarded to Supply Chain Insights.

## Onboarding

After you receive an email invitation to join Supply Chain Insights as a user, follow these steps to get started with onboarding.

1. Select the sign-up link that is provided in your invitation email. Once you've used this link to sign up and onboard, please use [sci.dynamics.com](https://sci.dynamics.com/) to access Supply Chain Insights going forward.
1. Choose where your data will be stored. Data can be stored only in the United States for the public preview release, but there are plans to expand the list. 
1. Enter a company name and a team name. The combination of the two must be unique. 
1. Once your tenant is provisioned, accept the request for access to your location. This access will be used to offer better suggestions as you search for locations in the next two steps.
1. Search for and select your company location.
1. Search for and select your vendor and customer locations. You can enter multiple locations.
1. Select **Get Started**.
1. Follow these steps to provide additional information to Supply Chain Insights. This information will help the application deliver accurate insights to you.

    1. [Import your data](ingest-data.md).
    1. Complete your [Company profile](company-profile.md).
    1. [Create your supply chain network](partners.md).
