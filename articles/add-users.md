---
title: Add users to Supply Chain Insights
description: This topic describes how to add users to an instance of Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 01/25/2022
ms.topic: article
audience: Application Use
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---

# Add users to Supply Chain Insights

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

This topic describes how to add users to an instance of Microsoft Dynamics 365 Supply Chain Insights.

Multiple users from the same company can access the same instance of Supply Chain Insights (SCI), but you must follow a four-step procedure to give these users access. 

To give multiple users access to the same instance of Supply Chain Insights, follow these steps.

1. Add users to your Azure Active Directory (AAD) tenant.
1. Assign them a license with OneDrive access. 
1. Initialize their OneDrive licenses.
1. Add them within the SCI application. 

## Add users to your Azure AD tenant

To add users to your Azure AD tenant, follow these steps.

1. Go to the [Azure portal](https://portal.azure.com) and sign in.
1. Search for and then select **Azure Active Directory**. The **Overview** page of your Azure AD tenant appears.
1. Confirm that you are in the same Azure AD tenant as the one being used for SCI. You can change your tenant by selecting **Manage tenants** and then selecting the desired tenant. 
1. To add a user to the correct Azure AD tenant, on the **Overview** page select **+Add**, and then select **User** from the dropdown menu.
1. Enter the new user's information, and then select **Create**. 

>[!NOTE]
> Ensure that each added user's location is set to **United States**. You can check this in your Azure AD tenant by selecting **User** in the left pane, selecting the new user from the list, and then checking the **Usage location** field in the **Settings** section of the **Profile** tab. If the location listed is not the United States, select **Edit** in the top left to update the **Usage location** value.

## Assign users a license with OneDrive access

Users must have access to OneDrive so that they can import data within SCI. This access should be granted from your Azure AD tenant.

To assign users a license with OneDrive access, follow these steps.

1. Go to the [Azure portal](https://portal.azure.com) and sign in.
1. On your tenant's **Overview** page, select **Licenses** in the left pane. 
1. On the **Licenses** page, select **All products** in the left pane.
1. Select a license from the list that includes OneDrive (such as Office 365 or Microsoft 365), and then select **Assign**.
1. On the **Assign license** page, select **Add users and groups**. A side pane appears listing users that can be assigned the license. 
1. Confirm that the users you wish to join SCI are in this list, and then select **Select** to close the side pane.
1. Select **Review + assign**.

## Initialize a user's OneDrive license

After assigning a user a license to access to OneDrive, the user's OneDrive license must then be initialized for them to be able to import data within SCI. 

To initialize a user's license, follow these steps.

1. Go to the [Microsoft OneDrive home page](https://onedrive.live.com/) and sign into OneDrive as the new user, using the principal name and password from the Azure AD tenant as their credentials. 
1. You will be prompted to update the user's password if you just added them to your tenant. After updating the user's password, the account should automatically be set up after signing into OneDrive.
1. Repeat the preceding steps for each additional user that needs to be initialized. 

## Add users using SCI's user management functionality

To add a user using SCI's user management functionality, follow these steps.

1. As an SCI admin, sign in to the application and go to the **User management section**. 
1. Select **Invite user** to add any user that has already:
    - Been added to your Azure AD tenant.
    - Been assigned an Office 365 license.
    - Had their OneDrive license initialized.
