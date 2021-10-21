---
title: Analytics dashboards
description: This topic describes the analytics dashboards in Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 10/13/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry

---

# Analytics dashboards

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

Dynamics 365 Supply Chain Insights uses your ingested data and information received from partners to generate analytics. The analytics provide you with a current snapshot of different parts of your supply chain such as supply and demand, shipping, and vendor performance. Analytics are presented as dashboards using charts, tables, and graphs.

## Prerequisites
To generate insights that are relevant to your business, Supply Chain Insights requires data that is relevant to your supply chain. Therefore, that data must be brought (ingested) into the application. For more information, see [Ingest data](ingest-data.md). The sections below specify which entities are required for each tab on the **Analytics > Analytics** page.

## Product map
The **Product map** tab displays visuals to help you understand the dependencies between your finished products, the parts that make up those products, your warehouses that store the parts, and in-transit shipments of those parts.

The following entities are required for the **Product map** dashboard to display.
- **Warehouse**
- **Item**
- **Product**
- **Bill of material line**
- **Product map** 

## Shipping
The **Shipping** tab provides an overview of the on-time delivery performance for your products under various conditions. It contains information on which parts your company has delivered late or early based on historical data, along with current in-transit shipments. You can drill down into dependencies for a particular product, part, or warehouse by changing the filters or selecting one of the visuals.

The following entities are required for the **Shipping** dashboard to display.
- **Warehouse**
- **Item**
- **Product**
- **Vendor**
- **(Purchase and sales) order**
- **(Purchase and sales) order line**
- **Shipment item**
- **Shipment**

## Vendor performance
The dashboard on the **Vendor performance** tab provides an overview of your vendors' on-time delivery performance for various scenarios. You can change the filters to modify the display of your vendors' on-time delivery performance or to dill down into a particular type of delivery.

The following entities are required for the **Vendor performance** dashboard to display.
- **Item**
- **Product**
- **Vendor**
- **(Purchase) order**
- **(Purchase) order line**
- **Shipment item**
- **Shipment**

## Supply and demand
The **Supply and demand** dashboard provides an overview of the interest that different parts have relative to your overall inventory. You can use this information to identify which parts have the greatest shortage or greatest over-supply based on various conditions such as time range, partner, or product.

The following entities are required for the **Supply and demand** dashboard to display.
- **Item**
- **Product**
- **Customer**
- **Vendor**
- **Production order**
- **Customer product allocation**
- **Master plan schedule**
- **Material resource plan**
- **Warehouse item available stock**


