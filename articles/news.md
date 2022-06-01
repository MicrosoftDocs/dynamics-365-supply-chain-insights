---
title: Curated news
description: This topic describes the curated news feature that is included in Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 06/01/2022
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

Each news article is also assigned an impact score and a category by the same AI model which sorts the news articles by relevance. The impact score and category definitions are learned from past news articles which were labeled with the correct impact and category. The AI model learns patterns from the sentiment and content of these labeled articles to make predictions for new articles. Users can filter on these two characteristics on the dedicated **News** page. The categories can be filtered by selecting an individual category on the left navigation. Additionally, multiple categories can be toggled off/on within the settings found towards the top of the **News** page.

### Impact score definitions
Each article will be assigned one of the following three impact scores 

- **Immediate impact:** For articles containing news that are directly negatively impacting companies in your supply chain today. 
- **Future impact:** For articles containing news that has the potential to negatively impact companies your supply chain at some point in the future. 
- **Positive impact:** For articles containing news that is positive about companies in your supply chain and contain supply chain relevant content.

### Category definitions

All news articles will be assigned one of the following categories: 

- **Bankruptcy, acquisition, and collaboration:** For news articles containing information regarding mergers and acquisitions, bankruptcy, new (or reduced) collaborations with other companies/suppliers. 
- **Company:** For news articles containing information relevant to the company, change in leadership or important personnel, new investment areas, awards etc. 
- **Company financial:** For news articles containing information about the growth and financial outlook of an individual company. 
- **Disruption and weather:** For news articles containing information about events causing direct supply disruption e.g., factory fires, explosions, leaks, Suez Canal blockage etc.; or natural disasters such as forest fires, hurricanes, etc. 
- **Health:** For news articles containing information about human and animal epidemics and pandemics (COVID, Ebola, h1n1 etc.) 
- **Industry financial:** For news articles containing information about industry financial news focuses on the growth/financial outlook of the entire industries. 
- **Industry supplier:** For news articles containing information about other suppliers in the same industry, top supplier lists, general supplier risk articles, etc. 
- **Infrastructure:** For news articles containing information about general infrastructure improvements that could benefit a spesific supplier. 
- **Politics and government:** For news articles containing information about government investigation, government collaborations, discounts/deals, lobbying, litigation and regulations etc. 
- **Product:** For news articles containing information about new/old products of the company, new technologies used in existing products, removal of product lines etc. 
- **Quality:** For news articles containing information about supplier quality, or quality control issues. 
- **Sustainability:** For news articles containing information about new/existing sustainability efforts, environmental impact etc. 
- **Workforce:** For news articles containing information about employees, strikes, workplace conditions etc
