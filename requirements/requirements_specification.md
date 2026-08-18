# Software Requirements Specification (SRS)

**System:** Warehouse Stock Inventory System  
**Document Version:** 1.0  
**Authors:** Ankit Katwal, Sabrin Manandhar, Shivam Khadka  

---

## 1. Stakeholder Analysis

| Stakeholder Group | Role & Interests | Key System Needs |
|---|---|---|
| **Warehouse Clerks** | Primary operational end-users | Fast barcode lookup, clear stock availability indicators, instant intake registration |
| **Inventory Managers** | Operational supervisors | Threshold alert watchlists, supplier PO coordination, batch priority reassignment |
| **Warehouse Auditors** | Internal and external compliance | Tamper-proof, immutable transaction logs of every stock movement |
| **External Suppliers** | B2B trading partners | Automated electronic purchase order receipts and dispatch acknowledgment |

---

## 2. Functional Requirements (FR)

- **FR-01 (Authentication):** The system shall authenticate warehouse personnel via username/email and password, enforcing role-based access control (RBAC).
- **FR-02 (Stock Intake):** The system shall record incoming stock against active purchase order IDs, supporting partial intake with automated backorder logging.
- **FR-03 (Barcode Scanning):** The system shall parse standard SKU barcodes and QR codes from handheld scanners to retrieve item data within 500ms.
- **FR-04 (Availability Check):** The system shall verify real-time stock levels and prevent checkout requests exceeding on-hand quantities.
- **FR-05 (Low-Stock Watchlist):** The system shall allow managers to flag critical SKUs and trigger automated notifications when quantities fall below set safety thresholds.
- **FR-06 (Priority Queue):** The system shall allow clerks to assign priority tags (Urgent, Standard, Low) to fulfillment orders for prioritized picking.
- **FR-07 (Atomic Reservation):** The system shall lock and reserve stock units during picking to prevent race conditions and duplicate order allocation.
- **FR-08 (Supplier Replenishment):** The system shall generate electronic replenishment Purchase Orders when safety stock levels are breached.
- **FR-09 (Dispatch Documentation):** The system shall format and print itemized dispatch packing slips upon order completion.
- **FR-10 (Audit Logging):** The system shall record every inventory change into an append-only, immutable transaction ledger.

---

## 3. Non-Functional Requirements (NFR)

- **NFR-01 (Performance):** Real-time stock lookup and barcode queries shall respond in less than 500 milliseconds under 100 concurrent requests.
- **NFR-02 (Availability):** The core inventory database service shall maintain 99.9% uptime during operational warehouse shifts.
- **NFR-03 (Security):** All user credentials shall be encrypted with Argon2/bcrypt, and API communications shall use TLS 1.3 encryption.
- **NFR-04 (Data Integrity):** Inventory updates shall comply with strict ACID transactional guarantees to prevent inventory discrepancies.
- **NFR-05 (Usability):** Handheld scanning UI interfaces shall support high-contrast visual display and minimal tap navigation for rapid warehouse floor use.
