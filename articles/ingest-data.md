---
title: Ingest data
description: This topic describes how to ingest data into Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 03/02/2022
ms.topic: article
audience: Application User
ms.search.region: Global

ms.author: carylhenry
---

# Ingest data

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

This topic describes how to ingest data into Microsoft Dynamics 365 Supply Chain Insights.

To generate insights that are relevant to your business, Dynamics 365 Supply Chain Insights requires data that is relevant to your supply chain. Therefore, that data must be brought (*ingested*) into the application. Supply Chain Insights uses [Power Query](/power-query/power-query-what-is-power-query) to help ensure a smooth data ingestion experience.

## Prerequisites

Data management requires that you ingest data from various sources, according to the entities that are described in [Data entities](entities.md). For example, this set of [Excel files](https://download.microsoft.com/download/d/c/2/dc238977-69a5-4440-a19e-24d632c25cf5/OEM_Electronics_Sample.zip) contains data for a large manufacturing company and its supplier. Although this data set might not contain all the attributes for every entity, it's enough so that Supply Chain Insights can visually show a supply/demand mismatch issue in the **Analytics** section of the application.

Before ingesting your data, review the information in [Compliance](resiliency-compliance-security.md) to ensure that Supply Chain Insights meets your company's expectations.

## Get started

To start the ingestion process, open the **Data import** page, and select an entity that has a status other than **Not imported**. Select **Not imported** or the vertical ellipsis button, and then select **Import data**.

## Connect your data to Supply Chain Insights

Supply Chain Insights must connect to your own data storage or cloud storage service before you can upload the data for any entity. Additional information may be required to authenticate Supply Chain Insights' access to the data. If the data for a single entity is stored in two separate data sources, choose one source to begin with and the second one can be added later on in the ingestion process. We also recommend that your data contains the required attributes of a given entity. This will make sure you're getting the most value out of SCI, although not having all the required attributes will not block you from ingesting data. For example, if you upload an Excel file, the column headers should be named based off of the attributes of the entity your uploading. This will make it easier to map your data to the attributes of Supply Chain Insights' entities, but you can also transform your data to fit this format using the Power Query editor in the next step.

![Data import page showing a list of data sources that can be connected to Supply Chain Insights.](media/connector-options.png)

### Local file prerequisites

An [on-premises data gateway](/data-integration/gateway/service-gateway-onprem) is required to import local files on your computer into Supply Chain Insights. See [Install an on-premises data gateway](/data-integration/gateway/service-gateway-install) for information on how to install an on-premise data gateway. After you install the gateway, you must use your Supply Chain Insights user credentials to sign in to the application. Then make sure that the local folder which contains the file you want to upload is configured so that access is granted to everyone. To change this configuration, navigate the folder, right click on it, and then select **Give access to >> Specific people**.

## Transform and map the data according to your desired entity

Mappings inform Supply Chain Insights how to interpret your data so that it can be analyzed. A mapping describes how the data within a query's table relates to the attributes that represent a specific entity. The Power Query editor contains numerous tools that you can use to transform your data into a single query containing one table that contains all attributes of an entity. This transformation and mapping only needs to be completed once for an entity, assuming you don't change the data source(s). If only part of the data for an entity is contained in the first source you connected, click **Get Data** in the upper left of the Power Query editor when you are in the **Home** tab. This will prompt you to go through the connection process again to add another source. See [Transform data](/power-query/power-query-ui) for more information about the Power Query editor and what it can do.
    
![Data import page, showing the Power Query editor for the product entity.](media/power-query-editor.png)

After you've created a single query with the table that contains the data that you want to import, you can have Power Query automatically map the information in your table to the attributes of the entity. Select **Map to entity** in the upper right, select the entity in the left column of the dialog box that appears, and then select **Auto map**. Supply Chain Insights will use the column headers of the query table to determine which column represents which attribute. To ensure that automatic mapping is run correctly, select the **Mapped attributes** column together with the **Data preview** table at the bottom of the page. If an error occurs, or if you prefer to do the mapping manually, select the option for the required attribute in the **Mapped attributes** column, and then select the appropriate column header name. Choose **Done** once finished.

> [!NOTE]
> You can have multiple queries when using the Power Query editor, but Supply Chain Insights only uploads the data from one of the queries. The application determines the best query to ingest by matching the column headers of the queries to the attributes of the entity that is being uploaded. The query with the best matching column headers will then be selected by Supply Chain Insights and its data ingested.

![Data import page, showing the dialog box for Power Query's auto map feature when it's to map user data to a product entity's attributes.](media/product-attribute-mapping.png)

## Refresh schedule for data ingested through the cloud

Up-to-date insights rely on up-to-date data ingestion. There are three ways to ensure that data ingestion is up to date:

- A refresh schedule automatically updates the ingested data for a given entity, based on any changes that were made to that data in your cloud storage solution.
- On the **Data import** page, you can update entities that are connected to your storage solution by selecting **Refresh now** on the drop-down menu.
- On the **Data import** page, you can change a refresh schedule, stop a refresh schedule, or completely disconnect the entity from a data source.
