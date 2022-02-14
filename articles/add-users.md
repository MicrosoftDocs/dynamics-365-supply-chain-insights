---
title: Add users to Supply Chain Insights
description: This topic describes how to add users to an instance of Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 01/25/2022
ms.topic: article
audience: Application Use
ms.reviewer: v-chgriffin
ms.search.region: Global

ms.author: carylhenry
---

# Add users to Supply Chain Insights

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

This topic describes how to add users to an instance of Microsoft Dynamics 365 Supply Chain Insights.

Multiple users from the same company can access the same instance of Supply Chain Insights, but you must first give them access to it.

To give multiple users access to the same instance of Supply Chain Insights, complete this four-step procedure.

1. Add users to your Azure Active Directory (Azure AD) tenant.
1. Assign them a license that has OneDrive access. 
1. Initialize their OneDrive licenses.
1. Add them in the Supply Chain Insights application. 

## Add users to your Azure AD tenant

To add users to your Azure AD tenant, follow these steps.

1. Go to the [Azure portal](https://portal.azure.com), and sign in.
1. Search for and select **Azure Active Directory**. The **Overview** page of your Azure AD tenant appears.
1. Confirm that you're in the same Azure AD tenant that is being used for Supply Chain Insights. You can change the tenant by selecting **Manage tenants** and then selecting the desired tenant. 
1. To add a user to the correct Azure AD tenant, on the **Overview** page, select **Add**, and then select **User** on the drop-down menu.
1. Enter the new user's information, and then select **Create**. 

> [!NOTE]
> Make sure that the location for each user that you add is set to **United States**. To confirm this setting in your Azure AD tenant, select **User** in the left pane, and select the new user in the list. Then, on the **Profile** tab, in the **Settings** section, review the value of the **Usage location** field. If the value isn't **United States**, select **Edit** in the upper left to update it.

## Assign users a license that has OneDrive access

Users must have access to OneDrive so that they can import data in Supply Chain Insights. This access should be granted from your Azure AD tenant.

To assign users a license that has OneDrive access, follow these steps.

1. Go to the [Azure portal](https://portal.azure.com), and sign in.
1. On your tenant's **Overview** page, select **Licenses** in the left pane. 
1. On the **Licenses** page, select **All products** in the left pane.
1. In the list, select a license that includes OneDrive (such as Office 365 or Microsoft 365), and then select **Assign**.
1. On the **Assign license** page, select **Add users and groups**. The dialog box that appears lists the users that can be assigned the license. 
1. Confirm that the users that you want to join Supply Chain Insights are in the list, and then select **Select** to close the dialog box.
1. Select **Review + assign**.

## Initialize a user's OneDrive license

After you assign a user a license that has access to OneDrive, the user's OneDrive license must be initialized so that the user can import data in Supply Chain Insights. 

To initialize a user's license, follow these steps.

1. Go to the [Microsoft OneDrive home page](https://onedrive.live.com/), and sign in to OneDrive as the new user. Use the principal name and password from the Azure AD tenant as the user's credentials. 
1. If you just added the user to your tenant, you're prompted to update their password. After you update the user's password, the account should automatically be set up after sign-in to OneDrive.
1. Repeat the preceding steps for each additional user whose license must be initialized. 

## Add users by using the user management functionality in Supply Chain Insights 

To add a user by using the user management functionality in Supply Chain Insights, follow these steps.

1. Sign in to Supply Chain Insights as a Supply Chain Insights admin.
1. In the **User management** section, select **Invite user** to add any user that meets these criteria:

    - They have been added to your Azure AD tenant.
    - The have been assigned an Office 365 license.
    - Their OneDrive license has been initialized.
