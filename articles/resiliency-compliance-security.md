---
title: Compliance
description: This topic describes compliance and security as they are related to the handling of information in Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 11/04/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry

---

# Compliance

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

Supply Chain Insights was designed with compliance, privacy, security, and confidentiality in mind. It's intended to be used only to identify and mitigate risks that are related to your supply chain. Microsoft offers Supply Chain Insights under the Microsoft Online Services terms, which include robust data protection terms.

To determine whether Supply Chain Insights meets your compliance requirements, see the [Supply Chain Insights terms of service agreement](https://go.microsoft.com/fwlink/?linkid=2175113).

You have the following responsibilities:

- Inform your customers about your data processing practices. For example, disclose what data you collect and how it's used.
- Disclose your use of third parties that work on your behalf to process the data that you collect. These third parties include service providers for Supply Chain Insights.
- Comply with all laws and regulations that are applicable to the use of Supply Chain Insights. These laws and regulations include data protection laws.

## Data subject access requests

Data subject deletion requests can be completed by deleting or exporting the relevant entities within Supply Chain Insights. When responding to deletion requests, you should also update the ingestion source for those entities so that the data involved in the deletion request does not get reuploaded to the application.
 
>[!NOTE]
> - If the deleted data was originally shared with partners through a data collaboration and a partner exported the data, the partner may still have the data.
> - When you stop ingesting data, stop sharing data with partners, or delete data from an original data source and then refresh the data within Supply Chain Insights, it may take as long as 48 hours for Supply Chain Insights to cease making the data available to partners you previously shared the data with.


## Security

Supply Chain Insights might include data sharing with other users of the application. Therefore, Microsoft has implemented and will maintain appropriate technical and organizational measures to help protect customer data. This data includes personal data and company data that has been copied to another region so that it can be shared with a partner that stores its data in a different location than your company. These measures are described in the Microsoft security policy that will be made available to customers, together with descriptions of the security controls that are in place for Supply Chain Insights and other information that customers might reasonably request about Microsoft security practices and policies.


## Data sharing

Supply Chain Insights shares data between participants only when it's explicitly instructed to do so via data collaborations. The participants in a collaboration agree that, to share customer data as they instruct, Microsoft might have to store a copy of that data in any or all of the geographic regions where the other participants are located. For more information about data sharing, see [Data collaborations](create-collaboration.md) and the [Supply Chain Insights terms of service agreement](https://go.microsoft.com/fwlink/?linkid=2175113).

You agree that, to share customer data as you instruct, Microsoft might have to store a copy of that data in any or all of the geographic regions where the services store customer data, provided that the services will make the data available to other users only as you instruct.
