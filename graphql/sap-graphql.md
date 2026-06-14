# SAP GraphQL Schema

SAP's public APIs are built on REST and OData (both v2 and v4), surfaced primarily through the [SAP Business Accelerator Hub](https://api.sap.com). There is no unified public GraphQL endpoint. This schema is a conceptual representation of the SAP enterprise data model as it would appear if exposed via GraphQL, covering S/4HANA, Ariba, Concur, SuccessFactors, Fieldglass, and SAP Business Technology Platform (BTP).

## Schema File

- [sap-schema.graphql](sap-schema.graphql)

## Coverage

The schema spans the full SAP intelligent enterprise suite:

### S/4HANA — Order-to-Cash
Types: `Customer`, `CustomerOrder`, `SalesOrder`, `SalesOrderItem`, `DeliveryNote`, `DeliveryNoteItem`, `Invoice`, `InvoiceItem`

### S/4HANA — Procure-to-Pay
Types: `Supplier`, `PurchaseOrder`, `PurchaseOrderItem`, `PurchaseRequisition`, `PurchaseRequisitionItem`, `GoodsReceipt`, `Contract`, `ContractItem`

### S/4HANA — Master Data
Types: `BusinessPartner`, `BusinessPartnerAddress`, `Contact`

### S/4HANA — Material Management & Logistics
Types: `Product`, `ProductCategory`, `ProductGroup`, `BillOfMaterial`, `BOMItem`, `Plant`, `StorageLocation`, `MaterialDocument`, `MaterialMovement`

### S/4HANA — Project System
Types: `Project`, `WBSElement`, `Network`, `NetworkActivity`

### S/4HANA — Finance & Controlling
Types: `CompanyCode`, `GLAccount`, `CostCenter`, `CostCenterGroup`, `Controlling`, `ProfitCenter`, `FunctionalArea`

### SAP SuccessFactors — Human Capital Management
Types: `Employee`, `EmployeePosition`, `HCMWorker`, `Payroll`, `PayrollDeduction`, `PayrollEarning`, `Leave`, `Recruitment`, `RecruitmentCandidate`, `SuccessFactorsUser`, `TimeSheet`, `TimeSheetEntry`, `BenefitsPlan`

### SAP Ariba — Procurement & Sourcing
Types: `Ariba`, `AribaRequisition`, `AribaLineItem`, `AribaBid`, `AribaBidResponse`, `AribaBidLineItem`

### SAP Concur — Travel & Expense
Types: `ConcurExpense`, `ConcurReport`

### SAP Fieldglass — External Workforce
Types: `Fieldglass`, `WorkOrder`

### SAP BTP — Platform Services
Types: `ODataService`, `BTPService`, `BTPBinding`, `StandardIdentifier`

## Named Types

| Type | Domain |
|---|---|
| `Customer` | S/4HANA Sales |
| `CustomerOrder` | S/4HANA Sales |
| `SalesOrder` | S/4HANA Sales |
| `SalesOrderItem` | S/4HANA Sales |
| `BusinessPartner` | S/4HANA Master Data |
| `BusinessPartnerAddress` | S/4HANA Master Data |
| `Contact` | S/4HANA Master Data |
| `Supplier` | S/4HANA Procurement |
| `PurchaseOrder` | S/4HANA Procurement |
| `PurchaseOrderItem` | S/4HANA Procurement |
| `Invoice` | S/4HANA Finance |
| `InvoiceItem` | S/4HANA Finance |
| `PurchaseRequisition` | S/4HANA Procurement |
| `PurchaseRequisitionItem` | S/4HANA Procurement |
| `GoodsReceipt` | S/4HANA Logistics |
| `DeliveryNote` | S/4HANA Logistics |
| `DeliveryNoteItem` | S/4HANA Logistics |
| `Contract` | S/4HANA Procurement |
| `ContractItem` | S/4HANA Procurement |
| `Product` | S/4HANA MM |
| `ProductCategory` | S/4HANA MM |
| `ProductGroup` | S/4HANA MM |
| `BillOfMaterial` | S/4HANA MM |
| `BOMItem` | S/4HANA MM |
| `Plant` | S/4HANA Logistics |
| `StorageLocation` | S/4HANA Logistics |
| `MaterialDocument` | S/4HANA MM |
| `MaterialMovement` | S/4HANA MM |
| `WBSElement` | S/4HANA Project System |
| `Project` | S/4HANA Project System |
| `Network` | S/4HANA Project System |
| `NetworkActivity` | S/4HANA Project System |
| `CostCenter` | S/4HANA Controlling |
| `CostCenterGroup` | S/4HANA Controlling |
| `GLAccount` | S/4HANA Finance |
| `CompanyCode` | S/4HANA Finance |
| `Controlling` | S/4HANA Controlling |
| `ProfitCenter` | S/4HANA Controlling |
| `FunctionalArea` | S/4HANA Controlling |
| `Employee` | SuccessFactors HCM |
| `EmployeePosition` | SuccessFactors HCM |
| `Payroll` | SuccessFactors HCM |
| `PayrollDeduction` | SuccessFactors HCM |
| `PayrollEarning` | SuccessFactors HCM |
| `Leave` | SuccessFactors HCM |
| `Recruitment` | SuccessFactors HCM |
| `RecruitmentCandidate` | SuccessFactors HCM |
| `SuccessFactorsUser` | SuccessFactors Platform |
| `TimeSheet` | SuccessFactors HCM |
| `TimeSheetEntry` | SuccessFactors HCM |
| `BenefitsPlan` | SuccessFactors HCM |
| `Ariba` | SAP Ariba |
| `AribaRequisition` | SAP Ariba |
| `AribaLineItem` | SAP Ariba |
| `AribaBid` | SAP Ariba |
| `AribaBidResponse` | SAP Ariba |
| `AribaBidLineItem` | SAP Ariba |
| `ConcurExpense` | SAP Concur |
| `ConcurReport` | SAP Concur |
| `Fieldglass` | SAP Fieldglass |
| `WorkOrder` | SAP Fieldglass |
| `HCMWorker` | SuccessFactors HCM |
| `ODataService` | SAP BTP |
| `BTPService` | SAP BTP |
| `BTPBinding` | SAP BTP |
| `StandardIdentifier` | SAP Cross-Domain |

## Actual SAP API Resources

| Product | Protocol | URL |
|---|---|---|
| SAP S/4HANA Cloud | OData v2/v4, REST | https://api.sap.com/package/SAPS4HANACloud |
| SAP SuccessFactors | OData v2 | https://api.sap.com/package/SAPSuccessFactors |
| SAP Ariba | REST | https://developer.ariba.com/api |
| SAP Concur | REST | https://developer.concur.com/api-reference/ |
| SAP Fieldglass | OData | https://api.sap.com/package/FieldglassAPI |
| SAP BTP Core | REST | https://api.sap.com/package/SAPCloudPlatformCoreServices |

## References

- SAP Business Accelerator Hub: https://api.sap.com
- SAP Developer Center: https://developers.sap.com
- SAP Help Portal: https://help.sap.com
- GitHub: https://github.com/SAP
