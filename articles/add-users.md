---
title: Add users to Supply Chain Insights
description: Instructions for how to add users to an instance of Dynamics 365 Supply Chain Insights
author: carylhenry
ms.date: 01/19/2022
ms.topic: article
audience: Application Use
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---

# Add users to Supply Chain Insights

Multiple users from the same company can access the same instance of Supply Chain Insights (SCI), but a four-step process must be followed to give these users access. You must (1) add users to your Azure Active Directory (AAD) tenant, (2) assign them a license with OneDrive access, (3) initialize their OneDrive licenses, and (4) add them within the SCI application. 

## Add users to your AAD tenant

Go to portal.azure.com and select **Azure Active Directory** or use the search bar. This will present you with the **Overview** page of your AAD tenant.

<!--![Top part of the Azure portal home page that includes the search bar and featured capabilities](media/AzurePortalHomePageWithSearchBar.png)-->

Make sure you are in the same AAD tenant as the one being used for SCI. You can change your tenant by going to **Manage tenants** and select the correct one. To add a user to the correct AAD tenant, select **Add** then choose **User** from the dropdown menu on the **Overview** page.

<!--![Dropdown menu for the Add function on the overview page of an AAD tenant](media/AADTenantAddUserDropdown.png)-->

Enter the information necessary for a new user and select **Create**. 

>[!NOTE]
> Ensure for each added user that their usage location is set to United States. You can check this by clicking the new user from the **Users** section of your AAD tenant and looking at the **Settings** section of the **Profile** tab. If the location is not the United States, select **Edit** in the top left to make the update.
 
<!--![Dropdown menu for the Add function on the overview page of an AAD tenant](media/AADTenantUserProfile.png)-->

## Assign users a license with OneDrive access

Access to OneDrive is necessary for users so they can import data within SCI. This access should be granted from your AAD tenant. From your tenant's **Overview** page, go to **Licenses > All products** before choosing a license that includes OneDrive (such as Office 365 or Microsoft 365) and clicking **Assign**.

<!--![The "All products" section of the licenses for a single AAD tenant](media/AADTenantLicensesPage.png)-->

Next, select **Add users & groups**. This will open a side panel of users that can be assigned the license. Make sure the users you wish to join SCI are in this list before clicking **Select** to close the side panel and then **Review + assign** to complete this step.
 
<!--![Selecting which AAD tenant users should be assigned a specific license](media/SelectingAADTenantUsersForLicense.png)-->

## Initialize users' OneDrive license

The previous step gave users access to OneDrive, but their OneDrive license must be initialized first for them to import data within SCI. To initialize a user's license, navigate to [https://onedrive.live.com/](https://onedrive.live.com/) and sign into OneDrive as the new user. Their user principal name and password from the AAD tenant should be used as their credentials here, and you will be prompted to update their passwords if you just added them to your tenant. The account should automatically set up after signing into OneDrive.

## Add users through SCI's user management

As an SCI admin, log into the application and go to the **User management section**. Select **Invite user** and add the users which were added to your AAD tenant, assigned Office 365 licenses, and had OneDrive accounts initialized to complete this process.

<!--![Adding new users from the "User management" section of Dynaimcs 365 Supply Chain Insights](media/AddingUsersInSCI.png)-->

