---
title: Entities
description: This page contains an explanation of what entities are and the custom entities used in Supply Chain Insights
author: carylhenry
ms.date: 10/13/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhery
---

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

Entities are a critical concept for Supply Chain Insights because they are used to organize the data. Organized data is critical because this is what allows Supply Chain Insights to understand the information so it can then be analyzed for insights.


# Definition

Supply Chain Insights organizes its data by labeling it in order to analyze it for insights. To do so, Supply Chain Insights has users ingest data by entity. Entities are collections of attributes that come together to make a concept. For example, a vendor is an entity containing attributes related to their name, location, and other characteristics. Supply Chain Insights contains many of these entities to represent different parts of a supply chain, and each of these entities have attributes to describe them. A complete list of entities and their attributes can be found below.

# Entities list

## Facilities

### Warehouse
Entity to capture the details for a warehouse, such as its contact information and location.
| Attribute            | Description                                                              | Type   | Required     |
| -------------------- |--------------------------------------------------------------------------| ------ | ------------ | 
| WarehouseId          | Unique identifier for the warehouse                                      | String | Required     |
| Name                 | Name of the warehouse                                                    | String | Optional     |
| Description          | Description for the warehouse                                            | String | Optional     |
| PrimaryContactEmail  | Primary contact details for the warehouse                                | String | Optional     |
| PrimaryContactName   | Full name of the person to be contacted                                  | String | Optional     |
| AddressLine1         | Primary street address associated with warehouse                         | String | Optional     |
| AddressLine2         | Apartment number, suite, or other street address information associated with warehouse            | String | Optional     |
| AddressCity          | City where warehouse is located                                          | String | Required     |
| AddressState         | State where warehouse is located                                         | String | Required     |
| AddressCountryRegion | Country where warehouse is located                                       | String | Required     |
| AddressPostalCode    | Postal code for the warehouse primary address                            | String | Required     |
| AddressLongitude     | Will be autopopulted                                                     | String | Optional     |
| AddressLatitude      | Will be autopopulted                                                     | String | Optional     |
| RegionalLongitude    | Will be autopopulted                                                     | String | Optional     |
| RegionalLatitude     | Will be autopopulted                                                     | String | Optional     |

## Products

### Item
Entity to capture the physical representation of a good in a warehouse or production plant. A good can be a finished product, part, or raw material.
| Attribute                | Description                                                                             | Type   | Required |
| -------------------------|-----------------------------------------------------------------------------------------|--------|----------|                         
| ItemId                   | Unique identifier for an item                                                           | String | Required |                             
| ItemName                 | Name of the item                                                                        | String | Required |                            
| ItemDescription          | Description of the item                                                                 | String | Optional |                            
| ProductId                | The end product associated with the item if it's a finished good                        | String | Required for finished goods |
| VendorId                 | The vendor who supplies the item if it's a part or raw material                         | String | Required for parts and raw materials |
| VendorProductId          | The vendors representation of the item it's a part of raw material                      | String  | Optional |                            
| IsItemTypeWorkInProgress | Indicator of whether item is work in progress                                           | Boolean | Optional |                             
| IsItemTypeRawMaterial    | Indicator of item being a raw material                                                  | Boolean | Optional |                           
| IsItemTypeFinishedGood   | Indicator of item being finished good                                                   | Boolean | Optional |                           
| ItemAverageLeadTime      | Average number of days it takes to procure a raw material from a supplier               | Integer | Required | 
| lwhUom                   | Length width height unit of measure                                                     | String  | Optional |
| ItemHeight               | Height of the item                                                                      | Integer | Optional |  
| ItemWidth                | Width of the item                                                                       | Integer | Optional |   
| ItemLength               | Length of the item                                                                      | Integer | Optional |  
| ItemVolumeUomId          | Volume unit of measure                                                                  | String  | Optional |  
| ItemVolume               | Volume of the item                                                                      | Integer | Optional | 
| ItemWeight               | Weight of the item                                                                      | Integer | Optional | 
| WeightUomId              | Weight unit of measure                                                                  | String  | Optional | 
| SoleSourceSupplierName   | Name of the vendor                                                                      | String  | Optional | 
| SoleSourceItemIndicator  | Indicator if this item is singularly sourced by a vendor                                | Boolean | Optional |
| NegotiatedLeadTime       | The agreed upon lead time between the company and supplier for a given item             | Integer | Optional |

### Product
Entity to capture the end products that a company produces and sells their customers.
| Attribute                | Description                                                          | Type     | Required |
| -------------------------|----------------------------------------------------------------------| -------- | -------- |
| ProductId                | Unique identifier for the product                                    | String   | Required |
| ProductName              | Name of the product                                                  | String   | Required |
| ProductAlternateId       | Alternate identifiers for the product                                | String   | Optional |
| ProductDescription       | Description of the product                                           | String   | Optional |
| CriticalProductIndicator | Indicator                                                            | Boolean  | Optional |
| ImageUrl                 | Publicly accessible web url of the product in a catalogue            | String   | Optional |
| HeightUom                | Unit of measure for the height dimension                             | String   | Optional |
| WidthUom                 | Unit of measure for the width dimension                              | String   | Optional | 
| LengthUom                | Unit of measure for the length dimension                             | String   | Optional | 
| VolumeUom                | Unit of measure for the length dimension                             | String   | Optional |
| ModelNumber              | Model number or serial number for the product                        | String   | Optional |
| Color                    | Color of the product                                                 | String   | Optional |
| Volume                   | Volume of the product                                                | Integer  | Optional |
| Length                   | Length of the product                                                | Integer  | Optional |
| Width                    | Width of the product                                                 | Integer  | Optional |
| Height                   | Height of the product                                                | Integer  | Optional |

### Bill of material lines
Entity to capture the details for the production bill of materials or the parts/raw materials requirement for manufacturing a product. 
| Attribute            | Description                                                              | Type    | Required     |
| -------------------- |--------------------------------------------------------------------------| ------- | ------------ |
| BillofMaterialLineId | Unique identifier for the bill of material                               | String  | Required     |
| ItemId               | The parent item identifier in the BOM                                    | String  | Required     |
| ComponentItemId      | The component item identifier                                            | String  | Required     |
| BomLevel             | The level of the bill of materials in case of multi-level bill of materials        | Integer | Optional     |
| ComponentQuantity    | Quantity of the component item required in manufacturing the parent item | Integer | Optional     |
| UnitOfMeasureId      | Unit of measure used for item quantities                                 | String  | Optional     |
| ProductId            | Product associated with parent item                                      | String  | Optional     |

## Partners

### Customer
Entity to capture the list of customers that a company sells their end products to. 
| Attribute            | Description                                                             | Type   | Required     |
| -------------------- |-------------------------------------------------------------------------| ------ | ------------ |
| CustomerId           | Unique Id associated with the customer in the system of record          | String | Required     |
| Name                 | Name of the customer                                                    |	String | Required    |
| PrimaryContactEmail  | Primary contact email for the customer                                  | String | Required     |
| TaxCountryRegionCode | The country where the customer is situated                              | String | Optional     |
| CountryRegionTaxId   | The tax id associated with the customer in the country they’re situated | String | Optional     |
| AddressLine1         | Primary street address associated with customer                                | String | Optional     |
| AddressLine2         | Apartment number, suite, or other street address information associated with customer   |	String | Optional    |
| AddressCity          | City where customer is located                                          | String | Optional     |
| AddressState         | State where customer is located                                         |	String | Optional    |
| AddressCountryRegion | Country where customer is located                                       |	String | Optional    |
| AddressPostalCode    | Postal code for the customer primary address                            | String | Optional     |
| DunsNumber           | Dun & Bradstreet number for the customer company                        | String | Optional     |
| LexId                | LexisNexis id for the customer company                                  | String | Optional     |
| ExperianId           | Experian Id for the customer company                                    | String | Optional     |	 	

### Vendor
Entity to capture the list of vendors that supply raw materials or components that are needed for manufacturing a company’s products.  
| Attribute            | Description                                                            | Type   | Required     |
| -------------------- |------------------------------------------------------------------------| ------ | ------------ |
| VendorId             | Unique Id associated with the vendor in the system of record           | String | Required     |
| Name                 | Name of the vendor                                                     | String | Required     |
| PrimaryContactEmail  | Primary contact email for the vendor                                  | String | Required     |
| TaxCountryRegionCode | The country where the vendor is situated                              | String | Optional     |
| CountryRegionTaxId   | The tax id associated with the vendor in the country they’re situated. | String | Optional     |
| AddressLine1         | Primary street address associated with vendor                                | String | Optional     |
| AddressLine2         | Apartment number, suite, or other street address information associated with vendor   | String | Optional     |
| AddressCity          | City where vendor is located                                          | String | Optional     |
| AddressState         | State where vendor is located                                         | String | Optional     |
| AddressCountryRegion | Country where vendor is located                                       | String | Optional     |
| AddressPostalCode    | Postal code for the vendor’s primary address                          | String | Optional     |
| DunsNumber           | Dun & Bradstreet number for the vendor company                        | String | Optional     |
| LexId                | LexisNexis id for the vendor company                                  | String | Optional     |
| ExperianId           | Experian Id for the vendor company                                    | String | Optional     | 

## Orders

### Order
Entity to capture details about purchase and sales orders. 
| Attribute                  | Description                                                                      | Type            | Required |
| -------------------------- |----------------------------------------------------------------------------------| --------------- | -------- |
| OrderId                    | Unique identifier for the order. Can be same as PO number or sales order number. | String          | Required |
| OrderType                  | Type of order: purchase or sales                                                 | String          | Required |
| PurchaseOrderNumber        | Purchase order number for the order                                              | String          | Required |
| VendorId                   | Identifier of the vendor the order is raised for. (In case of PO)                | String          | Optional |
| CustomerId                 | Identifier of the customer the order is raised for (in case of sales order)      | String          | Optional |
| OrderReceivedDate          | Date when order was received                                                     | ISO 8601 format | Optional |
| OrderConfirmedDate         | Date when order was confirmed                                                    | ISO 8601 format | Optional |
| OrderRequestedDeliveryDate | Date when order was requested to be completed                                    | ISO 8601 format | Required |
| OrderCommittedDeliveryDate | Date when order was committed to be completed                                    | ISO 8601 format | Required |
| OrderActualDeliveryDate    | Date when order was actually completed                                           | ISO 8601 format | Optional |
| IssueDate                  | Date when order was raised                                                       | ISO 8601 format | Optional |
| ReturnedDate               | Date when order items were returned                                              | ISO 8601 format | Optional |
| CancellationDate           | Date when order was cancelled                                                    | ISO 8601 format | Optional |
| ShipToParty                | Name of the company/person the order is to be shipped to                         | String          | Optional |
| CarrierId                  | Identifier for carrier who ships the order. Can be System or SCAC ID             | String          | Optional |
| ShipmentMethod             | How theorder is being shipped (2 days, overnight, ground, etc)                   | String          | Optional |
| AddressLine1               | Street address mentioned in the order                                            | String          | Optional |
| AddressLine2               | Apartment number, suite, or other street address information mentioned in order  | String          | Optional |
| AddressCity                | Address mentioned in the order                                       | String          | Optional |
| AddressState               | Address mentioned in the order                                       | String          | Optional |
| AddressCountryRegion       | Address mentioned in the order                                       | String          | Optional |
| AddressPostalCode          | Address mentioned in the order                                       | String          | Optional |
| Status                     | Order status: completed, in progress                                             | String          | Optional |
| ConfirmationTimestamp      | Timestamp when order was confirmed                                               | ISO 8601 format | Optional |
| ReceivedTimestamp          | Timestamp when order was received                                                | ISO 8601 format | Optional |
| ConfirmationNumber         | Acknowledgment for order being received and confirmed                            | String          | Optional |
| Quantity                   | Ordered quantity                                                                 | Integer         | Optional |


### Order line
Entity to capture the order line details for each purchase and sales order. 
| Attribute                          | Description                                                                    | Type            | Required |
| ---------------------------------- |--------------------------------------------------------------------------------| --------------- | -------- |
| OrderLineDescription               | Description of the order line                                                  | String          | Optional |
| OrderId                            | Identifier of the order that contains the order line                           | String          | Required |
| OrderLineId                        | Unique identifier for the order line. Cane be same as the purchase order line number           | String          | Required |
| PurchaseOrderLineNumber            | Corresponding purcharse order line number                                                   | String          | Required |
| OrderLineStatus                    | Status: completed, in progress                                                 | String          | Required |
| WarehouseId                        | Identifier of the warehouse servicing the order                                | String          | Required |
| ItemId                             | Identifier of the item being ordered                                           | String          | Required |
| WarehouseAddress                   | Address of the warehouse                                                       | String          | Optional |
| VendorItemNumber                   | For purchases orders, the identifier of the item in the vendor’s system              | String          | Optional |
| ConfirmedShippingDate              | Date when the shipment associated with the order is confirmed to be shipped    | ISO 8601 format | Optional |
| ConfirmedDeliveryDate              | Date when the shipment associated with the order is confirmed to be delivered  | ISO 8601 format | Required |
| ActualDeliveryTimestamp            | Date when the order line is actually completed                                 | ISO 8601 format | Optional |
| PlannedDeliveryDate                | Date when the order line is estimated to ship                                  | ISO 8601 format | Optional |
| PlannedShipmentDate                | Estimated ship date of the order line                                          | ISO 8601 format | Required |
| PlannedPickDate                    | Estimated picking or packing date of the order line                            | ISO 8601 format | Optional |
| CommittedDeliveryDate              | Order committed ship or delivery date                                          | ISO 8601 format | Optional |
| RequestedDeliveryDate              | Customer requested delivery or ship date                                       | ISO 8601 format | Required |
| ActualPickTimestamp                | Actual order line pick or pack data and time                                   | ISO 8601 format | Optional |
| ActualShipmentTimestamp            | Actual order ship date and time                                                | ISO 8601 format | Optional |
| OrderLineQuantityUnitOfMeasurement | Unit of measure (KG, EA,LB, etc) to describe the amount being shipped          | String          | Optional |
| OrderLineQuantity                  | Amount of the order line item being shipped                                    | Integer         | Optional |
| ReturnedQuantity                   | Amount of the order line item that was returned                                | Integer         | Optional |
| CancelledQuantity                  | Amount of the order line item that was cancelled                               | Integer         | Optional |
| AcceptedQuantity                   | Confirmed amount of the line item to be shipped                                | Integer         | Optional |

## Shipments

### Shipment item
Entity to capture details about what part of an order is contained in a single shipment.
| Attribute            | Description                                              | Type    | Required |
| -------------------- |----------------------------------------------------------| ------- | -------- |
| ShipmentId           | Unique identifier for the shipment                       | String  | Required |
| OrderId              | Order associated with the shipment or shipment item      | String  | Required |
| OrderLineId          | Order line associated with the shipment or shipment item | String  | Required |
| ShipmentItemQuantity | Quantity of item that is being shipped                   | Integer | Optional |

### Shipment
Entity to capture details about inbound and outbound shipments associated with a warehouse.  
| Attribute            | Description                                                             | Type            | Required     |
| -------------------- |-------------------------------------------------------------------------| --------------- | ------------ |
| ShipmentId           | Unique identifier of the shipment                                       | String          | Required     |
| VendorId             | Vendor that is sending the shipment (in case of inbound shipments)      | String          | Required     |
| CustomerId           | Customer that is receiving the shipment (in case of outbound shipments) | String          | Required     |
| ReceivingWarehouseId | Warehouse that is receiving a shipment                                  | String          | Required     |
| SendingWarehouseId   | Warehouse that is sending a shipment                                    | String          | Required     |
| CarrierName          | Name of the carrier                                                     | String          | Optional     |
| CarrierType          | Type of carrier                                                         | String          | Optional     |
| TrackingNumber       | Tracking number for the shipment                                        | String          | Optional     |
| ShipFromAddress      | Source address of shipment                                              | String          | Required     |
| ShipToAddress        | Destination address of the shipment                                     | String          | Required     |
| ShipmentType         | Inbound or outbound                                                     | String          | Required     |
| PlannedShippedDate   | Projected shipment date                                                 | ISO 8601 format | Required     |
| ActualShippedDate    | Date when shipment was shipped                                          | ISO 8601 format | Required     |
| EstimatedArrivalDate | Date when shipment is expected to arrive                                | ISO 8601 format | Required     |
| ShipmentReceivedDate | Date when shipment actually arrived                                     | ISO 8601 format |              |

## Production

### Customer product allocation
Entity to capture the quantities allocated for customers to satisfy anticipated demand. This is capturing the committed supply.  
| Attribute                            | Description                                                                        | Type            | Required     |
| ------------------------------------ |------------------------------------------------------------------------------------| --------------- | ------------ |
| WarehouseId                          | Identifier for the warehouse which contains the item 	 	                          | String          | Required     | 
| CustomerProductAllocationId          | Unique identifier for the customer product allocation entry                        | String          | Required     | 
| CustomerId                           | Identifier of the customer whose demand is being met 	                            | String          | Required     | 
| VendorId                             | Supplier of the part, component, or goods            	                            | String          | Required     | 
| ItemId 	                             | Identifier for the item or component                                               | String          | Required     |
| AllocationQuantity                   | Quantity of stock allocated for the customer over the specified time period        | Integer         | Required     | 
| ConfirmedAllocationQuantity          | Actual quantity that can be allocated for the customer                             | Integer         | Optional     | 
| ConfirmedToDeliverAllocationQuantity | Quantity of stock that can be delivered to the customer out of the allocated stock | Integer         |	Optional     |
| PeriodStartDate                      | Starting date for when the allocation quantity is valid                            | ISO 8601 format | Required     | 
| PeriodEndDate 	 	                   | Ending date for when the allocation quantity is valid                              | ISO 8601 format | Required     | 

### Master plan schedule
Entity to capture the build plan details, including what is being produced, in what quantity, and when.
| Attribute                 | Description                                                                         | Type            | Required |
| ------------------------- |-------------------------------------------------------------------------------------| --------------- | -------- |
| MasterPlanScheduleId      | Unique identifier for a master plan                                                 | String          | Required |
| MaterialResourcePlanId    | Material resource plan associated with the master schedule                          | String          | Required |
| ItemId                    | Item that is to be produced                                                         | String          | Required |
| ActualProductionQuantity  | The quantity of material actually produced at the end of the period                 | Integer         | Optional |
| PlannedProductionQuantity | Quantity of material that is projected to be produced by the end of the time period | Integer         | Required |
| UnitOfMeasure             | Unit of measure (KG, EA,LB, etc) to describe the amount being produced              | String          | Optional |
| PeriodStartDate           | Starting date for when the master plan is valid                                     | ISO 8601 format | Required |
| PeriodEndDate             | Ending date for when the master plan is valid                                       | ISO 8601 format | Required |

### Material resource plan
Entity to capture the material resource plan which contains the quantity of items required to satisfy demand for an end product and to achieve the master plan schedule.  
| Attribute              | Description                                                                          | Type            | Required |
| ---------------------- |--------------------------------------------------------------------------------------| --------------- | -------- |
| MaterialResourcePlanId | Unique identifier for the master resource plan                                                         | String   | Required |
| ItemId                 | The item that is involved in the master resource plan forecast. Can be finished good or raw material   | String   | Required |
| QuantityRequired       | The quantity of item required to satisfy demand                                      | Integer         | Required |
| QuantityUnitOfMeasure  | Unit of measure for the item quantity                                                | String          | Optional |
| PeriodStartDate        | Start date for master resource plan                                                  | ISO 8601 format | Required |
| PeriodEndDate          | End date for master resource plan                                                    | ISO 8601 format | Required |
 
### Production order
Entity to capture details about the production orders that are raised to meet customer demand in response to purchase orders or to replenish stock.  
| Attribute                       | Description                                                                   | Type            | Required |
| ------------------------------- |-------------------------------------------------------------------------------| --------------- | -------- |
| ProductionOrderId               | Unique identifier for the production order                                    | String          | Required |
| ProductionPlantId               | Production plant that is fulfilling the production order                      | String          | Required |
| ItemId                          | Item that is being produced                                                   | String          | Required |
| OrderId                         | Purchase order or sales order associated with the production order            | String          | Required |
| OrderLineId                     | Purchase order line or sales order lines associated with the production order | String          | Optional |
| MasterPlanScheduleId            | Master schedule that the production order is a part of                        | Integer         | Optional |
| ItemManufacturedPlannedQuantity | Planned quantity of item to manufacture                                       | Integer         | Optional |
| ItemManufacturedActualQuantity  | Actual quantity manufactured at the end of the time period                    | String          | Optional |
| ItemManufacturedPlannedUom      | Unit of measure for item quantity                                             | String          | Optional |
| ActualStartDate                 | Actual date when production starts                                            | ISO 8601 format | Optional |
| ActualEndDate                   | Actual date when production ends                                              | ISO 8601 format | Optional |
| OrderPlannedStartDate           | Estimated date to start production                                            | ISO 8601 format | Optional |
| OrderActualStartDate            | Estimated date to end production                                              | ISO 8601 format | Optional |

### Production plant
Entity to capture the location and contact details for production plants.  
| Attribute              | Description                                                              | Type   | Required     |
| ---------------------- |--------------------------------------------------------------------------| ------ | ------------ |
| ProductionPlantId      | Unique identifier for the production plant                               | String | Required     |
| Name                   | Name of the production plant                                             | String | Required     |
| Description            | Description for the production plant                                     | String | Optional     |
| RawMaterialWarehouseId | Identifier of the dedicated warehouse associated with the production plant where raw materials are stored | String | Optional  |
| OutputWarehouseId      | Identifier of the dedicated warehouse where finished goods from the production plant are stored           | String | Optional  |
| PrimaryContactEmail    | Primary contact details for reaching the production plant                | String | Optional     |
| PrimaryContactName     | Full name of the person to be contacted                                  | String | Optional     |
| AddressLine1           | Primary street address associated with production plant                  | String | Required     |
| AddressLine2           | Apartment number, suite, or other street address information associated with production plant    | String | Required     |
| AddressCity            | City where warehouse is located.                                         | String | Required     |
| AddressState           | State where warehouse is located.                                        | String | Required     |
| AddressCountryRegion   | Country where warehouse is located.                                      | String | Required     |           
| AddressPostalCode      | Postal code for the warehouse primary address.                           | String | Required     |
| AddressLongitude       | Will be autopopulated                                                    | String | Optional     |
| AddressLatitude        | Will be autopopulated                                                    | String | Optional     |
| RegionalLongitude      | Will be autopopulated                                                    | String | Optional     |
| RegionalLatitude       | Will be autopopulated                                                    | String | Optional     |

## Supply
### Warehouse item available stock
Entity to capture the available stock in warehouses.  
| Attribute                     | Description                                                              | Type            | Required     |
| ----------------------------- |--------------------------------------------------------------------------| --------------- | ------------ | 
| WarehouseId                   | Identifier for the warehouse where the stock is located                  | String          | Required     |
| ItemId                        | Identifier for the item whose stock is being recorded                    | String          | Required     |
| VendorId                      | If item is procured, identifier of the vendor who is supplying it        | String          | Required for raw materials  |
| PlannedItemAvailableQuantity  | Estimated stock levels for an item                                       | Integer         | Optional     |
| ActualItemQuantity            | Actual stock levels for an item                                          | Integer         | Required     |
| AllocationQuantity            | Quantity of stock reserved either as safety stock or to meet customer demand  | Integer    | Optional     |
| AnticipationStockQuantity     | Quantity of stock expected through inbound shipments                     | Integer         | Optional     |
| AvailableToPromiseQuantity    | Quantity of stock available to service new demand                        | Integer         | Optional     |
| FillRatePercentage            | Fill rate of item or component supplied. Will be autopopulated           | Integer         | Optional     |
| ItemStatusName                | Status for the stock associated with an item (ex: blocked)               | Number          | Optional     |
| Timestamp                     | Timestamp when the stock levels were updated in the system               | ISO 8601 format | Optional     |
