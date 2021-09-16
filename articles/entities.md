---
title: Entities
description: This page contains an explanation of what entities are and the custom entities used in Supply Chain Insights
author: carylhenry
ms.date: 09/01/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhery
---

# Metadata and Markdown template

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Insights organizes its data by labeling it in order to analyze it for insights. To do so, Supply Chain Insights has users ingest data by entity. 
Entities are collections of attributes that come together to make a concept. 
Supply Chain Insights contains many entities to represent different parts of a supply chain, and each of these entities have attributes to describe them. 
For example, a vendor is an entity containing attributes related to their name, location, and more. 

# Entities list

## Vendor
Entity to capture the list of vendors/suppliers that provide raw materials or components that are needed for manufacturing a company’s products.  

| Attribute            | Description                                                            | Type | Required     |
| -------------------- |------------------------------------------------------------------------| ---- | ------------ |
| VendorId             | Unique Id associated with the vendor in the system of record           |      | Required     |
| Name                 | Name of the vendor                                                     |      | Required     |
| PrimaryContactEmail  | Primary contact email for the vendor.                                  |      | Required     |
| TaxCountryRegionCode | The country where the vendor is situated.                              |      | Optional     |
| CountryRegionTaxId   | The tax id associated with the vendor in the country they’re situated. |      | Optional     |
| AddressLine1         | Primary address associated with vendor.                                |      | Optional     |
| AddressLine2         | Primary address associated with vendor.                                |      | Optional     |
| AddressCity          | City where vendor is located.                                          |      | Optional     |
| AddressState         | State where vendor is located.                                         |      | Optional     |
| AddressCountryRegion | Country where vendor is located.                                       |      | Optional     |
| AddressPostalCode    | Postal code for the vendor’s primary address.                          |      | Optional     |
| DunsNumber           | Dun & Bradstreet number for the vendor company.                        |      | Optional     |
| LexId                | LexisNexis id for the vendor company.                                  |      | Optional     |
| ExperianId           | Experian Id for the vendor company.                                    |      | Optional     |

## Customer
Entity to capture the list of customers/buyers that a company sells their end products to. 

| Attribute            | Description                                                              | Type | Required     |
| -------------------- |--------------------------------------------------------------------------| ---- | ------------ |
| CustomerId           | Unique Id associated with the customer in the system of record           |      | Required     |
| Name                 | Name of the customer                                                     |	     | Required     |
| PrimaryContactEmail  | Primary contact email for the customer.                                  | 	   | Required     |
| TaxCountryRegionCode | The country where the customer is situated.                              |  	   | Optional     |
| CountryRegionTaxId   | The tax id associated with the customer in the country they’re situated. |      | Optional     |
| AddressLine1         | Primary address associated with customer.                                |      | Optional     |
| AddressLine2         | Primary address associated with customer.                                |	     | Optional     |
| AddressCity          | City where customer is located.                                          |    	 | Optional     |
| AddressState         | State where customer is located.                                         |	     | Optional     |
| AddressCountryRegion | Country where customer is located.                                       |	     | Optional     |
| AddressPostalCode    | Postal code for the customer primary address.                            |    	 | Optional     |
| DunsNumber           | Dun & Bradstreet number for the customer company.                        |    	 | Optional     |
| LexId                | LexisNexis id for the customer company.                                  |    	 | Optional     |
| ExperianId           | Experian Id for the customer company.                                    |      | Optional     |	 	 

## Product
Entity to capture the end products that a company produces and sells their customers.
| Attribute                | Description                                                          | Type     | Required |
| -------------------------|----------------------------------------------------------------------| -------- | -------- |
| ProductId                | Unique identifier for the product                                    |          | Required |
| ProductName              | Name of the product.                                                 |          | Required |
| ProductAlternateId       | Alternate identifiers for the product                                |          | Optional |
| ProductDescription       | Description of the product.                                          |          | Optional |
| CriticalProductIndicator | Indicator                                                            | Boolean  | Optional |
| ImageUrl                 | Publicly accessible web url of the product in a catalogue            |          | Optional |
| HeightUom                | Unit of measure for the height dimension                             |          | Optional |
| WidthUom                 | Unit of measure for the width dimension                              |          | Optional | 
| LengthUom                | Unit of measure for the length dimension                             |          | Optional | 
| VolumeUom                | Unit of measure for the length dimension                             |          | Optional |
| ModelNumber              | Model number or serial number for the product                        |          | Optional |
| Color                    | Color of the product                                                 |          | Optional |
| Volume                   | Volume of the product                                                |          | Optional |
| Length                   | Length of the product                                                |          | Optional |
| Width                    | Width of the product                                                 |          | Optional |
| Height                   | Height of the product                                                |          | Optional |

## Item
Entity to capture the physical representation of goods (finished products, raw materials, sub components) in a warehouse or production plant. 
| Attribute                    | Description                                                                                   | Type | Required |
| -----------------------------|-----------------------------------------------------------------------------------------------|------|----------|                         
| ItemId                       | Unique   identifier for an item                                                               |      | Required |                             
| ItemName                     | Name   of the item                                                                            |      | Required |                            | ItemDescription              | Description   of the item                                                                     |      | Optional |                            | ProductId                    | The end   product associated with the item if item is of type finished good.                  |      | Required for finished goods |
| VendorId                     | The vendor   who supplies the item if item is of type raw material or   component.            |      | Required for all items that are raw materials) |
| VendorProductId              | The   vendors representation of the item if item is of type raw material or   component.      |      | Optional |                            | IsItemTypeWorkInProgress     | Indicator   of whether item is work in progress                                               |      | Optional |                             | IsItemTypeRawMaterial        | Indicator   of item being a raw material                                                      |      | Optional |                           
| IsItemTypeFinishedGood       | Indicator   of item being finished good                                                       |      | Optional |                           
| ItemAverageLeadTime          | Average   number of days it takes to procure a raw material from a   supplier.                |      | Required | 
| lwhUom                       | Length   width height unit of measure                                                         |      | Optional |
| ItemHeight                   | Height   of the item                                                                          |      | Optional |  
| ItemWidth                    | Width   of the item                                                                           |      | Optional |   
| ItemLength                   | Length   of the item                                                                          |      | Optional |  
| ItemVolumeUom                | Volume   unit of measure                                                                      |      | Optional |  
| ItemVolume                   | Volume   of the item                                                                          |      | Optional | 
| ItemWeight                   | Weight   of the item                                                                          |      | Optional | 
| WeightUomId                  | Weight   unit of measure                                                                      |      | Optional | 
| NegotiatedLeadTime           | The   agreed upon lead time between the company and supplier for a given item                 |      | Optional |
| SoleSourceItemIndicator      | Indicator   if this item is singularly sourced by a vendor                                    |      | Optional |
| SoleSourceSupplierName       | Name   of the vendor                                                                          |      | Optional | 


## Bill of material
Entity to capture the production bill of material details or the component/raw material requirement for manufacturing a product. 
| Attribute            | Description                                                              | Type | Required     |
| -------------------- |--------------------------------------------------------------------------| ---- | ------------ |

## Warehouse
Entity to capture the warehouse locations and contacts details. 
| Attribute            | Description                                                              | Type | Required     |
| -------------------- |--------------------------------------------------------------------------| ---- | ------------ |

## Warehouse item available stock
Entity to capture the available stock in warehouses.  
| Attribute            | Description                                                              | Type | Required     |
| -------------------- |--------------------------------------------------------------------------| ---- | ------------ |


## Production plant
Entity to capture the location and contact details for production plants.  
| Attribute            | Description                                                              | Type | Required     |
| -------------------- |--------------------------------------------------------------------------| ---- | ------------ |

## Customer product allocation
Entity to capture the quantities allocated for customers to satisfy anticipated demand. This is capturing the committed supply.  
| Attribute            | Description                                                              | Type | Required     |
| -------------------- |--------------------------------------------------------------------------| ---- | ------------ |

## Order
Entity to capture details about purchase and sales orders. 
| Attribute            | Description                                                              | Type | Required     |
| -------------------- |--------------------------------------------------------------------------| ---- | ------------ |

## Order line
Entity to capture the order line details for each purchase and sales order. 
| Attribute            | Description                                                              | Type | Required     |
| -------------------- |--------------------------------------------------------------------------| ---- | ------------ |

## Shipment
Entity to capture details about inbound and outbound shipments associated with a warehouse.  
| Attribute            | Description                                                              | Type | Required     |
| -------------------- |--------------------------------------------------------------------------| ---- | ------------ |

## Shipment item
Entity to capture details about what part of an order is contained in a single shipment.
| Attribute            | Description                                                              | Type | Required     |
| -------------------- |--------------------------------------------------------------------------| ---- | ------------ |

## Production order
Entity to capture details about the production orders that are raised to meet customer demand in response to purchase orders or to replenish stock.  
| Attribute            | Description                                                              | Type | Required     |
| -------------------- |--------------------------------------------------------------------------| ---- | ------------ |

## Master plan schedule
Entity to capture the build plan details – what is being produced, in what quantity and when.
| Attribute            | Description                                                              | Type | Required     |
| -------------------- |--------------------------------------------------------------------------| ---- | ------------ |

## Material resource plan
Entity to capture the material resource plan which tells us the quantity of items required to satisfy demand for an end product and to achieve the master plan schedule.  
| Attribute            | Description                                                              | Type | Required     |
| -------------------- |--------------------------------------------------------------------------| ---- | ------------ |
