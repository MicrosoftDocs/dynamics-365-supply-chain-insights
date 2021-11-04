---
title: Review, edit, and delete data collaborations
description: This topic describes how to review, edit, and delete data collaborations in Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 11/01/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---
# Review, edit, and delete data collaborations

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

This topic describes how to review, edit, and delete data collaborations in Microsoft Dynamics 365 Supply Chain Insights.

The data that you must know and the data that you must share with your partners can change over time. To accommodate these changes, you can review, edit, and delete data collaborations as required.

## Review and edit your organization's collaborations

Data collaborations that you create are listed on the **My organization's collaborations** tab of the **Data collaborations** page in Dynamics 365 Supply Chain Insights. Select a collaboration to review or edit it.

### Partners tab

The **Partners** tab lists partners who have been invited for a data collaboration or who have accepted an invitation. To remove a partner from a collaboration, select the vertical ellipsis button for that partner, and then select **Remove**. To add a partner to the set of partners that you specified when you first made a collaboration, select **Add partners** in the upper left.

### Data shared tab

The **Data shared** tab contains information about what data you're sharing with the partners in a collaboration. To update what data you're giving to your partners, update the checkbox values in the **Share?** column.

### Data requested tab

The **Data requested** tab contains information about what data you're requesting from the partners in a collaboration. To update what data you want from your partners, update the checkbox values in the **Request to share?** column.

### Delete collaborations

You can delete a collaboration on the **My organizations' collaborations** tab by selecting the collaboration and then selecting **Delete** in the upper left. Although you can delete your own collaborations, you can't delete your partners' collaborations.

## Review and edit your partners' collaborations

To review or change what data you're sharing in a partner's collaboration, first find the collaboration on the **Partners' collaborations** tab of the **Data collaborations** page. Then, on the **Data requested** tab, update the checkbox values in the **Share?** column. Finally, select **Save changes** in the upper right.

If you no longer want to share any data, you can clear all the checkboxes in the **Share?** column. Alternatively, you can completely leave the collaboration by selecting **Leave collaboration** in the upper left.

## Notes about deleting data

If data is deleted from a collaboration in Supply Chain Insights, the original source of the data that Supply Chain Insights ingested isn't affected. Data can be deleted from Supply Chain Insights when you remove requested entities from collaborations on the **My organization's collaborations** tab, or when you delete one of those collaborations. In a similar way, data can be deleted when you stop sharing entities among collaborations that are listed on the **Partners' collaborations** tab, or when you leave one of those collaborations.

> [!NOTE]
> When you delete data by choosing to no longer ingest it in Supply Chain Insights, by deleting it in the original data source and refreshing the data within Supply Chain Insights, or by choosing to no longer share data with your partners, it may take as long as 48 hours for Supply Chain Insights stop making the data available to partners who you previously shared the data with.
