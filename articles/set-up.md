---
title: Requirements and set up
description: This page contains requirements for using Supply Chain Insights and instructions for setting it up.
author: carylhenry
ms.date: 08/30/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---


[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]




# Requirements

Supply Chain Insights requires access to an existing email account. If you don't have one, then you can create one at www.outlook.com. 

A sign up url with an unused offer code is necessary to provision and use Supply Chain Insights. These are provided by the Supply Chain Insights product team. If you don't have one already, you can contact (scvquestions@microsoft.com). The code should look something like: 

https://signup.microsoft.com/create-account/signup?products=83d3609a-14c1-4fc2-a18e-0f5ca7047e46&pc=YOUR_PRODUCT_CODE

An Azure Active Directory tenant is also needed. An Azure represents an organization within Microsoft Azure Active Directory. It is a dedicated instance of the Azure AD service that an organization receives and owns when it signs up for a Microsoft cloud service such as Azure, Microsoft Intune, or Microsoft 365. Essentially, an Azure tenant is a way to manage user access to Azure resources to ensure you control access to your data. Contact your AAD Tenant Admin or IT department and have them sign up for SCI if your business already has an AAD tenant. Otherwise, you will be prompted during the sign up process for SCI to create an AAD tenant if your business does not already have one. You can also follow the steps in [Quickstart: Create a new tenant in Azure Active Directory](https://docs.microsoft.com/en-us/dynamics365/fraud-protection/provision-azure-tenant#create-and-provision-a-new-tenant-in-azure-ad) to create and provision a new Azure tenant.

The AzureAD PowerShell package must be installed on your machine because the admin for the AAD tenant will need it to authenticate Supply Chain Insights. If you created the tenant, then you are the tenant admin. If you did not create the tenant, you can talk to your IT department to find out who the tenant admin is for your company.


# Set up

## Configure your Azure Active Directory

1. Open a web browser and navigate to your sign up URL
2. Fill out the form. If your company already has an Azure Active Directorytenant, then the tenant admin must perform this step. If you don't have an Azure Active Directory tenant, a new one will be created for you as part of this step 
3. Open the PowerShell command prompt, selecting "Run as Administrator"
4. Run the following command: ``` az login ```
5. Login using the AAD tenant admin's credentials
6. Run the following command: ```New-AzureADServicePrincipal -AppId d6037e40-282c-493d-8f63-f255e36c6ef4```
7. Open a browser and login to the Azure portal
8. Go to your Azure Active Directory
9. Click on Enterprise Applications, select "All Applications" from the drop down filter, and search for "Microsoft Dynamics 365 Supply Chain"
10. Click on the link to Microsoft Dynamics 365 Supply Chain Insights  and select "Users And groups" option from the left hand menu then select the "Add user/group" button
11. Pick the user whom you want to allow access to Supply Chain Insights add then click the "Select" button
12. Next click on the "Assign" button
13. Go to your tenant properties by click on the name of your tenant in the upper-left-hand corner
14. Next click on "Properties" and copy the tenant ID and save it as you will need it for the next step
15. Email the Supply Chain Insights product team to inform them that your pre-requisite setups are complete at scvquestions@microsoft.com. Include your tenant Id in the body of the email
16. Wait until you get a response back saying that your tenant is ready


## Get started
1. Go to [PROD-Supply Chain Visibility](https://scv.azureedge.net/#code=0.ARoAv4j5cvGGr0GRqy180BHbR0B-A9YsKD1Jj2PyVeNsbvQaAKk.AQABAAIAAAD--DLA3VO7QrddgJg7Wevr231httP_cXi2yBbPqOdufAklnXRlDyNsg-INetruJ71vOph4VJKSjMuwXsko5pRY9dXrJJuDXAq_mdBUPUM4ehjj7hlfIo6M3pZSzx65cjan8JJ_ansitrNQ1fq5_7Yw4KpN0rMKmyUGWnlLwIwkWrLtSsLIT8fszfDS3FpC6TVzEaQ7yB-cBrbBOKfaLsR94NTRa0QjB_buwQS8e8hn4AD0HP_k4yfhQLl1I2me0m5qUWa2H4-xi6kDsgTmxqiySlfkczfjGLNZo4SWepK3ea4aLT8gH7zrwjQjZw-aHgbkr21aZCbOaRu96RsOpUMj2in2S_p8L_KD-mETZO3qETSCC1-3ts-qolfRiwesRFNnHRX_pROqYP1NngZmb741VIUN9D2VCqhLilMrwbO4Pe2-efYtcQQ2US5sMG79vUUiohMm_GMLXoReiTiakJaupEcXuH_dSt7UReYMyH_gRc1h1NiENgVNGfeQYfTQqXtHtwXMyaDZT4VVcDdFzaVXM_O7btFaXMWqg3cNfnFHFtKZGtyXuQyrlyINZR-Tm0VnPXMdVadxNs0rxqy_4S6c9dp1t3bWGSc5vo8zibLlA4gWZ178u4eoBJZ3iDjBWlBHpF2-ccfkvcUWPFf-p2ljBcDsON-vlxMpJdeJd2Bth6Mc9wcafUsD4jwyGOWEgrvzTa7-OD6NwdMjMG9D2GzjPBepPyTFVgNYfMZDuMPvwq1r5sGynOkLmenLCmMTLEGgOPDle1RajPKMzZ6ngGLwEcCPiB3avB-jkKdQp70NZzxI55KscuxU5RiwLM6bSJIf3CgdB7CX1iztnphX2XBoiQZ1kv9qPo2GMCTkklM-MKJxYEkurpLtaMwKpHt4vSy0n6gsCG3IIQbpGpgxJWSoIAA&client_info=eyJ1aWQiOiIyNDEwY2E2ZC1jYjlkLTRkNWEtYWNlNy0yMTZhZjk4MTljOWMiLCJ1dGlkIjoiNzJmOTg4YmYtODZmMS00MWFmLTkxYWItMmQ3Y2QwMTFkYjQ3In0&state=eyJpZCI6IjRkN2E1ZDJjLWRiYzItNDc5OC05MWNmLTZhYWY0NmFiZDc1NSIsInRzIjoxNjMwNDQ5NzMxLCJtZXRhIjp7ImludGVyYWN0aW9uVHlwZSI6InJlZGlyZWN0In19&session_state=cd905fda-f260-4b2b-b04b-6457dac81886) 
2. Accept the popup request asking for access to your location. This will be used to offer better suggestions as you search for locations in the next two steps
3. Search for and select your company location
4. Search for and select your vendor location(s)
5. Click the "Get Started" button


## Import PowerApps solutions
1. Open another browser and go to  https://make.powerapps.com/ 
2. Choose the environment on the right hand side of the UX named SCVN<TenantGuid> 
3. Click the Solution tab on the left pane.
4. Download the following zipped solution file: 
5. Go to the PowerApps portal and then click import. 
6. Import S2SApplicationRoles_managed **and then** import MicrosoftS2SApplicationIdentities_managed

## Complete onboarding
1. Return to [PROD-Supply Chain Visibility](https://scv.azureedge.net/) and login to see the supply chain map and news suggestions on the home page that are based upon the locations provided in the "Getting started" section above
2. Complete the three steps displayed in the onboarding section of Supply Chain Insight's home page to provide the application with more information to deliver you accurate insights. These three steps are [import your data](link to Data Management), complete your [company profile](link to Settings), and [connect with partners](link to Partners & Network Creation)
