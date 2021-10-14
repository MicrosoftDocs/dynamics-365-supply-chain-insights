---
title: Review, export, and delete data
description: This topic describes how to review, edit, delete, and export data in Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 10/14/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---

# Review, export, and delete data

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

This topic describes how to review, edit, delete, and export data in Microsoft Dynamics 365 Supply Chain Insights.

Reviewing, exporting, and deleting data in Dynamics 36 Supply Chain Insights can help you derive maximum benefits through analytics and data modeling by confirming that the data you have ingested are valid and mapping to the correct entities and attributes within the application. 

## Prerequisites

Data management requires that you have already ingested your data into Supply Chain Insights either manually from your local computer or from your data storage provider.

## Review the ingested data

Review the ingested data for a given entity by selecting the entity name on the main **Data import** page, or selecting **View data** from the vertical ellipsis contextual menu of a given entity. This displays a new page with a table listing all the data Supply Chain Insights has for the attributes of that entity. The panes on the right side contain tools for customizing data to see and understand what has been ingested. Any interactions with the side panes are not saved, so they will not edit your data. For more information on what is possible with these tools, see [Tour the report editor in Power BI](/power-bi/create-reports/service-the-report-editor-take-a-tour).

## Export data

Data export allows you to download ingested data in Microsoft Excel format for further analytics or partner collaboration outside the scope of Supply Chain Insights. The format of the data will mirror what is seen when reviewing the data in Supply Chain Insights. To export data for an entity from Supply Chain Insights, review the ingested data, select the contextual menu on the top right of the table, and then select **Export data**. This brings up a dialog box where you can choose to download the data as a XLSX or CSV file.

![reviewing and then exporting data](/articles/media/data-export.gif)

## Delete data

Data deletion enables you to delete an entity or all entities that have been ingested into Supply Chain Insights. If you see an issue or error in the ingested data such as an incorrect data mapping or incorrect data, the data deletion functionality allows you to delete incorrect data and then reingest the data. Currently, users are only able to delete all entries for an entity. To do this for a single entity or multiple entities at once, select one or multiple entities on the **Data import** page. Additionally, all data for all data entities can be removed by selecting **Delete all data** on the top left of the **Data import** page. 

> [!NOTE]
> It can take up to 48 hours for data deletion to take effect.
