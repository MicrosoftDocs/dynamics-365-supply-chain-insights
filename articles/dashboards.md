---
title: Dashboards
description: This page contains information on the analytic dashboards in Supply Chain Insights
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


Supply Chain Insights uses your ingested data along with information received from partners to generate analytics. The analytics provide a current snapshot of different parts of your supply chain such as supply & demand, shipping, and vendor performance, through charts, tables, and graphs.


# Prerequisites
Analytics requires data to have been ingested according to the process described in [Ingestion](/articles/ingestion.md).
Data for all entities should be imported because this is required for all analytic features to run and helps to ensure the analytics are accurate, but the specific data entities required for each analytic feature is listed within each feature's description below.

# Summary
The  "Summary" tab combines visuals contained in the other tabs to provide an overall snapshot of your supply chain's health. Selecting the same of a part on any of the visuals presents you with a new dashboard containing information on that particular part.

# Supply and demand
The "Supply and demand" dashboard gives an overview of how much interest various parts have relative to your inventory. 
Using the information provided on this dashboard, it's easy to identify which parts have the greatest shortage or greatest oversupply based on a variety of conditions such as time range, partner, product, etc.

## Required entities
- Vendor
- Customer
- Product
- Item
- Warehouse item available stock
- Customer product allocation
- Master plan schedule
- Material resource plan
- Production order


# Shipping
The "Shipping" dashboard provides an overview of your on-time-delivery performance under various conditions such as time range, vendor, and produc. 
The dashboard contains information on which parts your company has delivered late or early based on historical data. 
There is also a table with information on parts that have shipped and are currently in-transit.

## Required entities
- Vendor
- Warehouse
- Shipment
- Shipment item
- Order
- Order line
- Item
- Product
- Purchase order

# Vendor performance
The 'Vendor performance" dashboard gives an overview of your vendors' on-time delivery performance for a variety of scenarios. 
Changing the filters lets you have an overall understanding of your vendors' on-time delivery performance or delivers a deep dive into a particular type of delivery.

## Required entities
- Vendor
- Item
- Product
- Order
- Order line
- Shipment
- Shipment item
