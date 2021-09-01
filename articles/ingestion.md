---
title: Ingestion
description: This pge contains information for how users ingest data for Supply Chain Insights
author: carylhenry
ms.date: 09/01/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---

Microsoft Dynamics 365 Supply Chain Insights needs data relevant to your supply chain in order to generate insights relevant to your business. 
To bring that data into the application, Supply Chain Insights leverages [Power Query](https://docs.microsoft.com/en-us/power-query/power-query-what-is-power-query) for a smooth data ingestion experience.

# Sources

Import a local .csv file from your computer or connect Supply Chain Insights to a cloud storage service to populate the data for any entity. 
Make sure your data contains the required attributes of a given entity schema and that you have the information on hand to authenticate Supply Chain Insight's access to the data.

# Mapping
Mapping tells Supply Chain Insights how to interpret your data so it can be analyzed. 
More specifically, a mapping explains how your data relates to the attributes that represent a certain entity and is easy to complete during the ingestion process. 
Simply choose the table representing the desired entity from the left hand column once a data source has been selected. 
Power Query can automatically map the information in your table to the attributes of the entity by selecting "Map to entity" in the top right, choosing the entity of interest from the left hand column in the popup window, and then selecting "Auto map." 
Check the query output column for any errors or manually map your data using this column before selecting "OK."

# Refresh schedule
Up-to-date insights are reliant upon up-to-date data ingestion, which can be completed in two ways. 
A refresh schedule automatically updates the ingested data for a given entity based on any changes made to that data within your cloud storage solution. 
As such, a refresh schedule is only available for data that is ingested from a cloud storage solution. 
Entities reliant upon local files must be updated by repeating this data ingestion process. 

