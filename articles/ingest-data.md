---
title: Ingest data
description: This topic describes how to ingest data into Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 10/14/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---

# Ingest data

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

This topic describes how to ingest data into Microsoft Dynamics 365 Supply Chain Insights.

To generate insights relevant to your business, Dynamics 365 Supply Chain Insights needs data relevant to your supply chain. To bring that data (in other words, *ingest* it) into the application, Supply Chain Insights uses [Microsoft Power Query](/power-query/power-query-what-is-power-query) to help deliver a smooth data ingestion experience.

## Prerequisites

Data management requires that you ingest data from various sources according to the entities described in [Data entities](entities.md). For example, a Microsoft Excel file can contain data that can be used for the vendor, warehouse, production plant, bill of materials, and product entities. While it may not contain all the attributes for every entity, this data would be sufficient because it includes the required attributes for each of the entities.

Before ingesting your data, to ensure that Supply Chain Insights meets your company's expectations, review [Data resiliency, compliance, and security](resiliency-compliance-security.md).

## Get started

To get started ingesting data, go to the **Data import** page and select an entity that does not have a status of **Not imported**. Then select **Not imported** or the vertical ellipsis contextual menu, and then select **Import data**.

## Sources

Import a local CSV or XLSX file from your computer or connect Supply Chain Insights to a your own data storage or cloud storage service to populate the data for any entity. For either method, ensure that your data contains the required attributes of a given entity. For example, column headers must be named if you upload a local file. For cloud storage, additional information will be required to authenticate Supply Chain Insight's access to the data depending on the cloud storage service selected.

<!--![selecting an entity, choosing a cloud data source, and authorizing Supply Chain Insights' access to the data](/articles/media/connect-and-authorize-cloud-storage.gif)-->

## Local file prerequisites

- An [on-premises data gateway](/data-integration/gateway/service-gateway-onprem) is required for local files on your computer to be imported into Supply Chain Insights. For support on installing an on-premises data gateway, see [Install an on-premises data gateway](https://docs.microsoft.com/en-us/data-integration/gateway/service-gateway-install).
- After installing on-premises data gateway, you must use your Supply Chain Insights user credentials to sign into the application.
- You must ensure that the local folder containing the file you want to upload is configured to grant access to everyone.

## Mappings

Mappings inform Supply Chain Insights how to interpret your data so that it can be analyzed. A mapping describes how your data relates to the attributes that represent a certain entity, and is easy to complete during the ingestion process. 

### Local files

Local files that you upload must have column headers because Supply Chain Insights uses these headers to map your data to the attributes of the entity. When you select **Auto map**, Supply Chain Insights attempts to determine which column represents what attribute by using the column headers. Select the **Mapped attributes** column along with the **Data preview** table at the bottom of the page to ensure that automatic mapping is executed correctly. If there is an error, or if you would prefer to do the mapping manually, in the **Mapped attributes** column select the dropdown menu option for the required attribute of interest and then select the appropriate column header name.

### Cloud storage

If a table representing the desired entity is available, select it from the left hand column after a data source has been selected. If a table representing the desired entity is not available, the Power Query interface contains numerous tools to transform your data into a single table representing the entity. For more information on these tools and how to use them, see [Transform data](/power-query/power-query-ui). Once a table containing all of the information for an entity has been created, you can have Power Query automatically map the information in your table to the attributes of the entity by selecting **Map to entity** on the top right, selecting the entity of interest from the left column of the popup window, and then selecting **Auto map**. Check the query output column for any errors or manually map your data using this column, and then select **Done**.

<!--![mapping for importing data from a cloud storage solution](/articles/media/map-column-headers-to-attributes.gif)-->

## Refresh schedule

Up-to-date insights are reliant upon up-to-date data ingestion, which can be ensured in three ways. 
- A refresh schedule automatically updates the ingested data for a given entity based on any changes made to that data within your cloud storage solution. 
- Entities connected to your storage solution can also be updated on the **Data import** page by selecting **Refresh now** from the dropdown menu. 
- On the **Data import** page you can also change a refresh schedule, stop a refresh schedule, or disconnect the entity from a data source entirely. 

