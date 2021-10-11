---
title: Review, export, and delete
description: This page contains information on how to review, edit, delete, and export data in Supply Chain Insights
author: carylhenry
ms.date: 09/01/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

Reviewing, exporting, and deleting data gives you the power to make sure that the data you have ingested is correct and is mapping to the correct entities and attributes in within Supply Chain Insights in order to derive maximum benefits through analytics and data modeling. 

# Prerequisites
Data management requires that you have already ingested your data either manually from your computer or from your data storage into Supply Chain Insights.

# Review
Review the ingested data for a given entity by clicking the entity name  on the main "Data import" page or choosing "View data" from the contextual menu for a given entity. This displays a new page with a table containing all the data Supply Chain Insights has for the attributes of that entity. The panels on the righthand side contains tools for customizing the data to see and understand what has been ingested. Any interactions with the side panels are not saved, so they will not edit your data. Read [Power BI's documentation](https://docs.microsoft.com/en-us/power-bi/create-reports/service-the-report-editor-take-a-tour) to get a deeper dive on what is possible with these tools.


# Export
Data export allows you to download ingested data in excel for further analytics or partner collaboration outside the scope of Supply Chain Insights by letting you use the data for further analytics elsewhere. The format of the data will mirror what is seen in data review. To export the data for an entity from Supply Chain Insights, review the data as explained above.  Click the contextual menu on the top right of the table and select "Export data." This brings up a dialogue where you can choose to download the data as a XLSX or CSV file.
![reviewing and then exporting data](/articles/media/data-export.gif)

# Delete
Data delete helps you delete an entity or delete all entities that were ingested in Supply Chain Insights. If you saw an issue or error in the ingested data such as an incorrect data mapping or incorrect ingested data, delete capability allows you to delete the incorrected data and re ingest the data. This enables correct data for correct insights while letting users protect their privacy and security. Currently, users are only able to delete all entries for an entity. They can do this for a single entity or multiple entities at once by selecting one or multiple entities in the "Data import" page. Additionally, all data for all data entities can be removed using the "Delete all data" button in the top left of the "Data import" section of the application. Please note that data delete will take 24-48 hours to complete.
