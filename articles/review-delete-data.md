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

Reviewing, exporting, and deleting data gives you the power to make sure that the correct data is within Supply Chain Insights in order to be analyzed and is portable if further analysis needs to be completed outside of the application.

Prerequisites
Data management requires that you have data in a cloud storage solution that has already been ingested.

# Review
Review the ingested data for a given entity by clicking on the name of that entity on the main data import page. 
This displays a new page with a table containing all the data Supply Chain Insights has for the attributes of that entity.

# Export
Data export and download enables further analytics or partner collaboration outside the scope of Supply Chain Insights by letting you use the data for an entity elsewhere. The format of the data will mirror what is seen in data review. To export the data for an entity from Supply Chain Insights, review the data as explained above.  Click the contextual menu on the top right of the table and select "Export data." This brings up a dialogue where you can choose to download the data as a XLSX or CSV file.

![reviewing and then exporting data](/articles/media/data-export.gif)

# Delete
Data delete helps you resolve an issue or error in the ingested data such as an incorrect data mapping or incorrect ingested data. This enables correct data for correct insights while letting users protect their privacy and security. Currently, users are only able to delete all entries for an entity. They can do this for a single entity or multiple entities at once by selecting one or multiple entities in the "Data import" page. Additionally, all data for all data entities can be removed using the "Delete all data" button in the top left of the "Data import" section of the application. Please note that data delete will take 24-48 hours to complete.
