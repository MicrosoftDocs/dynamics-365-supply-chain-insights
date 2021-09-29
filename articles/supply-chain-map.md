---
title: Supply chain map
description: This page contains information for the supply chain map in Microsoft Dynamics 365 Supply Chain Insights
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


The supply chain map provides a visual representation of a company’s supply chain. This visualization shows how supplier are connected to company facilities and how those facilities are connected to customers. This feature utilizes an uploaded bill of materials to connect these sites together and visualize the geographic flow of a product and relationships between sites. 

The map view also provides risk data for each uploaded site. Currently the two types of risk data shown are latent weather risks based on historical events and real-time weather risks such as ongoing natural catastrophes.

Prerequisites
The supply chain map requires site location information to add locations to the map. Initially, Supply Chain Insights will utilize the data provided when a participant onboards to populate your and your vendors' locations. This view will be updated to include additional sites when uploading additional vendor data or when you receive data from connected suppliers or customers within Supply Chain Insights.

# Reading the map
"My site," "My production plant," "My warehouse," "Vendor's site," "Vendor's production plant," and "Vendor's warehouse" are all sites. They are represented by the icons in the image below, from top to bottom accordingly. 

## Sites
"My site," "My production plant," "My warehouse," "Vendor's site," "Vendor's production plant," and "Vendor's warehouse" are all sites. Please note that "My site" and "Vendor's site" are more generic, since they are used when Supply Chain Insights cannot detect the facility type or when a facility includes both production plants and warehouses. You must ingest the production plant and warehouse entities to see your sites on the map whereas you must ingest, connect, and share data with a vendor for their sites to appear.

Hovering over a site on the map with your mouse will bring up more information related to the site, including the company name, site address, and site risk score. After selecting a site icon, a sidebar will show more information on the site, including risks details and potentially impacted orders. In addition to the entities mentioned previously, the order entity must also be ingested for the potentially impacted order functionality.

## Connections
Arrows and dashed lines between two sites show the flow of goods. Goods are shipped from the site at the tail end of the arrow and are delivered to another site at the tip of the arrow. These connections are created based on attributes defined in your and your vendors' production plant, warehouse, and bill of material entities which must be ingested before these connections can be seen on the supply chain map.

## Risk score
The circle with a number next to all of the site icons is the correlating risk score for the site. Risk scores are ranked on a scale from 0-99.  These risk levels are calculated by averaging all the latent weather risks for a given site and factoring in any current weather risks as needed. A risk score can be classified as low, medium, or high. Low risk scores are displayed in green and represent risk scores 0-33. Medium risk scores are displayed as orange and represent risk scores 34-66. High risk score are displayed as red and represent risk scores 67-99. 

# Map views
The dropdown menu in the top right corner will display various types of latent risk overlaid on the map. Initially the view will be set to a default state where no latent risks will be overlaid. 

## Filters
Filters are provided to help you focus on different aspects of your supply chain. Selecting the "Filter button" in the top right corner will cause a sidebar with the options to filter by. Currently filters will be provided for facility type and vendor visibility for tier 1- 5+. By default vendor visibility will be set to all uploaded vendors regardless of tiers.

# List
Selecting "List" in the top left corner will cause a sidebar to display on the left side of the map. It will initially contain a list of sites ranked from highest to lowest risk. Alternatively, this list of sites can be opened by directly choosing a site from the supply chain map. Drilling into a site will bring up more information related to that site, including details on the risk and potentially impacted orders.

