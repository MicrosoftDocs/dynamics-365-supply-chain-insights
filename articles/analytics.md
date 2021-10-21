---
title: Analytics dashboards
description: This topic describes the analytics dashboards in Microsoft Dynamics 365 Supply Chain Insights.
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

Microsoft Dynamics 365 Supply Chain Insights uses your ingested data and information that is received from partners to generate analytics. The analytics provide a current snapshot of different parts of your supply chain, such as supply and demand, shipping, and vendor performance. Analytics are presented as dashboards that use charts and tables.

## Prerequisites

To generate insights that are relevant to your business, Supply Chain Insights requires data that is relevant to your supply chain. Therefore, that data must be brought (ingested) into the application. For more information, see [Ingest data](ingest-data.md).

The remaining sections of this topic specify the entities that are required for each tab on the **Analytics** page (**Analytics \> Analytics**).

## Product map

The dashboard on the **Product map** tab shows visuals that can help you understand the dependencies between your finished products, the parts that make up those products, your warehouses that store those parts, and in-transit shipments of those parts.

The following entities are required for the **Product map** dashboard to appear:

- Warehouse
- Item
- Product
- Bill of material line
- Product map

## Shipping

The dashboard on the **Shipping** tab provides an overview of the on-time delivery performance for your products under different conditions. It contains information about parts that your company has delivered late or early, based on historical data, together with information about current in-transit shipments. You can drill down into dependencies for a specific product, part, or warehouse by changing the filters or selecting one of the visuals.

The following entities are required for the **Shipping** dashboard to appear:

- Warehouse
- Item
- Product
- Vendor
- (Purchase and sales) order
- (Purchase and sales) order line
- Shipment item
- Shipment

## Vendor performance

The dashboard on the **Vendor performance** tab provides an overview of your vendors' on-time delivery performance in different scenarios. You can change the filters to change the display of your vendors' on-time delivery performance or drill down into a specific type of delivery.

The following entities are required for the **Vendor performance** dashboard to appear:

- Item
- Product
- Vendor
- (Purchase) order
- (Purchase) order line
- Shipment item
- Shipment

## Supply and demand

The dashboard on the **Supply and demand** tab provides an overview of the demand that there is for different parts relative to your overall inventory. You can use this information to identify which parts have the greatest shortage or greatest over-supply, based on conditions such as the time range, partner, or product.

The following entities are required for the **Supply and demand** dashboard to appear:

- Item
- Product
- Customer
- Vendor
- Production order
- Customer product allocation
- Master plan schedule
- Material resource plan
- Warehouse item available stock
