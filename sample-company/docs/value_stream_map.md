# Value Stream Map: Order-to-Delivery Process
## Midwest Premier Logistics

```mermaid
flowchart TB
    subgraph Customer["CUSTOMER"]
        CO[Customer Order<br/>via EDI/Portal/Email]
    end

    subgraph OrderMgmt["ORDER MANAGEMENT"]
        OM1[Order Receipt<br/>⏱️ 5 min]
        OM2[Order Validation<br/>⏱️ 15 min]
        OM3[Inventory Check<br/>⏱️ 10 min]
        OM4[Order Confirmation<br/>⏱️ 5 min]
    end

    subgraph Planning["TRANSPORTATION PLANNING"]
        TP1[Load Building<br/>⏱️ 20 min]
        TP2[Rate Shopping<br/>⏱️ 45 min ⚠️]
        TP3[Carrier Selection<br/>⏱️ 15 min]
        TP4[Tender to Carrier<br/>⏱️ 10 min]
        TP5[Carrier Acceptance<br/>⏱️ 2-4 hrs ⚠️]
    end

    subgraph Warehouse["WAREHOUSE OPERATIONS"]
        WH1[Pick Wave Release<br/>⏱️ 5 min]
        WH2[Order Picking<br/>⏱️ 45 min]
        WH3[Packing/Staging<br/>⏱️ 30 min]
        WH4[Load Trailer<br/>⏱️ 45 min]
        WH5[BOL Generation<br/>⏱️ 10 min]
    end

    subgraph Execution["TRANSPORTATION EXECUTION"]
        TE1[Driver Check-in<br/>⏱️ 15 min]
        TE2[Trailer Inspection<br/>⏱️ 10 min]
        TE3[Departure Scan<br/>⏱️ 5 min]
        TE4[In-Transit Tracking<br/>⏱️ Continuous]
        TE5[Delivery Confirmation<br/>⏱️ 15 min]
    end

    subgraph Systems["SYSTEMS INVOLVED"]
        S1[(SAP ERP)]
        S2[(Manhattan WMS)]
        S3[(Oracle TMS)]
        S4[(FourKites)]
        S5[(IBM DB2)]
    end

    CO --> OM1
    OM1 --> OM2
    OM2 --> OM3
    OM3 --> OM4
    OM4 --> TP1
    TP1 --> TP2
    TP2 --> TP3
    TP3 --> TP4
    TP4 --> TP5
    TP5 --> WH1
    WH1 --> WH2
    WH2 --> WH3
    WH3 --> WH4
    WH4 --> WH5
    WH5 --> TE1
    TE1 --> TE2
    TE2 --> TE3
    TE3 --> TE4
    TE4 --> TE5

    OM1 -.-> S1
    OM3 -.-> S2
    TP2 -.-> S3
    TP2 -.-> S5
    WH2 -.-> S2
    TE4 -.-> S4
```

---

## Process Metrics Summary

| Phase | Steps | Total Time | Value-Add Time | Wait Time | Systems |
|-------|-------|------------|----------------|-----------|---------|
| Order Management | 4 | 35 min | 30 min | 5 min | SAP, WMS |
| Transportation Planning | 5 | 3-5 hrs | 1.5 hrs | 2-4 hrs | TMS, DB2 |
| Warehouse Operations | 5 | 2.25 hrs | 2 hrs | 15 min | WMS |
| Transportation Execution | 5 | Variable | 45 min | N/A | TMS, FourKites |

**Total Lead Time:** 6-8 hours (same-day) to 24+ hours (standard)

---

## Pain Points Identified (⚠️)

### 1. Rate Shopping (45 min)
- **Current State:** Manual process across multiple carrier portals
- **Root Cause:** No API integration, spreadsheet-based comparison
- **Impact:** Delays load confirmation, reduces carrier options
- **AI Opportunity:** Automated rate aggregation and recommendation

### 2. Carrier Acceptance (2-4 hrs)
- **Current State:** Email/phone back-and-forth
- **Root Cause:** Carriers check capacity manually, no real-time visibility
- **Impact:** Uncertainty in pickup scheduling, warehouse staging delays
- **AI Opportunity:** Predictive acceptance scoring, auto-escalation

### 3. Data Silos
- **Current State:** 5 systems with limited integration
- **Root Cause:** Legacy architecture, point-to-point interfaces
- **Impact:** Manual data entry, reconciliation errors
- **AI Opportunity:** Unified data layer, exception detection

---

## Handoff Points (Integration Gaps)

```mermaid
flowchart LR
    SAP[SAP ERP] -->|Manual Export| TMS[Oracle TMS]
    TMS -->|EDI 204| Carrier[Carrier Systems]
    SAP -->|Scheduled Batch| WMS[Manhattan WMS]
    WMS -->|API| TMS
    TMS -->|API| FourKites[FourKites]
    WMS -.->|Query| DB2[(IBM DB2)]
    TMS -.->|Query| DB2

    style SAP fill:#e1f5fe
    style TMS fill:#e8f5e9
    style WMS fill:#fff3e0
    style FourKites fill:#f3e5f5
    style DB2 fill:#ffebee
```

| From | To | Integration Type | Frequency | Reliability |
|------|-----|-----------------|-----------|-------------|
| SAP → TMS | Manual CSV | Daily | 95% |
| SAP → WMS | Batch API | Hourly | 98% |
| WMS → TMS | Real-time API | Event-driven | 99% |
| TMS → Carrier | EDI 204/990 | Real-time | 97% |
| TMS → FourKites | API | Real-time | 99% |
| WMS → DB2 | Query | On-demand | 99% |

---

## AI Workflow Opportunities

### Quick Wins (0-3 months)
1. **Rate Shopping Automation**
   - Input: Lane, weight, equipment, date
   - Output: Ranked carrier options with confidence scores
   - Savings: 30 min/load × 50 loads/day = 25 hrs/day

2. **Exception Alerting**
   - Monitor: Delivery appointments, carrier acceptance, temp readings
   - Alert: Proactive notification with recommended actions
   - Impact: Reduce reactive fire-fighting by 40%

### Medium-Term (3-6 months)
3. **SOP Digitization**
   - Convert 40+ SOPs to structured workflows
   - Enable AI-assisted training and compliance checking
   - Reduce onboarding time by 50%

4. **Demand Forecasting Integration**
   - Combine historical data with customer forecasts
   - Pre-position inventory, pre-book carrier capacity
   - Improve on-time delivery by 3-5%

### Long-Term (6-12 months)
5. **Autonomous Planning**
   - AI builds loads, selects carriers, tenders shipments
   - Human approval for exceptions only
   - Target: 80% touchless load execution

---

*Document Owner: Sarah Chen, VP Operations*
*Last Updated: 2026-01-15*
*Version: 1.2*
