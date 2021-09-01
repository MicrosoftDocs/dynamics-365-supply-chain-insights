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

# Reading the map
## Sites
"My site," "My production plant," "My warehouse," "Vendor's site," "Vendor's production plant," and "Vendor's warehouse" are all sites. 
Please note that "My site" and "Vendor's site" are more generic, since they are used when Supply Chain Insight cannot detect the facility type or when a facility includes both production plants and warehouses. 

## Connections
Connections show the flow of goods between sites.
Goods are delivered from one site at the tail end of the arrow and are sent to another located at the tip of the arrow.

## Risk factor
The circle with a number next to all of the site icons is the correlating "Risk factor" for the site. 
Risk factors may not necessarily always be a red circle with a number. 
They can be green or yellow depending upon the severity of a risk at a given location.

## Live alerts
Red circles on the map represent areas containing sites which may be impacted by a weather event. 
Clicking on a circle will pull up a sidebar on the left hand side with a list containing live alerts. 
Alternatively, filters are available in the dropdown menu in the top right corner to show the severity of different weather events around the world.

# List
Selecting "List" in the top left corner will cause a sidebar to appear on the left side of the map. It will initially contain a list of sites from highest to lowest risk. Alternatively, this list of sites can be opened by directly clicking on a site from the supply chain map. Drilling into a site will bring up more information related to that site, including details on the risk, potentially impacted orders, and mitigation cases assigned to that site.

The list can also be ordered by live alerts from highest to lowest risk instead of sites. Clicking on a live alert from the supply chain map will also cause the list to appear. Drilling into a live alert will show more details, including what sites may be impacted from the weather event.

# Filters
Filters are provided to help you focus on different aspects of your supply chain. Selecting the "Filter button" in the top right corner will cause a sidebar with the options to filter by. Filters are provided for risk severity, visibility score, sites and facility type.
