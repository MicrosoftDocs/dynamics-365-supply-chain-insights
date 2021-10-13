---
title: Analytics
description: This page contains information on the analytic dashboards in Supply Chain Insights
author: carylhenry
ms.date: 10/13/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]


Supply Chain Insights uses your ingested data along with information received from partners to generate analytics. The analytics provide a current snapshot of different parts of your supply chain such as supply & demand, shipping, and vendor performance, through charts, tables, and graphs.


# Prerequisites
The "Analytics" section requires data for various etities to have been ingested according to the process described in [Ingestion](/articles/ingestion.md). The sections below specify which entities are required for each tab within the "Analytics" section to be fully functional.

# Product map
The  "Product map" tab combines visuals for you to understand the dependencies between your finished products, the parts that make up those products, your warehouses to store the parts, and in-transit shipments of those parts.

## Required entities
- Warehouse
- Item
- Product
- Bill of mterial line
- Vendor 

# Shipping
The "Shipping" dashboard provides an overview of your on-time-delivery performance for your products under various conditions. It contains information on which parts your company has delivered late or early based on historical data along with current in-transit shipments. Changing the filters or clicking one of the visuals helps you drill down into the dependencies for a particular product, part, or warehouse.

## Required entities
- Warehouse
- Item
- Product
- Vendor
- (Purchase and sales) order
- (Purchase and sales) order line
- Shipment item
- Shipment

# Vendor performance
The 'Vendor performance" dashboard gives an overview of your vendors' on-time delivery performance for a variety of scenarios. Changing the filters lets you have an overall understanding of your vendors' on-time delivery performance or delivers a deep dive into a particular type of delivery.

## Required entities
- Item
- Product
- Vendor
- (Purchase) order
- (Purchase) order line
- Shipment item
- Shipment

# Supply & demand
The "Supply & demand" dashboard gives an overview of how much interest various parts have relative to your inventory. 
Using the information provided on this dashboard, it's easy to identify which parts have the greatest shortage or greatest oversupply based on a variety of conditions such as time range, partner, product, etc.

## Required entities
- Item
- Product
- Customer
- Vendor
- Production order
- Customer product allocation
- Master plan schedule
- Material resource plan
- Warehouse item available stock


