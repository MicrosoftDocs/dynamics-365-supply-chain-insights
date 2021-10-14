---
title: Products page
description: This topic describes the functionality of the products page in Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 10/13/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---

# Products

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

This topic describes the functionality of the products page in Microsoft Dynamics 365 Supply Chain Insights.

Products are often manufactured goods that require parts and materials to be created. The products page of Supply Chain Insights lists all of the products you sell and highlights dependencies in your supply chain by enabling you to easily identify what parts and materials are required to manufacture each product.

> [!NOTE]
> For the **Products** page to function, the entities for products and their corresponding bills of material must be ingested into Supply Chain Insights according to the process outlined in [Ingestion](ingestion.md).

## Products page functionality

To view information about a product in Supply Chain Insights, you first select **Products** in the left navigation pane, which brings up the **Products** page with a list of products. To view product details, select the vertical ellipsis in the product's row, and then select **Details**. The product page then appears with two tabs:

- The **Details** tab lists details about the product such as the product name, product ID, product description, vendor name, and vendor ID.
- The **Bill of materials** tab lists the component parts of the product.

Selecting a part on the **Bill of materials** tab opens a pane on the right that contains details about the part such as the part name, part ID, vendor product ID, and item ID. Alternatively, selecting **Details** via the vertical ellipsis of a part's row on the **Bill of materials** tab opens a part page with **Details** and **Bill of materials** tabs. Part information is listed on the **Details** tab, and any part components are listed on the **Bill of materials** tab.

<!-- ![selecting a product, looking at its bill of material, and then choosing an item listed in the bill of material](/articles/media/Basket-assembly-product.gif)-->



