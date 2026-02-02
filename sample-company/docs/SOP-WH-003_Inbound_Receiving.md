# SOP-WH-003: Inbound Receiving Process

| Field | Value |
|-------|-------|
| Document ID | SOP-WH-003 |
| Version | 2.4 |
| Effective Date | 2025-09-12 |
| Last Review | 2025-09-01 |
| Next Review | 2026-03-01 |
| Owner | Tom Bradley, Director Operations |
| Approver | Sarah Chen, VP Operations |
| Classification | Internal Use Only |

---

## 1. Purpose

This procedure establishes the standard process for receiving inbound freight at all Midwest Premier Logistics facilities. Proper execution ensures inventory accuracy, product integrity, and customer satisfaction.

---

## 2. Scope

This SOP applies to:
- All warehouse associates performing receiving functions
- All facilities: CLB-01, IND-02, MEM-03, CHI-04
- All inbound freight types: FTL, LTL, parcel, customer returns

---

## 3. Responsibilities

| Role | Responsibility |
|------|----------------|
| Receiving Clerk | Verify appointments, check in drivers, document discrepancies |
| Forklift Operator | Unload freight, stage in receiving area, transport to putaway |
| Receiving Supervisor | Resolve exceptions, approve adjustments, ensure compliance |
| Inventory Control | Investigate variances, process adjustments, maintain accuracy |

---

## 4. Required Equipment & Systems

- RF scanner (Zebra MC9300)
- Manhattan SCALE WMS (Receiving module)
- Pallet jack / forklift (certified operators only)
- Digital camera (for damage documentation)
- Temperature probe (for refrigerated freight)
- PPE: Safety vest, steel-toe boots, gloves

---

## 5. Procedure

### Step 1: Verify Appointment (5 min)

1.1. Check TMS (Oracle OTM) for scheduled delivery appointment
1.2. Confirm the following match the ASN (Advanced Ship Notice):
   - PO number(s)
   - Carrier name
   - Expected piece count
   - Expected weight
1.3. If no appointment exists:
   - Contact Receiving Supervisor
   - Check with customer service for authorization
   - Do NOT proceed without supervisor approval

**System:** TMS → Appointments → Search by PO or Carrier

### Step 2: Driver Check-In (5 min)

2.1. Collect from driver:
   - Bill of Lading (BOL)
   - Delivery receipt
   - Driver's license (for log)
2.2. Assign dock door in WMS
2.3. Provide driver with:
   - Door assignment slip
   - Facility safety rules acknowledgment
   - Estimated unload time
2.4. Log check-in time in TMS

**System:** WMS → Receiving → Door Assignment

### Step 3: Trailer Inspection (10 min)

3.1. Verify seal number matches BOL
   - If mismatch: STOP - notify Supervisor immediately
   - Document seal number on receiving log
3.2. Break seal and photograph (required for all shipments)
3.3. Inspect trailer condition:
   - Check for damage, water intrusion, pest evidence
   - Check load shift or fallen product
3.4. For temperature-controlled freight:
   - Record reefer temperature from unit display
   - Probe product temperature (minimum 3 locations)
   - **Requirement:** Must be ≤35°F for refrigerated, ≤0°F for frozen
   - If out of spec: STOP - contact QA and customer

**Exception Codes:**
| Code | Description | Action |
|------|-------------|--------|
| SEAL-01 | Seal missing | Supervisor approval required |
| SEAL-02 | Seal mismatch | Supervisor + customer notification |
| TEMP-01 | Temperature variance | QA hold + customer notification |
| DMG-01 | Visible damage | Photo documentation + claims process |

### Step 4: Unload and Stage (30-60 min)

4.1. Unload freight using appropriate equipment
   - Standard pallets: Forklift
   - Floor-loaded: Pallet jack + manual handling
   - Heavy/oversized: Supervisor coordination required
4.2. Stage pallets in designated receiving lanes (RECV-01 through RECV-08)
4.3. Scan each pallet/carton barcode to receiving location
4.4. Count pieces and compare to BOL
4.5. Document any discrepancies immediately:
   - Shortage: Note on BOL, driver signature required
   - Overage: Note on BOL, contact customer service
   - Damage: Photo documentation, set aside for inspection

**WMS Transaction:** Receiving → Scan to Stage → Location RECV-XX

### Step 5: Receipt Verification (15 min)

5.1. In WMS, open the ASN/PO
5.2. Enter received quantities by SKU
5.3. System will flag variances:
   - **Green:** Within tolerance (±2%)
   - **Yellow:** Outside tolerance, supervisor review
   - **Red:** Major variance, stop and investigate
5.4. For variances:
   - Recount affected SKUs
   - Check for mislabeled product
   - Document findings
   - Supervisor approval required to proceed

**Tolerance Thresholds:**
| Variance Type | Threshold | Action |
|---------------|-----------|--------|
| Quantity ±2% | Auto-accept | Proceed to putaway |
| Quantity 2-5% | Supervisor review | Recount, document, approve |
| Quantity >5% | Hold | Investigation required |
| SKU mismatch | Hold | Do not receive, contact shipper |

### Step 6: Putaway (20-40 min)

6.1. Within 4 hours of staging, initiate system-directed putaway
6.2. Scan pallet/carton
6.3. System assigns bin location based on:
   - Product velocity (ABC class)
   - Lot/FIFO requirements
   - Available capacity
6.4. Transport product to assigned location
6.5. Confirm putaway with RF scan
6.6. Verify bin label matches system

**Exceptions:**
| Product Type | Special Handling |
|--------------|------------------|
| Hazmat | Supervisor sign-off required, designated storage |
| High-value (>$1000/unit) | Cage storage, dual verification |
| Temperature-controlled | Immediate putaway, max 30 min staging |
| Oversize | Floor storage, supervisor assignment |

### Step 7: Complete Receipt (5 min)

7.1. Sign driver's delivery receipt
7.2. Return BOL copy to driver
7.3. Close receipt in WMS
7.4. File paperwork in daily receiving log
7.5. Update TMS with receipt confirmation

---

## 6. Exception Handling

### 6.1 Driver Detention
- Free time: 2 hours from check-in
- After 2 hours: Begin detention log
- Detention rate: Per carrier contract (typically $75/hour)

### 6.2 Refused Shipments
- Supervisor authorization required
- Document reason on BOL
- Contact customer service within 1 hour
- Carrier must countersign

### 6.3 Concealed Damage
- Discovered after receipt completion
- Notify Inventory Control within 24 hours
- Initiate claims process (SOP-WH-015)

---

## 7. Performance Metrics

| Metric | Target | Measurement |
|--------|--------|-------------|
| Dock-to-stock time | <4 hours | WMS timestamp |
| Receiving accuracy | 99.5% | Cycle count variance |
| Driver wait time | <90 min | TMS log |
| ASN compliance | 95% | EDI match rate |

---

## 8. Related Documents

- SOP-WH-001: Dock Door Management
- SOP-WH-002: Appointment Scheduling
- SOP-WH-004: Putaway Process
- SOP-WH-015: Freight Claims
- SOP-QA-003: Temperature Monitoring
- WI-WH-003A: RF Scanner Operation
- WI-WH-003B: Forklift Safety

---

## 9. Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 2.4 | 2025-09-12 | T. Bradley | Added temperature probe requirements |
| 2.3 | 2025-06-01 | T. Bradley | Updated exception codes |
| 2.2 | 2025-01-15 | S. Chen | Added driver detention policy |
| 2.1 | 2024-08-20 | T. Bradley | New WMS transaction codes |
| 2.0 | 2024-03-01 | S. Chen | Major revision for Manhattan SCALE |
| 1.0 | 2022-07-01 | R. Johnson | Initial release |

---

*This document is controlled. Printed copies are for reference only.*
*Current version available in SharePoint: Operations > SOPs > Warehouse*
