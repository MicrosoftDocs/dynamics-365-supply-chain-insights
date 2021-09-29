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

# Prerequisites
Data management requires that you have data in a cloud storage solution that has data to ingest according to the entities described in [Data entities](/articles/entities.md).

Please review the "Data resiliency, compliance, and security" page of this documentation before ingesting your data to ensure that Supply Chain Insights meets your company's expectations.

# Getting started
Select an entity from the "Data import" page which has a "Not imported" status. Afterwards, select "Not imported" or open the contextual menu and choose "Import data."

# Sources

Import a local CSV or XLS file from your computer or connect Supply Chain Insights to a cloud storage service to populate the data for any entity. Make sure your data contains the required attributes of a given entity for both methods. Additional information will be required to authenticate Supply Chain Insight's access to the data depending on the cloud storage service selected or the column headers must be named if you upload a local file.

# Mapping
Mapping informs Supply Chain Insights how to interpret your data so it can be analyzed. More specifically, a mapping explains how your data relates to the attributes which represent a certain entity and is easy to complete during the ingestion process. 
## Local files
Local files must have column headers because Supply Chain Insights uses the headers to map your data to the attributes of the entity. More specifically, Supply Chain Insights will attempt to determine which column represents what attribute by using the column headers when you click "Auto map." Check the "Mapped attributes" column along with the "Data preview" table at the bottom of the page to make sure the auto-mapping was correct. If there was an error, or you would prefer to manually do the mapping, select the dropdown menu in the "Mapped attributes" column for the required attribute of interest and choose the appropriate column header name.

## Cloud storage
If a table representing the desired entity is readily available, simply select it from the left hand column once a data source has been selected. If not, the Power Query interface contains many tools to transform your data into a single table representing the entity. More information on these tools and how to use them can be found within the sub-articles of the "[Transform data](https://docs.microsoft.com/en-us/power-query/power-query-ui)" section of Power Query's documentation. Once a table containing all of the information for the entity has been created, Power Query can automatically map the information in your table to the attributes of the entity by selecting "Map to entity" in the top right, choosing the entity of interest from the left hand column in the popup window, and then selecting "Auto map." Check the query output column for any errors or manually map your data using this column before selecting "Done."

![mapping for importing data from a cloud storage solution](/articles/media/cloud-storage-ingestion.PNG)
# Refresh schedule
Up-to-date insights are reliant upon up-to-date data ingestion, which can be completed in three ways. A refresh schedule automatically updates the ingested data for a given entity based on any changes made to that data within your cloud storage solution. Entities connected to a cloud storage solution can also be updated by selecting "Refresh now" from their dropdown menu on the "Data import" page. This is also where you can change a refresh schedule, stop it, or disconnect the entity from the data source entirely. The final way to update the data for an entity is to complete the data ingestion process descried above. 
