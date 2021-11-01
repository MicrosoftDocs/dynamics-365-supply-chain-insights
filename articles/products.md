---
title: Products page
description: This topic describes the functionality of the Products page in Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 11/01/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---

# Products page

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

This topic describes the functionality of the **Products** page in Microsoft Dynamics 365 Supply Chain Insights.

Products are often manufactured goods that are created from parts and materials. The **Products** page in Supply Chain Insights lists all the products that you sell. It highlights dependencies in your supply chain by letting you easily identify the parts and materials that are required to manufacture each product.

> [!NOTE]
> For the **Products** page to work, the entities for products and their corresponding bills of materials (BOMs) must be ingested into Supply Chain Insights according to the process that is outlined in [Ingest data](ingest-data.md).

## Products page functionality

To view information about a product in Supply Chain Insights, select **Products** in the left navigation pane. The **Products** page that appears contains a list of products. To view a product's details, select the vertical ellipsis button in the row for the product, and then select **Details**. The page that appears has two tabs:

- **Details** – This tab lists details about the product, such as the product name, product ID, product description, vendor name, and vendor ID.
- **Bill of materials** – This tab lists the component parts of the product.

If you select a part on the **Bill of materials** tab, a pane appears on the right and shows details about that part, such as the part name, part ID, vendor product ID, and item ID. Alternatively, if you select the vertical ellipsis button in the row for a part on the **Bill of materials** tab, and then select **Details**, a part page appears. This page has a **Details** tab that lists part information and a **Bill of materials** tab that lists any part components.

![selecting a product, looking at its bill of material, and then choosing an item listed in the bill of material](/articles/media/Basket-assembly-product.gif)
