---
title: Partner management
description: This topic includes information on anaging partners in Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 10/08/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry

---

# Partner management

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

With Dynamics 365 Supply Chain Insights, you can connect with your vendors and customers to share data and gain greater visibility into your supply chain. You can invite your existing vendors and suppliers to connect in Supply Chain Insights, or find new partners to connect with. Partners that are connected in Supply Chain Insights can collaborate and share data with you. 

You should complete your [company profile](company-profile.md) before you add partners. Supply Chain Insights will suggest partners based on the data you import and your company's industry. 

![find partners tab with filter](/articles/media/find-partners-with-filter.PNG)

## Find and connect with partners
When you connect with a partner, your contact email address and any other data provided in the **General information** section of your company profile is shared with the partner. 

To diplay a list of companies who have joined Supply Chain Insights, go to **Partners > All partners > Find partners**. Select a partner name or card to display the partner's company profile. To request to connect to a partner, select **Connect** on the partner card. When you make your request, you can add a customized note to personalize your request. 

You can use the search field and filters to find specific partners. If the partner you're looking for isn't found, you can invite them to join Supply Chain Insights by selecting **Invite partners** on the upper left side of the page. You may need to have the company name, vendor ID, DUNS number, and contact email to manually add them.
 
The status of your request is displayed under the pending invitation on the **Sent requests** tab.
 
## Invite existing vendors and customers to connect
In addition to connecting with new partners, you can invite and connect with your existing vendors and customers in Supply Chain Insights. You can invite your partners from the **Find Partners** tab or from the **Imported** tab. You can invite customers and vendors that you previously [imported to Supply Chain Insights](/articles/ingestion.md), or invite a single partner that was not imported. When you invite a vendor or a customer, you can add a customized note to personalize your request. 
 
If a partner you are connecting with already exists in your ERP system as a vendor or customer, you can identify them by setting the **Relationship** field on the **My partners** tab, and add their vendor ID or customer ID. The **Relationship** value and any vendor or customer ID you provide will not be visible to the partner. 

After you select **Invite**, an email invitation is sent to your customer or vendor from a Microsoft mailbox. You should let your partners know that they should expect an email from Microsoft, as it might be routed to their spam folder. After the partner joins Supply Chain Insights, they will receive a   connect request from your participant. After they accept the request, they can collaborate and share data. 

The status of your request is displayed under the pending invitation on the **Sent requests** tab.

## Imported partners
The **Imported** tab displays a list of companies that haven't joined Supply Chain Insights but have been detected based on your ingested data for customer and vendor entities. You can import additional partners by selecting **Import partners** on the upper left side of the page. You can invite any of these customers and vendors to join Supply Chain Insights and connect with you.

## Incoming requests
The **Incoming requests** tab displays requests from partners to connect with them. You can choose to accept or decline the requests on this tab. Once you connect with a partner, you can find the partner on the **My partners** tab.

## Sent requests
The **Sent requests** tab displays the status of requests that haven't been accepted. The requests will be listed as "Pending" or "Declined". Once a request is accepted, the company will be listed on the **My partners** tab. 

## Manage connections
The **My partners** tab contains a list of companies you have connected with using Supply Chain Insights. You can manage your relationship, [start a new data collaboration with them](/articles/create-collaboration.md), [view the collaborations that have been established with them](/articles/review-edit-delete-collaboration.md), and view the general information included in their company profile.
