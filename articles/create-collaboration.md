---
title: Create a collaboration
description: This topic describes how to create data collaborations in Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 10/14/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---

# Create a collaboration

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

This topic describes how to create data collaborations in Microsoft Dynamics 365 Supply Chain Insights.

The health of your supply chain is dependent upon your suppliers and customers, making data sharing between you and your partners vital for granting everyone greater visibility into their supply chains. Dynamics 365 Supply Chain Insights makes data sharing a straightforward process by creating data collaborations that can generate more insights about your supply chain by taking into account your partners' information.

## Prerequisites

Before starting a data collaboration, make note of what happens and what can happen when you share your data with partners within Supply Chain Insights. You should also determine what responsibilities related to the data falls upon you and Microsoft to ensure that you meet your company's expectations. When sharing data with partners, your data may be copied to a different region if you are sharing it with a partner who holds their Supply Chain Insights data in a different location from yours. Additionally, partners may view and use your data within Supply Chain Insights and/or use your data outside of Supply Chain Insights by exporting the data you have shared with them. To review your and Microsoft's responsibilities concerning data sharing, see [Supply Chain Insight's terms and conditions](https://aka.ms/scitc).

Collaborations require connected partners who use Supply Chain Insights, and ingested data to share with them.

## Create a data collaboration 

![demo for how to create a data collaboration with one partner](/articles/media/create-collaboration-example-flow.gif)

### Send a request
 
To start a new data collaboration, select **Data collaborations** in the left navigation pane, and then select **+New collaboration** in the command bar. After initiating a new data collaboration, you must enter a name for the collaboration, add a partner or partners, and specify which data should be shared before saving and sharing the collaboration.

### Add partners
 
You can add one or more partners depending on if you created the collaboration within the data collaborations page or through the partners section accordingly. It is possible to add partners who are in other collaborations because a partner can join multiple collaborations simultaneously. Once added, selecting the chat icon next to a partner's name brings up a sidebar where you can write an optional note. Different partners can receive different notes or all partners can receive the same note, and not all partners need to be sent a note. Notes will be seen by the partner as part of the invitation for the new data collaboration.

### Request data from partners

The "Data requested" tab presents a list of data entities that can be requested using the toggles provided in the "Request to share?" column. All, none, or some entities can be requested.

### Share data with partners

The format of the "Data shared" tab mirrors the "Data requested" tab, except it determines what information you will share with your partners instead of what information your partners will share with you.

### Respond to a request

You may respond to a data collaboration request through the email invitation, notification on the home screen, or the "Partners' collaborations" tab of the "Data collaborations" section. Data collaborations which have not been responded to under the "Partners' collaborations" tab will have a 0% visibility score and a "Decline" button in the top right once clicked. Beyond the "Decline" button, clicking on a data collaboration will show more information on what data is being shared.

### View the requested data and share your data

The **Data requested** tab of a partner's collaboration page contains a list of which data entities are requested, as well as which data entities you are sharing. It is not necessary to share all of the requested entities to accept a data collaboration request, and you can also share data not requested.

### View the data shared with you

The **Data shared** tab of a partner's collaboration page is similar to the **Data requested** tab, but it simply lists information about what data your partner is sharing with you in the data collaboration. If the partner is involved in other data collaborations with you they may already be sharing some of the data listed on this tab with you.

### View and add notes

The **Notes** tab contains notes sent from you and your partner to provide additional information such as the purpose of the data collaboration and why or why not some data has been shared.

### Send a response

After reviewing a data collaboration request, to send a response select **Share data** or **Decline** in the upper right corner. If you decide to decline a collaboration, that collaboration will then be removed from the **Partners** collaborations tab. If the data collaboration is accepted, a percentage will appear in the **Visibility score** column on the **Partners' collaborations** tab based on how much data you shared in relation to how much data was requested of you.
