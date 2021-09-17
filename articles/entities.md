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
| Attribute                | Description                                                                             | Type | Required |
| -------------------------|-----------------------------------------------------------------------------------------|------|----------|                         
| ItemId                   | Unique identifier for an item                                                           |      | Required |                             
| ItemName                 | Name of the item                                                                        |      | Required |                            
| ItemDescription          | Description of the item                                                                 |      | Optional |                            
| ProductId                | The end product associated with the item if item is of type finished good.              |      | Required for finished goods |
| VendorId                 | The vendor who supplies the item if item is of type raw material or   component.        |      | Required for all items that are raw materials) |
| VendorProductId          | The vendors representation of the item if item is of type raw material or component.    |      | Optional |                            
| IsItemTypeWorkInProgress | Indicator of whether item is work in progress                                           |      | Optional |                             
| IsItemTypeRawMaterial    | Indicator of item being a raw material                                                  |      | Optional |                           
| IsItemTypeFinishedGood   | Indicator of item being finished good                                                   |      | Optional |                           
| ItemAverageLeadTime      | Average number of days it takes to procure a raw material from a   supplier.            |      | Required | 
| lwhUom                   | Length width height unit of measure                                                     |      | Optional |
| ItemHeight               | Height of the item                                                                      |      | Optional |  
| ItemWidth                | Width of the item                                                                       |      | Optional |   
| ItemLength               | Length of the item                                                                      |      | Optional |  
| ItemVolumeUom            | Volume unit of measure                                                                  |      | Optional |  
| ItemVolume               | Volume of the item                                                                      |      | Optional | 
| ItemWeight               | Weight of the item                                                                      |      | Optional | 
| WeightUomId              | Weight unit of measure                                                                  |      | Optional | 
| NegotiatedLeadTime       | The agreed upon lead time between the company and supplier for a given item             |      | Optional |
| SoleSourceItemIndicator  | Indicator if this item is singularly sourced by a vendor                                |      | Optional |
| SoleSourceSupplierName   | Name of the vendor                                                                      |      | Optional | 


## Bill of material
Entity to capture the production bill of material details or the component/raw material requirement for manufacturing a product. 
| Attribute            | Description                                                              | Type | Required     |
| -------------------- |--------------------------------------------------------------------------| ---- | ------------ |
| Attribute            | Description                                                              | Type |              |
| BillofMaterialLineId | Unique   identifier for the bill of material                             |      | Required     |
| ItemId               | The parent item identifier in the BOM                                    |      | Required     |
| ComponentItemId      | The component item identifier                                            |      | Required     |
| BomLevel             | The level of the BOM in case of multi-level BOMs                         |      | Optional     |
| ComponentQuantity    | Quantity of the component item required in manufacturing the parent item |      | Optional     |
| UnitOfMeasureId      | Unit of measure used for item quantities                                 |      | Optional     |
| ProductId            | Product associated with parent item                                      |      | Optional     |

## Warehouse
Entity to capture the warehouse locations and contacts details. 
| Attribute            | Description                                                              | Type | Required     |
| -------------------- |--------------------------------------------------------------------------| ---- | ------------ | 
| WarehouseId          | Unique   identifier for the warehouse                                    |      | Required     |
| Name                 | Name   of the warehouse                                                  |      | Optional     |
| Description          | Description for the   warehouse                                          |      | Optional     |
| PrimaryContactEmail  | Primary contact details for the warehouse.                               |      | Optional     |
| PrimaryContactName   | Full name of the personto be contacted such as warehouse manager etc.    |      | Optional     |
| AddressLine1         | Primary address associated with warehouse.                               |      | Optional     |
| AddressLine2         | Primary address associated with warehouse.                               |      | Optional     |
| AddressCity          | City where warehouse is located.                                         |      | Required     |
| AddressState         | State where warehouse is located.                                        |      | Required     |
| AddressCountryRegion | Country where warehouse is located.                                      |      | Required     |
| AddressPostalCode    | Postal code for the warehouse primary address.                           |      | Required     |
| AddressLongitude     |                                                                          |      | Optional     |
| Addresslatitude      |                                                                          |      | Optional     |

## Warehouse item available stock
Entity to capture the available stock in warehouses.  
| Attribute                     | Description                                                              | Type | Required     |
| ----------------------------- |--------------------------------------------------------------------------| ---- | ------------ | 
| WarehouseItemAvailableStockId | Unique identifier for each of the stock entries                          |      | Required     |
| WarehouseId                   | Identifierfor the warehouse where the stock is located                   |      | Required     |
| ItemId                        | Identifier fo the item whose stock is being recorded                     |      | Required     |
| VendorId                      | If item is procured, identifier of the vendor who is supplying it        |      | Required for raw materials  |
| PlannedItemAvailableQuantity  | Estimated stock levels for an item                                       |      | Optional     |
| ActualItemQuantity            | Actual stock levels for an item                                          |      | Required     |
| AllocationQuantity            | Quantity of stock reserved either as safety stock or to meet customer demand  | | Optional     |
| AnticipationStockQuantity     | Quantity of stock expected through inbound shipments                     |      | Optional     |
| AvailableToPromiseQuantity    | Quantity of stock available to service new demand. Actual item quantity – allocation quantity + anticipation stock quantity |   | Optional    |
| FillRatePercentage            | (N/A for this release)                                                   |      | Optional     |
| ItemStatusName                | Status for the stock associated with an item. Ex: blocked                |      | Optional     |
| Timestamp                     | Timestamp when the stock levels were updated in the system               |      | Optional     |

## Production plant
Entity to capture the location and contact details for production plants.  
| Attribute              | Description                                                              | Type | Required     |
| ---------------------- |--------------------------------------------------------------------------| ---- | ------------ |
| ProductionPlantId      | Unique identifier for the production plant                               |      | Required     |
| Name                   | Name of the production plant                                             |      | Required     |
| Description            | Description for the production plant                                     |      | Optional     |
| RawMaterialWarehouseId | Identifier of the dedicated warehouse associated with the production plant where raw materials are stored |    | Optional  |
| OutputWarehouseId      | Identifier of the dedicated warehouse where finished goods from the production plant are stored           |    | Optional  |
| PrimaryContactEmail    | Primary contact details for reaching the production plant.               |       |              |
| PrimaryContactName     | Full name of the person to be contacted.                                 |       | Optional     |
| AddressLine1           | Primary address associated with warehouse.                               |       | Required     |
| AddressLine2           | Primary address associated with warehouse.                               |       | Required     |
| AddressCity            | City where warehouse is located.                                         |       | Required     |
| AddressState           | State where warehouse is located.                                        |       | Required     |
| AddressCountryRegion   | Country where warehouse is located.                                      |       | Required     |           
| AddressPostalCode      | Postal code for the warehouse primary address.                           |       | Required     |
| AddressLongitude       |                                                                          |       | Optional     |
| Addresslatitude        |                                                                          |       | Optional     |


## Customer product allocation
Entity to capture the quantities allocated for customers to satisfy anticipated demand. This is capturing the committed supply.  
| Attribute                            | Description                                                                         | Type | Required     |
| ------------------------------------ |-------------------------------------------------------------------------------------| ---- | ------------ |
| CustomerProductAllocationId          |	Unique identifier for the customer product allocation entry                        |	    | Required     | 
| WarehouseId                          | Identifier for the warehouse which contains the item 	 	                           |      | Required     | 
| ItemId 	                             | Identifier for the item  	                                                         |      | Required     |
| CustomerId                           |	Identifier of the customer whose demand is being met 	                             |      | Required     | 
| PeriodStartDate                      |                                                                                     | 	 	  | Required     | 
| PeriodEndDate 	 	                   | 	                                                                                   |      | Required     | 
| AllocationQuantity                   |	Quantity of stock allocated for the customer over the specified time period.       |      | Required     | 
| ConfirmedAllocationQuantity          |	Actual quantity that can be allocated for the customer.                            |      | Optional     | 
| ConformedToDeliverAllocationQuantity | Quantity of stock that can be delivered to the customer out of the allocated stock. | 	    |	Optional     |

## Order
Entity to capture details about purchase and sales orders. 
| Attribute                  | Description                                                                      | Type | Required |
| -------------------------- |----------------------------------------------------------------------------------| ---- | -------- |
| Id                         |                                                                                  |      | Required |
| OrderId                    | Unique identifier for the order. Can be same as PO number or sales order number. |      | RequireD |
| OrderType                  | Type of order: purchase or sales                                                 |      | Required |
| PurchaseOrderNumber        | PO number for the order                                                          |      | Required |
| VendorId                   | Identifier of the vendor the order is raised for. (In case of PO)                |      | Optional |
| CustomerId                 | Identifier of the customer the order is raised for (in case of sales order)      |      | Optional |
| OrderReceivedDate          | Date when order was received                                                     |      | Optional |
| OrderConfirmedDate         | Date when order was confirmed                                                    |      | Optional |
| OrderRequestedDeliveryDate | Date when order was requested to be completed                                    |      | Required |
| OrderCommittedDeliveryDate | Date when order was committed to be completed                                    |      | Required |
| OrderActualDeliveryDate    | Date when order was actually completed                                           |      | Optional |
| IssueDate                  | Date when order was raised                                                       |      | Optional |
| ReturnedDate               | N/A for April release                                                            |      | Optional |
| CancelationDate            | Date when order was cancelled                                                    |      | Optional |
| ShipToParty                | Name of the company/person the order is to be shipped to.                        |      | Optional |
| CarrierId                  | N/A for April release                                                            |      | Optional |
| ShipmentMethod             | N/A for April release                                                            |      | Optional |
| AddressLine1               | Address mentioned in the PO or sales order                                       |      | Optional |
| AddressLine2               | Address mentioned in the PO or sales order                                       |      | Optional |
| AddressCity                | Address mentioned in the PO or sales order                                       |      | Optional |
| AddressState               | Address mentioned in the PO or sales order                                       |      | Optional |
| AddressCountryRegion       | Address mentioned in the PO or sales order                                       |      | Optional |
| AddressPostalCode          | Address mentioned in the PO or sales order                                       |      | Optional |
| Status                     | Order status: completed, in progress                                             |      | Optional |
| ConfirmationTimestamp      | Timestamp when order was confirmed                                               |      | Optional |
| ReceivedTimestamp          | Timestamp when order was received                                                |      | Optional |
| ConfirmationNumber         | Acknowledgment for order being received and confirmed                            |      | Optional |
| Quantity                   | N/A for April release                                                            |      | Optional |


## Order line
Entity to capture the order line details for each purchase and sales order. 

| Attribute                          | Description                                                                    | Type | Required |
| ---------------------------------- |--------------------------------------------------------------------------------| ---- | -------- |
| OrderLineId                        | Unique identifier for the order line. Cane be same as PO line number           |      | Required |
| OrderId                            | Identifier of the order that contains the order line                           |      | Required |
| OrderLineDescription               | Description of the order line                                                  |      | Optional |
| PurchaseOrderLineNumber            | Corresponding PO line number                                                   |      | Required |
| OrderLineStatus                    | Status: completed, in progress                                                 |      | Required |
| WarehouseId                        | Identifier of the warehouse servicing the order                                |      | Required |
| ItemId                             | Identifier of the item being ordered                                           |      | Required |
| WarehouseAddress                   | Address of the warehouse                                                       |      | Optional |
| VendorItemNumber                   | For PO, this is the identifier of the item in the vendor’s system              |      | Optional |
| ConfirmedShippingDate              | Date when the shipment associated with the order is confirmed to be shipped    |      | Optional |
| ConfirmedDeliveryDate              | Date when the shipment associated with the order is confirmed to be delivered  |      | Required |
| ActualDeliveryTimestamp            | Date when the order line is actually completed                                 |      | Optional |
| PlannedDeliveryDate                | Date when the order line is estimated to ship                                  |      | Optional |
| PlannedShipmentDate                |                                                                                |      | Required |
| PlannedPickDate                    | N/A for April release                                                          |      | Optional |
| CommittedDeliveryDate              |                                                                                |      | Optional |
| RequestedDeliveryDate              |                                                                                |      | Required |
| ActualPickTimestamp                | N/A for April release                                                          |      | Optional |
| ActualShipmentTimestamp            |                                                                                |      | Optional |
| OrderLineQuantityUnitOfMeasurement |                                                                                |      | Optional |
| OrderLineQuantity                  |                                                                                |      | Optional |
| ReturnedQuantity                   | N/A for April release                                                          |      | Optional |
| CancelledQuantity                  |                                                                                |      | Optional |
| AcceptedQuantity                   |                                                                                |      | Optional |

## Shipment
Entity to capture details about inbound and outbound shipments associated with a warehouse.  
| Attribute            | Description                                                             | Type | Required     |
| -------------------- |-------------------------------------------------------------------------| ---- | ------------ |
| ShipmentId           | Unique identifier of the shipment                                       |      | Required     |
| VendorId             | Vendor that is sending the shipment (in case of inbound shipments)      |      | Required     |
| CustomerId           | Customer that is receiving the shipment (in case of outbound shipments) |      | Required     |
| ReceivingWarehouseId | Warehouse that is receiving a shipment                                  |      | Required     |
| SendingWarehouseId   | Warehouse that is sending a shipment                                    |      | Required     |
| CarrierName          | Name of the carrier                                                     |      | Optional     |
| CarrierType          | Type of carrier                                                         |      | Optional     |
| TrackingNumber       | Tracking number for the shipment                                        |      | Optional     |
| ShipFromAddress      | Source address of shipment                                              |      | Required     |
| ShipToAddress        | Destination address of the shipment                                     |      | Required     |
| ShipmentType         | Inbound or outbound                                                     |      | Required     |
| PlannedShippedDate   | Projected shipment date                                                 |      | Required     |
| ActualShippedDate    | Date when shipment was shipped                                          |      | Required     |
| EstimatedArrivalDate | Date when shipment is expected to arrive                                |      | Required     |
| ShipmentReceivedDate | Date when shipment actually arrived                                     |      |              |

## Shipment item
Entity to capture details about what part of an order is contained in a single shipment.
| Attribute            | Description                                              | Type | Required |
| ShipmentItemId       | Unique identifier for the shipment line                  |      | Required |
| ShipmentId           | Unique identifier for the shipment                       |      | Required |
| OrderId              | Order associated with the shipment or shipment item      |      | Required |
| OrderLineId          | Order line associated with the shipment or shipment item |      | Required |
| ShipmentItemQuantity | Quantity of item that is being shipped                   |      | Optional |

## Production order
Entity to capture details about the production orders that are raised to meet customer demand in response to purchase orders or to replenish stock.  
| Attribute                       | Description                                                                   | Type | Required |
| ------------------------------- |-------------------------------------------------------------------------------| ---- | -------- |
| ProductionorderId               | Unique identifier for the production order                                    |      | Required |
| ItemId                          | Item that is being produced                                                   |      | Required |
| ProductionPlantId               | Production plant that is fulfilling the production order                      |      | Required |
| OrderId                         | Purchase order or sales order associated with the production order            |      | Required |
| OrderLineId                     | Purchase order line or sales order lines associated with the production order |      | Optional |
| MasterPlanScheduleId            | Master schedule that the production order is a part of                        |      | Optional |
| ItemManufacturedPlannedQuantity | Planned quantity of item to manufacture                                       |      | Optional |
| ItemManufacturedActualQuantity  | Actual quantity manufactured at the end of the time period                    |      | Optional |
| ItemManufacturedPlannedUom      | Unit of measure for item quantity                                             |      | Optional |
| ActualStartDate                 |                                                                               |      | Optional |
| ActualEndDate                   |                                                                               |      | Optional |
| OrderPlannedStartDate           |                                                                               |      | Optional |
| OrderActualStartDate            |                                                                               |      | Optional |

## Master plan schedule
Entity to capture the build plan details – what is being produced, in what quantity and when.
| Attribute                 | Description                                                                         | Type | Required |
| ------------------------- |-------------------------------------------------------------------------------------| ---- | -------- |
| MasterPlanScheduleId      | Unique identifier for a master plan                                                 |      | Required |
| ActualProductionQuantity  | The quantity of material actually produced at the end of the period                 |      | Optional |
| PlannedProductionQuantity | Quantity of material that is projected to be produced by the end of the time period |      | Required |
| Unit of Measure           |                                                                                     |      | Optional |
| ItemId                    | Item that is to be produced                                                         |      | Required |
| PeriodStartDate           |                                                                                     |      | Required |
| PeriodEndDate             |                                                                                     |      | Required |
| MaterialResourcePlanId    | Material resource plan associated with the master schedule                          |      | Required |

## Material resource plan
Entity to capture the material resource plan which tells us the quantity of items required to satisfy demand for an end product and to achieve the master plan schedule.  
| Attribute              | Description                                                                          | Type | Required |
| ---------------------- |--------------------------------------------------------------------------------------| ---- | -------- |
| MaterialResourcePlanId | Unique identifier for the MRP                                                        |      | Required |
| ItemId                 | The item that is involved in the MRP forecast. Can be finished good or raw material. |      | Required |
| PeriodStartDate        | Start date for MRP                                                                   |      | Required |
| PeriodEndDate          | End date for MRP                                                                     |      | Required |
| QuantityRequired       | The quantity of item required to satisfy demand                                      |      | Required |
| QuantityUnitOfMeasure  | Unit of measure for the item quantity                                                |      | Optional |
