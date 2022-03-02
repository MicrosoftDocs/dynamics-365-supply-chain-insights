---
title: Entities
description: This topic covers entities in Microsoft Dynamics 365 Supply Chain Insights.
author: carylhenry
ms.date: 02/22/2022
ms.topic: article
audience: Application User
ms.search.region: Global

ms.author: carylhenry

---

# Entities

[!include[banner](includes/banner.md)]
[!include[banner](includes/preview-banner.md)]

Entities are collections of attributes that are used to organize data in Microsoft Dynamics 365 Supply Chain Insights. Supply Chain Insights depends on organized data to effectively present supply chain information so that it can be analyzed for insights.

## Definition

Supply Chain Insights organizes its data by using labels. That way, it can analyze the data for insights. Supply Chain Insights has users ingest data by entities, which are collections of attributes that together make up a concept. For example, a vendor is an entity that contains attributes that are related to the vendor's name, location, and other characteristics. Supply Chain Insights contains many entities to represent different parts of a supply chain, and each entity has attributes that describe it. 

It is also important to note that an entity provides the structure to represent a concept as a way of helping users ingest their data, but the entity is not the data itself. A record of an entity represents the data for one instance of the entity, so you will most likely ingest many records for a single entity. Continuing the vendor example, the data for a vendor's name, location, and other characteristics represent a single record of a vendor.

## Entity list

The following tables provide a complete list of entities and their attributes.

> [!NOTE]
> Supply Chain Insights can ingest data for an entity that does not contain all of the required attributes, but if it doesn't contain all of the attributes, the insights provided may be limited. For example, if a record of the warehouse entity does not contain data for the AddressCity, AddressState, AddressCountryRegion, and AddressPostalCode attributes, then the warehouse can't be properly placed on the supply chain map.

### Facilities

#### Warehouse

A *Warehouse* entity captures details about a warehouse, such as its contact information and location.

| Attribute            | Description | Type | Max Length | Required |
|----------------------|-------------|------|------------|----------|
| WarehouseId          | The unique identifier of the warehouse. | String | 256 characters | Required |
| Name                 | The name of the warehouse. | String | 256 characters | Optional |
| Description          | The description of the warehouse. | String | 256 characters | Optional |
| PrimaryContactEmail  | The primary contact details for the warehouse. | String | 256 characters | Optional |
| PrimaryContactName   | The full name of the person to contact. | String | 256 characters | Optional |
| AddressLine1         | The primary street address that is associated with the warehouse. | String | 256 characters | Optional |
| AddressLine2         | The apartment number, suite, or other street address information that is associated with the warehouse. | String | 256 characters | Optional |
| AddressCity          | The city where the warehouse is located. | String | 256 characters | Required |
| AddressState         | The state or province where the warehouse is located. | String | 256 characters | Required |
| AddressCountryRegion | The country or region where the warehouse is located. | String | 256 characters | Required |
| AddressPostalCode    | The postal code for the warehouse's primary address. | String | 256 characters | Required |
| AddressLongitude     | The value will be automatically set. | String | 256 characters | Optional |
| AddressLatitude      | The value will be automatically set. | String | 256 characters | Optional |
| RegionalLongitude    | The value will be automatically set. | String | 256 characters | Optional |
| RegionalLatitude     | The value will be automatically set. | String | 256 characters | Optional |
### Products

#### Item

An *Item* entity captures physical representation details about a good in a warehouse or production plant. A good can be a finished product, a part, or a raw material.

| Attribute                | Description | Type | Max length | Required |
|--------------------------|-------------|------|------------|----------|
| ItemId                   | The unique identifier of the item. | String | 256 characters | Required |
| ItemName                 | The name of the item. | String | 256 characters | Required |
| ItemDescription          | The description of the item. | String | 256 characters | Optional |
| ProductId                | The end product that is associated with the item, if it's a finished good. | String | 256 characters | Required for finished goods |
| VendorId                 | The vendor that supplies the item, if it's a part or raw material. | String | 256 characters | Required for parts and raw materials |
| VendorProductId          | The vendor's representation of the item, if it's a part or raw material. | String | 256 characters | Optional |
| IsItemTypeWorkInProgress | A flag that indicates whether the item is work in progress. | Boolean | N/A | Optional |
| IsItemTypeRawMaterial    | A flag that indicates whether the item is a raw material. | Boolean | N/A | Optional |
| IsItemTypeFinishedGood   | A flag that indicates whether the item is a finished good. | Boolean | N/A | Optional |
| ItemAverageLeadTime      | The average number of days that is required to procure a raw material from a supplier. | Integer | 2^31 | Required |
| lwhUom                   | The unit of measure for the length, width, and height. | String | 256 characters | Optional |
| ItemHeight               | The height of the item. | Integer | 2^31 | Optional |
| ItemWidth                | The width of the item. | Integer | 2^31 | Optional |
| ItemLength               | The length of the item. | Integer | 2^31 | Optional |
| ItemVolumeUomId          | The unit of measure for the volume. | String | 256 characters | Optional |
| ItemVolume               | The volume of the item. | Integer | 2^31 | Optional |
| ItemWeight               | The weight of the item. | Integer | 2^31 | Optional |
| WeightUomId              | The unit of measure for the weight. | String | 256 characters | Optional |
| SoleSourceSupplierName   | The name of the vendor. | String | 256 characters | Optional |
| SoleSourceItemIndicator  | A flag that indicates whether the item is singularly sourced by a vendor. | Boolean | N/A | Optional |
| NegotiatedLeadTime       | The agreed-on lead time between the company and supplier for the item. | Integer | 2^31 | Optional |

#### Product

A *Product* entity captures details about end products that a company produces and sells to its customers.

| Attribute                | Description | Type | Max length | Required |
|--------------------------|-------------|------|------------|----------|
| ProductId                | The unique identifier of the product. | String | 256 characters | Required |
| ProductName              | The name of the product. | String | 256 characters | Required |
| ProductAlternateId       | Alternate identifiers for the product. | String | 256 characters | Optional |
| ProductDescription       | The description of the product. | String | 256 characters | Optional |
| CriticalProductIndicator | A flag that indicates whether the product is a critical product. | Boolean | N/A | Optional |
| ImageUrl                 | The publicly accessible web address of the product in a catalog. | String | 256 characters | Optional |
| HeightUom                | The unit of measure for the height dimension. | String | 256 characters | Optional |
| WidthUom                 | The unit of measure for the width dimension. | String | 256 characters | Optional |
| LengthUom                | The unit of measure for the length dimension. | String | 256 characters | Optional |
| VolumeUom                | The unit of measure for the volume dimension. | String | 256 characters | Optional |
| ModelNumber              | The model number or serial number for the product. | String | 256 characters | Optional |
| Color                    | The color of the product. | String | 256 characters | Optional |
| Volume                   | The volume of the product. | Integer | 2^31 | Optional |
| Length                   | The length of the product. | Integer | 2^31 | Optional |
| Width                    | The width of the product. | Integer | 2^31 | Optional |
| Height                   | The height of the product. | Integer | 2^31 | Optional |

### Bill of material lines

A *BillOfMaterialLine* entity captures details about a single line of the production bill of materials (BOM) or the parts/raw materials that are required to manufacture a product.

| Attribute            | Description | Type | Max length | Required |
|----------------------|-------------|------|------------|----------|
| BillofMaterialLineId | The unique identifier of the BOM. | String | 256 characters | Required |
| ItemId               | The parent item identifier in the BOM. | String | 256 characters | Required |
| ComponentItemId      | The component item identifier. | String | 256 characters | Required |
| BomLevel             | The level of the BOM (in the case of a multi-level BOM). | Integer | 2^31 | Optional |
| ComponentQuantity    | The quantity of the component item that is required to manufacture the parent item. | Number | 9 digits, up to 3 decimal places | Optional |
| UnitOfMeasureId      | The unit of measure that is used for item quantities. | String | 256 characters | Optional |
| ProductId            | The product that is associated with the parent item. | String | 256 characters | Optional |

### Partners

#### Customer

A *Customer* entity captures details about customers that a company sells its end products to.

| Attribute            | Description | Type | Max length | Required |
|----------------------|-------------|------|------------|----------|
| CustomerId           | The unique identifier that is associated with the customer in the system of record. | String | 256 characters | Required |
| Name                 | The name of the customer. | String | 256 characters | Required |
| PrimaryContactEmail  | The primary contact email address for the customer. | String | 256 characters | Required |
| TaxCountryRegionCode | The country or region where the customer is located. | String | 256 characters | Optional |
| CountryRegionTaxId   | The tax ID that is associated with the customer in the country or region where it's located. | String | 256 characters | Optional |
| AddressLine1         | The primary street address that is associated with the customer. | String | 256 characters | Optional |
| AddressLine2         | The apartment number, suite, or other street address information that is associated with the customer. | String | 256 characters | Optional |
| AddressCity          | The city where the customer is located. | String | 256 characters | Optional |
| AddressState         | The state or province where the customer is located. | String | 256 characters | Optional |
| AddressCountryRegion | The country or region where the customer is located. | String | 256 characters | Optional |
| AddressPostalCode    | The postal code for the customer's primary address. | String | 256 characters | Optional |
| DunsNumber           | The Dun & Bradstreet number for the customer company. | String | 256 characters | Optional |
| LexId                | The LexisNexis ID for the customer company. | String | 256 characters | Optional |
| ExperianId           | The Experian ID for the customer company. | String | 256 characters | Optional |

#### Vendor

A *Vendor* entity captures details about vendors that supply raw materials or components that are required to manufacture a company's products.

| Attribute            | Description | Type | Max length | Required |
|----------------------|-------------|------|------------|----------|
| VendorId             | The unique identifier that is associated with the vendor in the system of record. | String | 256 characters | Required |
| Name                 | The name of the vendor. | String | 256 characters | Required |
| PrimaryContactEmail  | The primary contact email address for the vendor. | String | 256 characters | Required |
| TaxCountryRegionCode | The country or region where the vendor is located. | String | 256 characters | Optional |
| CountryRegionTaxId   | The tax ID that is associated with the vendor in the country or region where it's located. | String | 256 characters | Optional |
| AddressLine1         | The primary street address that is associated with the vendor. | String | 256 characters | Optional |
| AddressLine2         | The apartment number, suite, or other street address information that is associated with the vendor. | String | 256 characters | Optional |
| AddressCity          | The city where the vendor is located. | String | 256 characters | Optional |
| AddressState         | The state or province where the vendor is located. | String | 256 characters | Optional |
| AddressCountryRegion | The country or region where the vendor is located. | String | 256 characters | Optional |
| AddressPostalCode    | The postal code for the vendor's primary address. | String | 256 characters | Optional |
| DunsNumber           | Dun & Bradstreet number for the vendor company. | String | 256 characters | Optional |
| LexId                | The LexisNexis ID for the vendor company. | String | 256 characters | Optional |
| ExperianId           | The Experian ID for the vendor company. | String | 256 characters | Optional |

### Orders

#### Order

An *Order* entity captures details about purchase orders and sales orders.

| Attribute                  | Description | Type | Max length | Required |
|----------------------------|-------------|------|------------|----------|
| OrderId                    | The unique identifier of the order. It can be the same as the purchase order or sales order number. | String | 256 characters | Required |
| OrderType                  | The type of order: purchase or sales. | String | 256 characters | Required |
| PurchaseOrderNumber        | The purchase order number for the order. | String | 256 characters | Required |
| VendorId                   | The identifier of the vendor that the order is raised for (in the case of a purchase order). | String | 256 characters | Optional |
| CustomerId                 | The identifier of the customer that the order is raised for (in the case of a sales order). | String | 256 characters | Optional |
| OrderReceivedDate          | The date when the order was received. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |
| OrderConfirmedDate         | The date when the order was confirmed. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |
| OrderRequestedDeliveryDate | The date when the order was requested to be completed. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Required |
| OrderCommittedDeliveryDate | The date when the order was committed to be completed. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Required |
| OrderActualDeliveryDate    | The date when the order was actually completed. | ISO 8601 format | Up to 7 digits for the fractional part of seconds |  Optional |
| IssueDate                  | The date when the order was raised. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |
| ReturnedDate               | The date when order items were returned. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |
| CancellationDate           | The date when the order was canceled. | ISO 8601 format | Up to 7 digits for the fractional part of seconds |  Optional |
| ShipToParty                | The name of the company or person that the order must be shipped to. | String | 256 characters | Optional |
| CarrierId                  | The identifier of the carrier that ships the order. It can be System or a Standard Carrier Alpha Code (SCAC). | String | 256 characters | Optional |
| ShipmentMethod             | The method that is being used to ship the order (for example, 2 days, overnight, or ground). | String | 256 characters | Optional |
| AddressLine1               | The street address that is mentioned in the order. | String | 256 characters | Optional |
| AddressLine2               | The apartment number, suite, or other street address information that is mentioned in the order. | String | 256 characters | Optional |
| AddressCity                | The city from the address that is mentioned in the order. | String | 256 characters | Optional |
| AddressState               | The state or province from the address that is mentioned in the order. | String | 256 characters | Optional |
| AddressCountryRegion       | The country or region from the address that is mentioned in the order. | String | 256 characters | Optional |
| AddressPostalCode          | The postal code from the address that is mentioned in the order. | String | 256 characters | Optional |
| Status                     | The order status: completed or in progress. | String | 256 characters | Optional |
| ConfirmationTimestamp      | The timestamp that indicates when the order was confirmed. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |
| ReceivedTimestamp          | The timestamp that indicates when the order was received. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |
| ConfirmationNumber         | The acknowledgment that the order was received and confirmed. | String | 256 characters | Optional |
| Quantity                   | The ordered quantity. | Integer | 2^31 | Optional |

#### Order line

An *OrderLine* entity captures order line details for each purchase and sales order.

| Attribute                          | Description | Type | Max length | Required |
|------------------------------------|-------------|------|------------|----------|
| OrderLineDescription               | The description of the order line. | String | 256 characters | Optional |
| OrderId                            | The identifier of the order that contains the order line. | String | 256 characters | Required |
| OrderLineId                        | The unique identifier of the order line. It can be the same as the purchase order line number. | String | 256 characters | Required |
| PurchaseOrderLineNumber            | The corresponding purchase order line number. | String | 256 characters | Required |
| OrderLineStatus                    | The status: completed or in progress. | String | 256 characters | Required |
| WarehouseId                        | The identifier of the warehouse that is servicing the order. | String | 256 characters | Required |
| ItemId                             | The identifier of the item that is being ordered. | String | 256 characters | Required |
| WarehouseAddress                   | The address of the warehouse. | String | 256 characters | Optional |
| VendorItemNumber                   | For purchases orders, the identifier of the item in the vendor's system. | String | 256 characters | Optional |
| ConfirmedShippingDate              | The date when the shipment that is associated with the order is confirmed to be shipped. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |
| ConfirmedDeliveryDate              | The date when the shipment that is associated with the order is confirmed to be delivered. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Required |
| ActualDeliveryTimestamp            | The date when the order line is actually completed. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |
| PlannedDeliveryDate                | The estimated delivery date of the order line. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |
| PlannedShipmentDate                | The estimated ship date of the order line. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Required |
| PlannedPickDate                    | The estimated picking or packing date of the order line. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |
| CommittedDeliveryDate              | The committed ship or delivery date of the order. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |
| RequestedDeliveryDate              | The customer-requested delivery or ship date. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Required |
| ActualPickTimestamp                | The actual picking or packing date and time of the order line. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |
| ActualShipmentTimestamp            | The actual ship date and time of the order. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |
| OrderLineQuantityUnitOfMeasurement | The unit of measure (for example, KG, EA, or LB) that describes the amount that is being shipped. | String | 256 characters | Optional |
| OrderLineQuantity                  | The amount of the order line item that is being shipped. | Integer | 2^31 | Optional |
| ReturnedQuantity                   | The amount of the order line item that was returned. | Integer | 2^31 | Optional |
| CancelledQuantity                  | The amount of the order line item that was canceled. | Integer | 2^31 | Optional |
| AcceptedQuantity                   | The confirmed amount of the line item that will be shipped. | Integer | 2^31 | Optional |

### Shipments

#### Shipment item

A *ShipmentItem* entity captures details about the part of an order that is contained in a single shipment.

| Attribute            | Description | Type | Max length | Required |
|----------------------|-------------|------|------------|----------|
| ShipmentId           | The unique identifier of the shipment. | String | 256 characters | Required |
| OrderId              | The order that is associated with the shipment or shipment item. | String | 256 characters | Required |
| OrderLineId          | The order line that is associated with the shipment or shipment item. | String | 256 characters | Required |
| ShipmentItemQuantity | The quantity of the item that is being shipped. | Integer | 2^31 |  Optional |

#### Shipment

A *Shipment* entity captures details about inbound and outbound shipments that are associated with a warehouse.

| Attribute            | Description | Type | Max length | Required |
|----------------------|-------------|------|------------|----------|
| ShipmentId           | The unique identifier of the shipment. | String | 256 characters | Required |
| VendorId             | The vendor that is sending the shipment (in the case of inbound shipments). | String | 256 characters | Required |
| CustomerId           | The customer that is receiving the shipment (in the case of outbound shipments). | String | 256 characters | Required |
| ReceivingWarehouseId | The warehouse that is receiving the shipment. | String | 256 characters | Required |
| SendingWarehouseId   | The warehouse that is sending the shipment. | String | 256 characters | Required |
| CarrierName          | The name of the carrier. | String | 256 characters | Optional |
| CarrierType          | The type of carrier. | String | 256 characters | Optional |
| TrackingNumber       | The tracking number for the shipment. | String | 256 characters | Optional |
| ShipFromAddress      | The source address of the shipment. | String | 256 characters | Required |
| ShipToAddress        | The destination address of the shipment. | String | 256 characters | Required |
| ShipmentType         | The type of shipment: inbound or outbound. | String | 256 characters | Required |
| PlannedShippedDate   | The projected shipment date. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Required |
| ActualShippedDate    | The date when the shipment was shipped. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Required |
| EstimatedArrivalDate | The date when the shipment is expected to arrive. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Required |
| ShipmentReceivedDate | The date when shipment actually arrived. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Required |

### Production

#### Customer product allocation

A *CustomerProductAllocation* entity captures the quantities that are allocated for customers to satisfy anticipated demand. In other words, it captures the committed supply.

| Attribute                            | Description | Type | Max length | Required |
|--------------------------------------|-------------|------|------------|----------|
| WarehouseId                          | The identifier of the warehouse that contains the item. | String | 256 characters | Required |
| CustomerProductAllocationId          | The unique identifier of the customer product allocation entry. | String | 256 characters | Required |
| CustomerId                           | The identifier of the customer whose demand is being met. | String | 256 characters | Required |
| VendorId                             | The supplier of the part, component, or goods. | String | 256 characters | Required |
| ItemId                               | The identifier of the item or component. | String | 256 characters | Required |
| AllocationQuantity                   | The quantity of stock that is allocated for the customer over the specified period. | Integer | 2^31 | Required |
| ConfirmedAllocationQuantity          | The actual quantity that can be allocated for the customer. | Integer | 2^31 | Optional |
| ConfirmedToDeliverAllocationQuantity | The quantity of stock that can be delivered to the customer out of the allocated stock. | Integer | 2^31 | Optional |
| PeriodStartDate                      | The first date that the allocation quantity is valid. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Required |
| PeriodEndDate                        | The last date that the allocation quantity is valid. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Required |

#### Master plan schedule

A *MasterPlanSchedule* entity captures the build plan details, such as what is being produced, in what quantity, and when.

| Attribute                 | Description | Type | Max length | Required |
|---------------------------|-------------|------|------------|----------|
| MasterPlanScheduleId      | The unique identifier of the master plan. | String | 256 characters | Required |
| MaterialResourcePlanId    | The material resource plan that is associated with the master schedule. | String | 256 characters | Required |
| ItemId                    | The item that is being produced. | String | 256 characters | Required |
| ActualProductionQuantity  | The quantity of material that was actually produced at the end of the period. | Integer | 2^31 | Optional |
| PlannedProductionQuantity | The quantity of material that is projected to be produced by the end of the period. | Integer | 2^31 | Required |
| UnitOfMeasure             | The unit of measure (for example, KG, EA, or LB) that describes the amount that is being produced. | String | 256 characters | Optional |
| PeriodStartDate           | The first date that the master plan is valid. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Required |
| PeriodEndDate             | The last date that the master plan is valid. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Required |

#### Material resource plan

A *MaterialResourcePlan* entity captures details about the material resource plan that contains the quantity of items that is required to satisfy demand for an end product and achieve the master plan schedule.

| Attribute              | Description | Type | Max length | Required |
|------------------------|-------------|------|------------|----------|
| MaterialResourcePlanId | The unique identifier of the master resource plan. | String | 256 characters | Required |
| ItemId                 | The item that is involved in the master resource plan forecast. It can be a finished good or raw material. | String | 256 characters | Required |
| QuantityRequired       | The quantity of the item that required to satisfy demand. | Integer | 2^31| Required |
| QuantityUnitOfMeasure  | The unit of measure for the item quantity. | String | 256 characters | Optional |
| PeriodStartDate        | The start date of the master resource plan. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Required |
| PeriodEndDate          | The end date of the master resource plan. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Required |
 
#### Production order

A *ProductionOrder* entity captures details about the production orders that are raised to meet customer demand in response to purchase orders or to replenish stock.

| Attribute                       | Description | Type | Max length | Required |
|---------------------------------|-------------|------|------------|----------|
| ProductionOrderId               | The unique identifier of the production order. | String | 256 characters | Required |
| ProductionPlantId               | The production plant that is fulfilling the production order. | String | 256 characters | Required |
| ItemId                          | The item that is being produced. | String | 256 characters | Required |
| OrderId                         | The purchase order or sales order that is associated with the production order. | String | 256 characters | Required |
| OrderLineId                     | The purchase order line or sales order lines that are associated with the production order. | String | 256 characters | Optional |
| MasterPlanScheduleId            | The master schedule that the production order is part of. | Integer | 2^31 | Optional |
| ItemManufacturedPlannedQuantity | The planned quantity of the item to manufacture. | Integer | 2^31 | Optional |
| ItemManufacturedActualQuantity  | The actual quantity that was manufactured at the end of the period. | String | 256 characters | Optional |
| ItemManufacturedPlannedUom      | The unit of measure for the item quantity. | String | 256 characters | Optional |
| ActualStartDate                 | The actual date when production starts. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |
| ActualEndDate                   | The actual date when production ends. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |
| OrderPlannedStartDate           | The estimated date to start production. | ISO 8601 format | Up to 7 digits for the fractional part of seconds |  Optional |
| OrderActualStartDate            | The estimated date to end production. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |

#### Production plant

A *ProductionPlant* entity captures the location and contact details for production plants.

| Attribute              | Description | Type | Max length | Required |
|------------------------|-------------|------|------------|----------|
| ProductionPlantId      | The unique identifier of the production plant. | String | 256 characters | Required |
| Name                   | The name of the production plant. | String | 256 characters | Required |
| Description            | The description of the production plant. | String | 256 characters | Optional |
| RawMaterialWarehouseId | The identifier of the dedicated warehouse that is associated with the production plant where raw materials are stored. | String | 256 characters | Optional |
| OutputWarehouseId      | The identifier of the dedicated warehouse where finished goods from the production plant are stored. | String | 256 characters | Optional |
| PrimaryContactEmail    | The primary contact details for the production plant. | String | 256 characters | Optional |
| PrimaryContactName     | The full name of the person to contact. | String | 256 characters | Optional |
| AddressLine1           | The primary street address that is associated with the production plant. | String | 256 characters | Required |
| AddressLine2           | The apartment number, suite, or other street address information that is associated with the production plant. | String | 256 characters | Required |
| AddressCity            | The city where the warehouse is located. | String | 256 characters | Required |
| AddressState           | The state or province where the warehouse is located. | String | 256 characters | Required |
| AddressCountryRegion   | The country or region where the warehouse is located. | String | 256 characters | Required |
| AddressPostalCode      | The postal code for the warehouse's primary address. | String | 256 characters | Required |
| AddressLongitude       | The value will be automatically set. | String | 256 characters | Optional |
| AddressLatitude        | The value will be automatically set. | String | 256 characters | Optional |
| RegionalLongitude      | The value will be automatically set. | String | 256 characters | Optional |
| RegionalLatitude       | The value will be automatically set. | String | 256 characters | Optional |

### Supply

#### Warehouse item available stock

A *WarehouseItemAvailableStock* entity captures details about available stock in warehouses.

| Attribute                    | Description | Type | Max length | Required |
|------------------------------|-------------|------|------------|----------|
| WarehouseId                  | The identifier of the warehouse where the stock is located. | String | 256 characters | Required |
| ItemId                       | The identifier of the item that stock is being recorded for. | String | 256 characters | Required |
| VendorId                     | If the item is procured, the identifier of the vendor that is supplying it. | String | 256 characters | 256 characters | Required for raw materials |
| PlannedItemAvailableQuantity | The estimated stock levels for the item. | Integer | 2^31 | Optional |
| ActualItemQuantity           | The actual stock levels for the item. | Integer | 2^31 | Required |
| AllocationQuantity           | The quantity of stock that is reserved either as safety stock or to meet customer demand. | Integer | 2^31 | Optional |
| AnticipationStockQuantity    | The quantity of stock that is expected through inbound shipments. | Integer | 2^31 | Optional |
| AvailableToPromiseQuantity   | The quantity of stock that is available to service new demand. | Integer | 2^31 | Optional |
| FillRatePercentage           | The fill rate of the item or component that is supplied. The value will be automatically set. | Decimal | 9 digits, up to 3 decimal places | Optional |
| ItemStatusName               | The status of the stock that is associated with the item (for example, blocked). | String | 256 characters | Optional |
| Timestamp                    | The timestamp that indicates when the stock levels were updated in the system. | ISO 8601 format | Up to 7 digits for the fractional part of seconds | Optional |

