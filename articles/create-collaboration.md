---
title: Create a collaboration
description: This page contains information on how to create a data collaboration.
author: carylhenry
ms.date: 09/20/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---

# Metadata and Markdown template

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

Data sharing between you and your partners grants everyone greater visibility into their supply chains because the health of your supply chain is also dependent upon your suppliers and customers. Supply Chain Insights using data collaborations to make data sharing a straightforward process so it can then include partner data when generating insights to identify risks within all parts of your supply chain. Data collaborations enable you to request and share data with one or more partners.  Each partner in a collaboration will be able to see your data, and you will be able to see all of your partners' data. However, your partners won't be aware of what other companies are involved in the collaboration and can't see each other's data.


# Prerequisites

Before starting a collaboration, make note of what happens and can happen when you share your data with partners within Supply Chain Insights along with what responsibilities related to this data falls upon you and Microsoft to ensure this meets your companies' expectations.  When sharing data with partners, your data may be copied to a different region if you are sharing it with a partner who holds their Supply Chain Insights data in a different location from you. Additionally, partners may view and use your data within Supply Chain Insights and/or use your data outside of Supply Chain Insights by exporting the data you have shared with them. Please refer to Supply Chain Insight's terms and conditions to review your and Microsoft's responsibilities concerning data sharing.

Collaborations require connected partners who use Supply Chain Insights and ingested data to share with them.


# Create a data collaboration
A new data collaboration can be started in two ways. The first is by clicking the "New collaboration" button in the top left of the "Data collaboration" section. The second is by selecting "Partners" within the "All partners" tab of the "Partners" section and then clicking the three dots. After initiating a new data collaboration, a name must be entered, partners must be chosen, and some data must be specified before sharing the collaboration.
 
 ## Send a request
 ### Partners
 You can add one or more partners depending on if you created the collaboration within the data collaboration section or through the partners section accordingly. It is possible to add partners who are in other collaborations because  the same partner can join multiple collaborations simultaneously. Once added, clicking on a partner will cause a sidebar to appear where you can write an optional note. Different partners can receive different notes, all partners can receive the same note, and not all partners need to be sent a note. Notes will be seen by the partner as part of the invitation for the new data collaboration.


 ### Data requested
The Data requested step presents a list of data entities that can be requested using the toggles provided in the "Request to share?" column. How often you receive updated information for the data entities you are requesting can be seen under the "Requested schedule" column.  Clicking on an item in this column lets you edit how often you get the updated data.

![requested-entities-for-a-data-collaboration](/articles/media/data-collaboration-request-entities.PNG)

### Data shared
Data shared mirrors Data requested, except it determines what information you will give to your Partners and how often you will update that information.

### Documents
The Documents step is to share information that can't be captured within the data entities provided in the Data shared step. If no documents have been added, you can add documents by clicking the "Add files" button in the middle of the screen. Afterwards, you must select "Attach files" from the bar at the top of the page.

## Respond to a request
Partners may initiate a response to a data collaboration request through the email invitation, notification on their home screen, or the Partners' collaborations tab of the Data collaborations section. Data collaborations which have not been responded to under the collaborations tab will have "Not yet shared" for their entry under the "Data shared" column. 

### Data requested
Partners will be able to see what data entities you requested and choose to comply with those requests or decline them. Declining some data entries does not mean a Partner has declined the data collaboration completely.

### Data shared
Partners can see what information you will be sharing with them.

### Notes and documents
Partners can see what notes and documents you will share with them. They will also be able to respond with their own notes and documents

### Respond
A partner can click "Share data" or "Decline" in the upper right corner will send a response to your data collaboration request. Regardless of their response, Partners are able to include a comment before being brought back to the Partner's collaborations tab of the Data collaborations section. If the data collaboration was declined, then the collaboration will be removed from the list. If the data collaboration was accepted, then a percentage will appear under the "Data shared" column based on how much data the Partner shared in respect to how much data you requested.

# Sharing non-requested data
If you would like to volunteer information to your Partners, you can update one of the data collaborations under "My org collaborations" and add an additional data entity under "Data shared."
