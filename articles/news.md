---
title: Curated news
description: This topic describes the curated news feature that is included in Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.search.region: Global

ms.author: carylhenry

---

# Curated news

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

This topic describes the curated news feature that is included in Microsoft Dynamics 365 Supply Chain Insights.

Dynamics 365 Supply Chain Insights is designed to help users identify and respond to external risks. The curated news feature is one way that it achieves this goal. The feature enables Supply Chain Insights to gather information about world events, and then present only the news that is relevant to your company and partner companies. To curate news articles in this way, Supply Chain Insights uses the names that were provided for your company and your vendor companies during initial onboarding.

## Prerequisites

Supply Chain Insights uses artificial intelligence to sort news articles based on their relevance to a company and its supply chain. Initially, news will be presented based on company, vendor, and customer names that were entered during the onboarding process. However, when additional vendors or customers are imported into Supply Chain Insights, or when a connection is made with another Supply Chain Insights participant, news will be curated for those companies.

## Functionality

Supply Chain Insights curates recent relevant news articles by using a trained AI model that identifies news that could affect a supply chain. The news articles are then presented as tiles on the **Home** and **News** pages of the application. If you select **Read article** on a tile, the news story is opened on a new tab. If you select **View impacts** on a tile, a page that is specific to the news article is opened. There, you can see which partners in your supply chain could be affected by the news.

> [!NOTE]
> Larger companies are more likely to be prominent in the news than smaller companies, which may affect what news articles are recommended in the curated news feature. As a result, certain sources of risks from smaller partner companies may not be highlighted.

Each news article is assigned an impact score and a category by the same AI model that sorts the news articles by relevance. The impact score and category definitions are learned from past news articles that were labeled with the correct impact and category. The AI model learns patterns from the sentiment and content of these labeled articles to make predictions for new articles. Users can filter on these two characteristics on the dedicated **News** page. The categories can be filtered by selecting an individual category on the left navigation. Additionally, multiple categories can be toggled off or on within the settings found on **News** page.

### Impact score definitions
Each article will be assigned one of the following three impact scores. 

- **Immediate impact:** Contains news that directly negatively impacts companies currently in your supply chain. 
- **Future impact:** Contains news that has the potential to negatively impact companies in your supply chain at some point in the future. 
- **Positive impact:** Contains news that is positive about companies in your supply chain and contain supply chain relevant content.

### Category definitions

All news articles will be assigned one of the following categories: 

- **Bankruptcy, acquisition, and collaboration:** Contains information about mergers and acquisitions, bankruptcy, or new or reduced collaborations with other companies or suppliers. 
- **Company:** Contains information relevant to the company, such as change in leadership or important personnel, new investment areas, or awards. 
- **Company financial:** Contains information about the growth and financial outlook of an individual company. 
- **Disruption and weather:** Contains information about events causing direct supply disruption, such as factory fires, explosions, leaks, Suez Canal blockage, or natural disasters such as forest fires or hurricanes. 
- **Health:** Contains information about human and animal epidemics and pandemics, such as COVID-19, Ebola, or H1N1. 
- **Industry financial:** Contains information that focuses on the growth or financial outlook of an entire industry. 
- **Industry supplier:** Contains information about other suppliers in the same industry, such as top supplier lists or general supplier risk articles. 
- **Infrastructure:** Contains information about general infrastructure improvements that could benefit a specific supplier. 
- **Politics and government:** Contains information such as government investigations, government collaborations, discounts/deals, lobbying, litigation, or regulations. 
- **Product:** Contains information about new or old products of the company, such as new technologies used in existing products or removal of product lines. 
- **Quality:** Contains information about supplier quality or quality control issues. 
- **Sustainability:** Contains information such as new or existing sustainability efforts or environmental impacts. 
- **Workforce:** Contains information affecting employees, such as strikes or workplace conditions.
