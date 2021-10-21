---
title: Entities
description: This topic covers entities in Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 10/14/2021
ms.topic: article
audience: Application User
ms.search.region: Global
ms.service: dynamics-365-supply-chain-insights
ms.author: carylhenry
---

# Entities

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

Entities are collections of attributes that are used to organize data in Microsoft Dynamics 365 Supply Chain Insights. Supply Chain Insights depends on organized data to effectively present supply chain information so that it can be analyzed for insights.

## Definition

Supply Chain Insights organizes its data by using labels, so that it can analyze the data for insights. To do so, Supply Chain Insights has users ingest data by entities, which are collections of attributes that together make up a concept. For example, a vendor is an entity that contains attributes that are related to the vendor's name, location, and other characteristics. Supply Chain Insights contains many entities to represent different parts of a supply chain, and each entity has attributes that describe it.

## Entity list

The following tables provide a complete list of entities and their attributes.

### Facilities

#### Warehouse

A *warehouse* entity captures details about a warehouse, such as its contact information and location.

| Attribute            | Description | Type | Required |
|----------------------|-------------|------|----------|
| WarehouseId          | The unique identifier of the warehouse. | String | Required |
| Name                 | The name of the warehouse. | String | Optional |
| Description          | The description of the warehouse. | String | Optional |
| PrimaryContactEmail  | The primary contact details for the warehouse. | String | Optional |
| PrimaryContactName   | The full name of the person to contact. | String | Optional |
| AddressLine1         | The primary street address that is associated with the warehouse. | String | Optional |
| AddressLine2         | The apartment number, suite, or other street address information that is associated with the warehouse. | String | Optional |
| AddressCity          | The city where the warehouse is located. | String | Required |
| AddressState         | The state or province where the warehouse is located. | String | Required |
| AddressCountryRegion | The country or region where the warehouse is located. | String | Required |
| AddressPostalCode    | The postal code for the warehouse's primary address. | String | Required |
| AddressLongitude     | The value will be automatically set. | String | Optional |
| AddressLatitude      | The value will be automatically set. | String | Optional |
| RegionalLongitude    | The value will be automatically set. | String | Optional |
| RegionalLatitude     | The value will be automatically set. | String | Optional |

### Products

#### Item

An *item* entity captures physical representation details about a good in a warehouse or production plant. A good can be a finished product, a part, or a raw material.

| Attribute                | Description | Type | Required |
|--------------------------|-------------|------|----------|
| ItemId                   | The unique identifier of the item. | String | Required |
| ItemName                 | The name of the item. | String | Required |
| ItemDescription          | The description of the item. | String | Optional |
| ProductId                | The end product that is associated with the item, if it's a finished good. | String | Required for finished goods |
| VendorId                 | The vendor that supplies the item, if it's a part or raw material. | String | Required for parts and raw materials |
| VendorProductId          | The vendor's representation of the item, if it's a part or raw material. | String | Optional |
| IsItemTypeWorkInProgress | A flag that indicates whether the item is work in progress. | Boolean | Optional |
| IsItemTypeRawMaterial    | A flag that indicates whether the item is a raw material. | Boolean | Optional |
| IsItemTypeFinishedGood   | A flag that indicates whether the item is a finished good. | Boolean | Optional |
| ItemAverageLeadTime      | The average number of days that is required to procure a raw material from a supplier. | Integer | Required |
| lwhUom                   | The unit of measure for the length, width, and height. | String | Optional |
| ItemHeight               | The height of the item. | Integer | Optional |
| ItemWidth                | The width of the item. | Integer | Optional |
| ItemLength               | The length of the item. | Integer | Optional |
| ItemVolumeUomId          | The unit of measure for the volume. | String | Optional |
| ItemVolume               | The volume of the item. | Integer | Optional |
| ItemWeight               | The weight of the item. | Integer | Optional |
| WeightUomId              | The unit of measure for the weight. | String | Optional |
| SoleSourceSupplierName   | The name of the vendor. | String | Optional |
| SoleSourceItemIndicator  | A flag that indicates whether the item is singularly sourced by a vendor. | Boolean | Optional |
| NegotiatedLeadTime       | The agreed-on lead time between the company and supplier for the item. | Integer | Optional |

#### Product

A *product* entity captures details about end products that a company produces and sells to its customers.

| Attribute                | Description | Type | Required |
|--------------------------|-------------|------|----------|
| ProductId                | The unique identifier of the product. | String | Required |
| ProductName              | The name of the product. | String | Required |
| ProductAlternateId       | Alternate identifiers for the product. | String | Optional |
| ProductDescription       | The description of the product. | String | Optional |
| CriticalProductIndicator | A flag that indicates whether the product is a critical product. | Boolean | Optional |
| ImageUrl                 | The publicly accessible web address of the product in a catalog. | String | Optional |
| HeightUom                | The unit of measure for the height dimension. | String | Optional |
| WidthUom                 | The unit of measure for the width dimension. | String | Optional |
| LengthUom                | The unit of measure for the length dimension. | String | Optional |
| VolumeUom                | The unit of measure for the volume dimension. | String | Optional |
| ModelNumber              | The model number or serial number for the product. | String | Optional |
| Color                    | The color of the product. | String | Optional |
| Volume                   | The volume of the product. | Integer | Optional |
| Length                   | The length of the product. | Integer | Optional |
| Width                    | The width of the product. | Integer | Optional |
| Height                   | The height of the product. | Integer | Optional |

### Bill of material lines

A *bill of material lines* entity captures details about the production bill of materials (BOM) or the parts/raw materials that are required to manufacture a product.

| Attribute            | Description | Type | Required |
|----------------------|-------------|------|----------|
| BillofMaterialLineId | The unique identifier of the BOM. | String | Required |
| ItemId               | The parent item identifier in the BOM. | String | Required |
| ComponentItemId      | The component item identifier. | String | Required |
| BomLevel             | The level of the BOM (in the case of a multi-level BOM). | Integer | Optional |
| ComponentQuantity    | The quantity of the component item that is required to manufacture the parent item. | Integer | Optional |
| UnitOfMeasureId      | The unit of measure that is used for item quantities. | String | Optional |
| ProductId            | The product that is associated with the parent item. | String | Optional |

### Partners

#### Customer

A *customer* entity captures details about customers that a company sells its end products to.

| Attribute            | Description | Type | Required |
|----------------------|-------------|------|----------|
| CustomerId           | The unique identifier that is associated with the customer in the system of record. | String | Required |
| Name                 | The name of the customer. | String | Required |
| PrimaryContactEmail  | The primary contact email address for the customer. | String | Required |
| TaxCountryRegionCode | The country or region where the customer is located. | String | Optional |
| CountryRegionTaxId   | The tax ID that is associated with the customer in the country or region where it's located. | String | Optional |
| AddressLine1         | The primary street address that is associated with the customer. | String | Optional |
| AddressLine2         | The apartment number, suite, or other street address information that is associated with the customer. | String | Optional |
| AddressCity          | The city where the customer is located. | String | Optional |
| AddressState         | The state or province where the customer is located. | String | Optional |
| AddressCountryRegion | The country or region where the customer is located. | String | Optional |
| AddressPostalCode    | The postal code for the customer's primary address. | String | Optional |
| DunsNumber           | The Dun & Bradstreet number for the customer company. | String | Optional |
| LexId                | The LexisNexis ID for the customer company. | String | Optional |
| ExperianId           | The Experian ID for the customer company. | String | Optional |

#### Vendor

A *vendor* entity captures details about vendors that supply raw materials or components that are required to manufacture a company's products.

| Attribute            | Description | Type | Required |
|----------------------|-------------|------|----------|
| VendorId             | The unique identifier that is associated with the vendor in the system of record. | String | Required |
| Name                 | The name of the vendor. | String | Required |
| PrimaryContactEmail  | The primary contact email address for the vendor. | String | Required |
| TaxCountryRegionCode | The country or region where the vendor is located. | String | Optional |
| CountryRegionTaxId   | The tax ID that is associated with the vendor in the country or region where it's located. | String | Optional |
| AddressLine1         | The primary street address that is associated with the vendor. | String | Optional |
| AddressLine2         | The apartment number, suite, or other street address information that is associated with the vendor. | String | Optional |
| AddressCity          | The city where the vendor is located. | String | Optional |
| AddressState         | The state or province where the vendor is located. | String | Optional |
| AddressCountryRegion | The country or region where the vendor is located. | String | Optional |
| AddressPostalCode    | The postal code for the vendor's primary address. | String | Optional |
| DunsNumber           | Dun & Bradstreet number for the vendor company. | String | Optional |
| LexId                | The LexisNexis ID for the vendor company. | String | Optional |
| ExperianId           | The Experian ID for the vendor company. | String | Optional |

### Orders

#### Order

An *order* entity captures details about purchase orders and sales orders.

| Attribute                  | Description | Type | Required |
|----------------------------|-------------|------|----------|
| OrderId                    | The unique identifier of the order. It can be the same as the purchase order or sales order number. | String | Required |
| OrderType                  | The type of order: purchase or sales. | String | Required |
| PurchaseOrderNumber        | The purchase order number for the order. | String | Required |
| VendorId                   | The identifier of the vendor that the order is raised for (in the case of a purchase order). | String | Optional |
| CustomerId                 | The identifier of the customer that the order is raised for (in the case of a sales order). | String | Optional |
| OrderReceivedDate          | The date when the order was received. | ISO 8601 format | Optional |
| OrderConfirmedDate         | The date when the order was confirmed. | ISO 8601 format | Optional |
| OrderRequestedDeliveryDate | The date when the order was requested to be completed. | ISO 8601 format | Required |
| OrderCommittedDeliveryDate | The date when the order was committed to be completed. | ISO 8601 format | Required |
| OrderActualDeliveryDate    | The date when the order was actually completed. | ISO 8601 format | Optional |
| IssueDate                  | The date when the order was raised. | ISO 8601 format | Optional |
| ReturnedDate               | The date when order items were returned. | ISO 8601 format | Optional |
| CancellationDate           | The date when the order was canceled. | ISO 8601 format | Optional |
| ShipToParty                | The name of the company or person that the order must be shipped to. | String | Optional |
| CarrierId                  | The identifier of the carrier that ships the order. It can be System or a Standard Carrier Alpha Code (SCAC). | String | Optional |
| ShipmentMethod             | The method that is being used to ship the order (for example, 2 days, overnight, or ground). | String | Optional |
| AddressLine1               | The street address that is mentioned in the order. | String | Optional |
| AddressLine2               | The apartment number, suite, or other street address information that is mentioned in the order. | String | Optional |
| AddressCity                | The city from the address that is mentioned in the order. | String | Optional |
| AddressState               | The state or province from the address that is mentioned in the order. | String | Optional |
| AddressCountryRegion       | The country or region from the address that is mentioned in the order. | String | Optional |
| AddressPostalCode          | The postal code from the address that is mentioned in the order. | String | Optional |
| Status                     | The order status: completed or in progress. | String | Optional |
| ConfirmationTimestamp      | The timestamp that indicates when the order was confirmed. | ISO 8601 format | Optional |
| ReceivedTimestamp          | The timestamp that indicates when the order was received. | ISO 8601 format | Optional |
| ConfirmationNumber         | The acknowledgment that the order was received and confirmed. | String | Optional |
| Quantity                   | The ordered quantity. | Integer | Optional |

#### Order line

An *order line* entity captures order line details for each purchase and sales order.

| Attribute                          | Description | Type | Required |
|------------------------------------|-------------|------|----------|
| OrderLineDescription               | The description of the order line. | String | Optional |
| OrderId                            | The identifier of the order that contains the order line. | String | Required |
| OrderLineId                        | The unique identifier of the order line. It can be the same as the purchase order line number. | String | Required |
| PurchaseOrderLineNumber            | The corresponding purchase order line number. | String | Required |
| OrderLineStatus                    | The status: completed or in progress. | String | Required |
| WarehouseId                        | The identifier of the warehouse that is servicing the order. | String | Required |
| ItemId                             | The identifier of the item that is being ordered. | String | Required |
| WarehouseAddress                   | The address of the warehouse. | String | Optional |
| VendorItemNumber                   | For purchases orders, the identifier of the item in the vendor's system. | String | Optional |
| ConfirmedShippingDate              | The date when the shipment that is associated with the order is confirmed to be shipped. | ISO 8601 format | Optional |
| ConfirmedDeliveryDate              | The date when the shipment that is associated with the order is confirmed to be delivered. | ISO 8601 format | Required |
| ActualDeliveryTimestamp            | The date when the order line is actually completed. | ISO 8601 format | Optional |
| PlannedDeliveryDate                | The estimated delivery date of the order line. | ISO 8601 format | Optional |
| PlannedShipmentDate                | The estimated ship date of the order line. | ISO 8601 format | Required |
| PlannedPickDate                    | The estimated picking or packing date of the order line. | ISO 8601 format | Optional |
| CommittedDeliveryDate              | The committed ship or delivery date of the order. | ISO 8601 format | Optional |
| RequestedDeliveryDate              | The customer-requested delivery or ship date. | ISO 8601 format | Required |
| ActualPickTimestamp                | The actual picking or packing date and time of the order line. | ISO 8601 format | Optional |
| ActualShipmentTimestamp            | The actual ship date and time of the order. | ISO 8601 format | Optional |
| OrderLineQuantityUnitOfMeasurement | The unit of measure (for example, KG, EA, or LB) that describes the amount that is being shipped. | String | Optional |
| OrderLineQuantity                  | The amount of the order line item that is being shipped. | Integer | Optional |
| ReturnedQuantity                   | The amount of the order line item that was returned. | Integer | Optional |
| CancelledQuantity                  | The amount of the order line item that was canceled. | Integer | Optional |
| AcceptedQuantity                   | The confirmed amount of the line item that will be shipped. | Integer | Optional |

### Shipments

#### Shipment item

A *shipment item* entity captures details about the part of an order that is contained in a single shipment.

| Attribute            | Description | Type | Required |
|----------------------|-------------|------|----------|
| ShipmentId           | The unique identifier of the shipment. | String | Required |
| OrderId              | The order that is associated with the shipment or shipment item. | String | Required |
| OrderLineId          | The order line that is associated with the shipment or shipment item. | String | Required |
| ShipmentItemQuantity | The quantity of the item that is being shipped. | Integer | Optional |

#### Shipment

A *shipment* entity captures details about inbound and outbound shipments that are associated with a warehouse.

| Attribute            | Description | Type | Required |
|----------------------|-------------|------|----------|
| ShipmentId           | The unique identifier of the shipment. | String | Required |
| VendorId             | The vendor that is sending the shipment (in the case of inbound shipments). | String | Required |
| CustomerId           | The customer that is receiving the shipment (in the case of outbound shipments). | String | Required |
| ReceivingWarehouseId | The warehouse that is receiving the shipment. | String | Required |
| SendingWarehouseId   | The warehouse that is sending the shipment. | String | Required |
| CarrierName          | The name of the carrier. | String | Optional |
| CarrierType          | The type of carrier. | String | Optional |
| TrackingNumber       | The tracking number for the shipment. | String | Optional |
| ShipFromAddress      | The source address of the shipment. | String | Required |
| ShipToAddress        | The destination address of the shipment. | String | Required |
| ShipmentType         | The type of shipment: inbound or outbound. | String | Required |
| PlannedShippedDate   | The projected shipment date. | ISO 8601 format | Required |
| ActualShippedDate    | The date when the shipment was shipped. | ISO 8601 format | Required |
| EstimatedArrivalDate | The date when the shipment is expected to arrive. | ISO 8601 format | Required |
| ShipmentReceivedDate | The date when shipment actually arrived. | ISO 8601 format | Required |

### Production

#### Customer product allocation

A *customer product allocation* entity captures the quantities that are allocated for customers to satisfy anticipated demand. In other words, it captures the committed supply.

| Attribute                            | Description | Type | Required |
|--------------------------------------|-------------|------|----------|
| WarehouseId                          | The identifier of the warehouse that contains the item. | String | Required |
| CustomerProductAllocationId          | The unique identifier of the customer product allocation entry. | String | Required |
| CustomerId                           | The identifier of the customer whose demand is being met. | String | Required |
| VendorId                             | The supplier of the part, component, or goods. | String | Required |
| ItemId                               | The identifier of the item or component. | String | Required |
| AllocationQuantity                   | The quantity of stock that is allocated for the customer over the specified period. | Integer | Required |
| ConfirmedAllocationQuantity          | The actual quantity that can be allocated for the customer. | Integer | Optional |
| ConfirmedToDeliverAllocationQuantity | The quantity of stock that can be delivered to the customer out of the allocated stock. | Integer | Optional |
| PeriodStartDate                      | The first date that the allocation quantity is valid. | ISO 8601 format | Required |
| PeriodEndDate                        | The last date that the allocation quantity is valid. | ISO 8601 format | Required |

#### Master plan schedule

A *master plan schedule* entity captures the build plan details, such as what is being produced, in what quantity, and when.

| Attribute                 | Description | Type | Required |
|---------------------------|-------------|------|----------|
| MasterPlanScheduleId      | The unique identifier of the master plan. | String | Required |
| MaterialResourcePlanId    | The material resource plan that is associated with the master schedule. | String | Required |
| ItemId                    | The item that is being produced. | String | Required |
| ActualProductionQuantity  | The quantity of material that was actually produced at the end of the period. | Integer | Optional |
| PlannedProductionQuantity | The quantity of material that is projected to be produced by the end of the period. | Integer | Required |
| UnitOfMeasure             | The unit of measure (for example, KG, EA, or LB) that describes the amount that is being produced. | String | Optional |
| PeriodStartDate           | The first date that the master plan is valid. | ISO 8601 format | Required |
| PeriodEndDate             | The last date that the master plan is valid. | ISO 8601 format | Required |

#### Material resource plan

A *material resource plan* entity captures details about the material resource plan that contains the quantity of items that is required to satisfy demand for an end product and achieve the master plan schedule.

| Attribute              | Description | Type | Required |
|------------------------|-------------|------|----------|
| MaterialResourcePlanId | The unique identifier of the master resource plan. | String | Required |
| ItemId                 | The item that is involved in the master resource plan forecast. It can be a finished good or raw material. | String | Required |
| QuantityRequired       | The quantity of the item that required to satisfy demand. | Integer | Required |
| QuantityUnitOfMeasure  | The unit of measure for the item quantity. | String | Optional |
| PeriodStartDate        | The start date of the master resource plan. | ISO 8601 format | Required |
| PeriodEndDate          | The end date of the master resource plan. | ISO 8601 format | Required |
 
#### Production order

A *production order* entity captures details about the production orders that are raised to meet customer demand in response to purchase orders or to replenish stock.

| Attribute                       | Description | Type | Required |
|---------------------------------|-------------|------|----------|
| ProductionOrderId               | The unique identifier of the production order. | String | Required |
| ProductionPlantId               | The production plant that is fulfilling the production order. | String | Required |
| ItemId                          | The item that is being produced. | String | Required |
| OrderId                         | The purchase order or sales order that is associated with the production order. | String | Required |
| OrderLineId                     | The purchase order line or sales order lines that is associated with the production order. | String | Optional |
| MasterPlanScheduleId            | The master schedule that the production order is part of. | Integer | Optional |
| ItemManufacturedPlannedQuantity | The planned quantity of the item to manufacture. | Integer | Optional |
| ItemManufacturedActualQuantity  | The actual quantity that was manufactured at the end of the period. | String | Optional |
| ItemManufacturedPlannedUom      | The unit of measure for the item quantity. | String | Optional |
| ActualStartDate                 | The actual date when production starts. | ISO 8601 format | Optional |
| ActualEndDate                   | The actual date when production ends. | ISO 8601 format | Optional |
| OrderPlannedStartDate           | The estimated date to start production. | ISO 8601 format | Optional |
| OrderActualStartDate            | The estimated date to end production. | ISO 8601 format | Optional |

#### Production plant

A *production plant* entity captures the location and contact details for production plants.

| Attribute              | Description | Type | Required |
|------------------------|-------------|------|----------|
| ProductionPlantId      | The unique identifier of the production plant. | String | Required |
| Name                   | The name of the production plant. | String | Required |
| Description            | The description of the production plant. | String | Optional |
| RawMaterialWarehouseId | The identifier of the dedicated warehouse that is associated with the production plant where raw materials are stored. | String | Optional |
| OutputWarehouseId      | The identifier of the dedicated warehouse where finished goods from the production plant are stored. | String | Optional |
| PrimaryContactEmail    | The primary contact details for the production plant. | String | Optional |
| PrimaryContactName     | The full name of the person to contact. | String | Optional |
| AddressLine1           | The primary street address that is associated with the production plant. | String | Required |
| AddressLine2           | The apartment number, suite, or other street address information that is associated with the production plant. | String | Required |
| AddressCity            | The city where the warehouse is located. | String | Required |
| AddressState           | The state or province where the warehouse is located. | String | Required |
| AddressCountryRegion   | The country or region where the warehouse is located. | String | Required |
| AddressPostalCode      | The postal code for the warehouse's primary address. | String | Required |
| AddressLongitude       | The value will be automatically set. | String | Optional |
| AddressLatitude        | The value will be automatically set. | String | Optional |
| RegionalLongitude      | The value will be automatically set. | String | Optional |
| RegionalLatitude       | The value will be automatically set. | String | Optional |

### Supply

#### Warehouse item available stock

A *warehouse item available stock* entity captures details about available stock in warehouses.

| Attribute                    | Description | Type | Required |
|------------------------------|-------------|------|----------|
| WarehouseId                  | The identifier of the warehouse where the stock is located. | String | Required |
| ItemId                       | The identifier of the item that stock is being recorded for. | String | Required |
| VendorId                     | If the item is procured, the identifier of the vendor that is supplying it. | String | Required for raw materials |
| PlannedItemAvailableQuantity | The estimated stock levels for the item. | Integer | Optional |
| ActualItemQuantity           | The actual stock levels for the item. | Integer | Required |
| AllocationQuantity           | The quantity of stock that is reserved either as safety stock or to meet customer demand. | Integer | Optional |
| AnticipationStockQuantity    | The quantity of stock that is expected through inbound shipments. | Integer | Optional |
| AvailableToPromiseQuantity   | The quantity of stock that is available to service new demand. | Integer | Optional |
| FillRatePercentage           | The fill rate of the item or component that is supplied. The value will be automatically set. | Integer | Optional |
| ItemStatusName               | The status of the stock that is associated with the item (for example, blocked). | Number | Optional |
| Timestamp                    | The timestamp that indicates when the stock levels were updated in the system. | ISO 8601 format | Optional |
