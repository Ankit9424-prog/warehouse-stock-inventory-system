# Quality Assurance & Test Execution Report

**System:** Warehouse Stock Inventory System  
**Test Suite:** Master Test Matrix (40 Test Cases)  
**QA Lead:** Sabrin Manandhar  

---

## 1. Test Summary

| Metric | Result |
|---|---|
| Total Executed Test Cases | 40 |
| Total Passed Cases | 30 (75%) |
| Total Failed Cases | 10 (25%) |
| User Stories Tested | 10 (WMS-01 through WMS-10) |
| Test Distribution per Story | 4 Test Cases (3 Positive / Standard, 1 Edge / Negative) |

---

## 2. Test Results by User Story

| User Story ID | Feature Under Test | Passed | Failed | Pass Rate | Defect Summary |
|---|---|---|---|---|---|
| **WMS-01** | User Authentication | 3 | 1 | 75% | Blank credential submission gives generic error instead of required field prompts |
| **WMS-02** | Stock Intake Registration | 3 | 1 | 75% | Negative item quantity input triggers unhandled server error |
| **WMS-03** | Barcode Item Scanning | 3 | 1 | 75% | Unregistered external barcode causes API timeout |
| **WMS-04** | Stock Availability Check | 3 | 1 | 75% | Discontinued items still show as available in general search |
| **WMS-05** | Low-Stock Watchlist | 3 | 1 | 75% | Duplicate SKU watchlist addition creates redundant alert rows |
| **WMS-06** | Priority Order Tagging | 3 | 1 | 75% | Inactive clerk session allows priority flag override |
| **WMS-07** | Atomic Stock Reservation | 3 | 1 | 75% | Negative reservation quantity accepted without rejection |
| **WMS-08** | Supplier Replenishment PO | 3 | 1 | 75% | Offline supplier gateway causes hanging queue instead of fallback retry |
| **WMS-09** | Dispatch Note Generation | 3 | 1 | 75% | Blank destination address generates empty shipping label |
| **WMS-10** | Immutable Audit Logging | 3 | 1 | 75% | Admin manual delete request returns 500 error instead of 403 Forbidden |

---

## 3. Spreadsheet Artifact
The complete raw testing matrix with precondition, test steps, expected result, actual result, and pass/fail indicators is available in `Testing.xlsx`.
