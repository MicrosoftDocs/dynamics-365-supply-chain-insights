---
title: Supply chain map
description: This topic describes the supply chain map in Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 6/07/2021
ms.topic: article
audience: Application User
ms.search.region: Global

ms.author: carylhenry
---

# Supply chain map

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

This topic describes the supply chain map in Microsoft Dynamics 365 Supply Chain Insights.

The supply chain map in Supply Chain Insights provides a geographic representation of your company's supply chain, including both you and your vendors' sites.


## Supply chain map prerequisites

The supply chain map requires that WebGL is enabled in your browser's settings. Site location information also must be ingested to add locations to the map. Initially, Supply Chain Insights adds participant and vendor locations by using the data that is provided when a participant is onboarded. Then, when other production plant and warehouse data is uploaded, or when you receive data from connected suppliers or customers in Supply Chain Insights, the map view is updated so that it includes additional locations.

## Reading the map

"My site," "My production plant," "My warehouse," "Vendor's site," "Vendor's production plant," and "Vendor's warehouse" are all sites that are represented by icons on the supply chain map, as shown in the following illustration.

![Icons that represent different types of locations on the supply chain map.](media/supply-chain-map-legend.png)

To view your sites on the map, you must first ingest the production plant and warehouse entities into Supply Chain Insights. To view vendor sites on the map, you must first ingest vendor entities into Supply Chain Insights, and then connect and share data with those vendors.

If you hover over a site on the map, information that is related to the site is shown. The information includes the company name, site address, and site risk score. If you select a site icon, a sidebar appears and shows additional site information, such as potentially affected orders. The "potentially affected order" functionality requires that the order entity is ingested into Supply Chain Insights, in addition to the production plant and warehouse entities that were mentioned earlier.


## Map views

### Filters

Filters are provided to help you focus on different aspects of your supply chain. If you select **Filters** in the upper right of the command bar, a sidebar appears and shows filtering options. You can currently filter by facility type and vendor visibility. By default, the vendor visibility filter is set to show all uploaded vendors, regardless of tier.

### List

If you select **List** in the upper left of the command bar, a sidebar appears on the left side of the map and shows a list of sites. If you select a specific site on the supply chain map, information that is related to that site appears, such as order information.
