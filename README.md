# Warehouse Stock Inventory System (WMS)
**Course:** CSE 220: Principles of Software Engineering  
---

## Engineering Team & Roles
* **Ankit Katwal** — Team Lead & Lead Software Architect (Product Owner)
* **Sabrin Manandhar** — Scrum Master & Senior QA Lead (Quality Assurance Specialist)
* **Shivam Khadka** — DevOps Lead & Senior Systems Engineer (Configuration Manager)

---

## Project Overview & Scope
The **Warehouse Stock Inventory System** is an enterprise-grade software engineering project simulating the complete software development lifecycle without raw source-code compilation. The system modernizes manual warehouse logistics through automated intake registration, handheld barcode scanning, real-time availability checking, low-stock threshold alerting, priority order queueing, atomic stock reservation, automated supplier replenishment, itemized dispatch packing slip generation, and immutable transaction audit logging.

---

## 8-Week Agile Sprint Schedule (July 1 – August 25, 2026)
The project was executed across an exact **8-week lifecycle (56 calendar days)** structured into four 2-week sprints:
1. **Sprint 1 (Foundations):** Weeks 1–2 (July 1 – July 14, 2026) — User Authentication (`WMS-01`), Stock Intake (`WMS-02`), Barcode Scanning (`WMS-03`), Stock Availability (`WMS-04`). Total = 13 Story Points.
2. **Sprint 2 (Inventory Control):** Weeks 3–4 (July 15 – July 28, 2026) — Low-Stock Watchlist (`WMS-05`), Urgent Priority Tagging (`WMS-06`), Atomic Stock Reservation (`WMS-07`). Total = 10 Story Points.
3. **Sprint 3 (Logistics & POs):** Weeks 5–6 (July 29 – August 11, 2026) — Supplier Replenishment PO Transmission (`WMS-08`), Dispatch Slip Generation (`WMS-09`), Immutable Audit Ledger (`WMS-10`). Total = 11 Story Points.
4. **Sprint 4 (QA & Final Deployment):** Weeks 7–8 (August 12 – August 25, 2026) — Master 40-Case Test Matrix Execution, Git Branch Merging, APA 7th Documentation Finalization, and Final Release Sign-Off.

---

## Repository Directory Structure
```text
warehouse-stock-inventory-system/
├── requirements/
│   ├── functional_requirements.md        # FR-01 to FR-10 specifications
│   ├── non_functional_requirements.md    # NFR-01 to NFR-05 specifications
│   ├── stakeholder_matrix.md             # Stakeholder roles, influence, and engagement
│   └── user_stories.md                   # WMS-01 to WMS-10 user stories & acceptance criteria
├── design/
│   ├── usecase_diagram_expanded.png      # UML Expanded Use Case Diagram (3 Actors)
│   ├── sequence_diagram.png              # UML Sequence Diagram (Authentication & Session)
│   ├── activity_diagram.png              # UML Activity Diagram (Outbound Stock Fulfillment)
│   └── class_diagram.png                 # UML Class Diagram (Domain Entities & Multiplicities)
├── testing/
│   ├── Testing.xlsx                      # Master 40-Case QA Test Matrix Spreadsheet
│   └── defect_log.md                     # Root-cause analysis of 10 failed design test cases
├── project_management/
│   ├── Planning_WMS.xlsx                 # 8-Week Agile Sprint Schedule with Excel Gantt Chart
│   ├── gantt_chart.png                   # High-Resolution 300 DPI Project Delivery Gantt Chart
│   └── trello_sprint_board.png           # Trello Kanban Sprint Board Snapshot
└── README.md                             # Project overview and repository guide
```

---

## Testing & Quality Assurance Summary
* **Total Test Cases Evaluated:** 40 Test Cases across 10 User Stories (4 per story).
* **Testing Levels Covered:** Unit Testing, Integration Testing, System Testing, and User Acceptance Testing (UAT).
* **Passed Cases:** 30 Cases (75% Pass Rate).
* **Failed Cases:** 10 Cases (25% Defect Rate).
* **Defect Classifications:** Input validation defects, boundary negative quantity faults, external service timeout handling, lifecycle state constraints, entity duplicate insertions, workflow state-machine violations, concurrency bin locking faults, business rule validations, hardware fault tolerance, and audit immutability constraints.
* **Master Test Spreadsheet:** `testing/Testing.xlsx` and live Google Drive matrix link.

---

## Deliverables & Version Control Policy
* **Branching Strategy:** Feature-branch workflow (`feature/wms-01-auth`, `feature/wms-02-stock-intake`, etc.).
* **Pull Request Policy:** Peer code/document review required prior to merging into `main`.
* **Documentation Standard:** APA 7th Edition Student Paper Format.
