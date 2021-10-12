---
title: Supply chain map
description: This topic describes the supply chain map in Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 10/12/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---

# Supply chain map

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

This topic describes the supply chain map in Microsoft Dynamics 365 Supply Chain Insights.

The Dynamics 365 Supply Chain Insights supply chain map provides a visual representation of a company’s supply chain. This visualization shows how suppliers are connected to company facilities and how those facilities are connected to customers. 

The map view also provides risk data for each uploaded site. Currently, two types of risk data are shown in map view: latent weather risks based on historical events and real-time weather risks such as ongoing natural catastrophes.

## Supply chain map prerequisites

The supply chain map requires site location information to add locations to the map. Initially, Supply Chain Insights will use the data provided when a participant is onboarded to populate your location and your vendors' locations. The map view is updated to include additional sites when other production plant and warehouse data is uploaded or when you receive data from connected suppliers or customers within Supply Chain Insights. The map view update feature uses uploaded bills of materials to connect sites and visualize the geographic flow of products and relationships between sites. 

## Reading the map

### Sites

"My site," "My production plant," "My warehouse," "Vendor's site," "Vendor's production plant," and "Vendor's warehouse" are all sites represented by icons in the Supply Chain Insights supply chain map, as shown in the following illustration. 

![Icons used to represent different types of locations on the supply chain map](/articles/media/supply-chain-map-legend.PNG)

"My site" and "Vendor's site" are generic icon labels that are used when Supply Chain Insights cannot detect the facility type or when a facility includes both production plants and warehouses. You must ingest the production plant and warehouse entities to see your sites on the map whereas you must ingest, connect, and share data with a vendor for their sites to appear.

To see your sites on the map, you must first ingest the production plant and warehouse entities into Supply Chain Insights. To see vendor sites on the map, you must forst ingest, connect, and share data with those vendors.

Hovering over a site on the map will bring up information related to the site, including the company name, site address, and site risk score. Selecting a site icon will bring up a sidebar that shows additional site information such as risks details and potentially impacted orders. For the potentially impacted order functionality to work, the order entity must be ingested in addition to the production plant and warehouse entities mentioned above.

### Connections

Arrows and dashed lines between two sites show the flow of goods. Goods are shipped from the site at the tail end of the arrow and are delivered to another site at the tip of the arrow. These connections are created based on attributes defined in your and your vendors' production plant, warehouse, and bill of material entities. These entities must be ingested before the relevant connections can be seen on the supply chain map.

### Risk score

The circle with a number next to a supply chain map site icon represents the correlating risk score for that site. Risk scores are ranked on a scale from 0 to 99, and are calculated by averaging all of the latent weather risks for a given site and also factoring in any current weather risks as warranted. Risk scores are classified as low, medium, or high as follows: 

- Low risk scores represent risk scores 0 to 33 and are displayed as green. 
- Medium risk scores represent risk scores 34 to 66 and are displayed as orange. 
- High risk scores represent risk scores 67 to 99 and are displayed as red. 

### Live alerts

Red circles on the supply chain map represent areas containing sites that may be impacted by real time events. Currently, the real time risks shown are weather risks such as ongoing natural catastrophes. Selecting a circle brings up a sidebar on the left with a list of live alerts. 

![Supply chain map showing the sidebar listing sites and their risk scores](/articles/media/supply-chain-map.PNG)

## Map views

The drop down menu in the top right of the supply chain map can display various types of latent risk overlaid on the map. Initially the view is set to a **Default** state where no latent risks are overlaid.  

The following latent weather risks can be viewed on the map page:

- River flooding
- High winds
- Hailstorms
- Seismic events
- Tornadoes
- Lightning
- Ash thickness
- Subsidence
- Storm surges

### Filters

Filters are provided to help you focus on different aspects of your supply chain. Selecting **Filters** in the top right of the command bar brings up a sidebar containing options to filter by. Currently filters will be provided for facility type and vendor visibility for tier 1- 5+. By default vendor visibility will be set to all uploaded vendors regardless of tiers.

### List

Selecting **List** in the top left of the command bar brings up a sidebar on the left side of the map that will initially contain a list of sites ranked from highest to lowest risk. Sites can be reordered based on risk score and alphabetically by site name. Selecting a specific site on the supply chain map will bring up information related to that site such as risk details and order information.
