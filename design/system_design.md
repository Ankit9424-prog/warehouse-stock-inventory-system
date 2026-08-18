# System Architectural Design & UML Models

**System:** Warehouse Stock Inventory System  
**Design Phase:** Object-Oriented Architectural Modeling  

---

## 1. Architectural Overview
The Warehouse Stock Inventory System uses a multi-tier object-oriented architecture consisting of Presentation, Business Logic/Services, Data Access, and External Gateway layers.

---

## 2. UML Diagrams Included

### 2.1 Use Case Diagram (`usecase_diagram_expanded.png`)
Models the core business functions accessible by the primary actors:
- **Warehouse Clerk:** Authenticates, registers intake, scans barcodes, checks stock levels, and initiates dispatches.
- **Inventory Manager:** Manages low-stock watchlists, triggers supplier POs, and generates audit reports.
- **Supplier Gateway:** Receives replenishment orders and confirms shipment batches.

### 2.2 Sequence Diagram (`sequence_diagram.png`)
Illustrates the synchronous message flow for user authentication and stock request validation across five system components:
- `Warehouse Clerk` -> `LoginPage` -> `LoginController` -> `LoginService` -> `LoginRepository`
- Incorporates `alt` conditional fragments for valid session issuance versus invalid credential error prompts.

### 2.3 Activity Diagram (`activity_diagram.png`)
Models the end-to-end fulfillment process across three swimlanes:
- **Warehouse Clerk:** Review request, initiate processing, provide dispatch details, finalize shipment.
- **Inventory System:** Availability verification, atomic reservation, dispatch slip generation.
- **Supplier Gateway:** External replenishment confirmation.

### 2.4 Class Diagram (`class_diagram.png`)
Defines the core domain entities, attributes, methods, and relationship cardinalities:
- `WarehouseStaff` (Abstract Base Class)
- `WarehouseClerk` & `InventoryManager` (Inheritance)
- `StockRequest` (1) contains `RequestItem` (1..*)
- `Product` (1) maps to `InventoryItem` (1)
- `DispatchNote` (1) generates `StockTransaction` (1)
