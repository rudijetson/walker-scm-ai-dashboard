# Midwest Premier Logistics - Sample Data Package

## Overview

This package contains realistic sample data representing a mid-sized 3PL (third-party logistics) company operating in the Midwest United States. The data is designed for:

- AI/ML training and demonstration
- Process mapping and workflow design
- Systems integration planning
- Logistics education and training

---

## Company Profile

**Midwest Premier Logistics, LLC**
- Founded: 1987
- HQ: Columbus, OH
- Revenue: $89M annually
- Employees: 342
- Fleet: 124 tractors, 310 trailers
- Facilities: 4 (Columbus, Indianapolis, Memphis, Joliet)

---

## Data Files

### Core Operational Data (`/data/`)

| File | Records | Description |
|------|---------|-------------|
| `tms_shipments.csv` | 20 | Transportation Management System shipment records |
| `wms_inventory.csv` | 30 | Warehouse Management System inventory positions |
| `lane_rates.csv` | 25 | Contract and spot rates by lane |
| `cycle_counts.csv` | 25 | Inventory audit/cycle count records |
| `carriers.csv` | 12 | Carrier master data with performance metrics |
| `dispatch_queue.csv` | 14 | Active dispatch/load board |
| `customers.csv` | 10 | Customer master data |
| `rate_shopping.csv` | 18 | Rate comparison/shopping records |

### Documentation (`/docs/`)

| File | Description |
|------|-------------|
| `rfp_tracker.md` | Active and closed RFP tracking |
| `SOP-WH-003_Inbound_Receiving.md` | Standard Operating Procedure example |
| `value_stream_map.md` | Order-to-delivery process map with Mermaid diagrams |

---

## Data Relationships

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│  Customers  │────▶│  Shipments  │────▶│  Dispatch   │
└─────────────┘     └─────────────┘     └─────────────┘
                           │                   │
                           ▼                   ▼
                    ┌─────────────┐     ┌─────────────┐
                    │ Lane Rates  │     │  Carriers   │
                    └─────────────┘     └─────────────┘
                           │
                           ▼
                    ┌─────────────┐
                    │Rate Shopping│
                    └─────────────┘

┌─────────────┐     ┌─────────────┐
│  Inventory  │────▶│Cycle Counts │
└─────────────┘     └─────────────┘
```

---

## Key Fields Reference

### Shipment Statuses
| Status | Description |
|--------|-------------|
| Pending | Order received, not yet planned |
| Open | Ready for carrier assignment |
| Tendered | Sent to carrier, awaiting acceptance |
| Confirmed | Carrier accepted |
| Picked Up | Freight collected from origin |
| In Transit | En route to destination |
| Delivered | Completed |

### Carrier Preferred Status
| Status | Description |
|--------|-------------|
| Gold | Strategic partner, prioritize |
| Silver | Preferred, standard rates |
| Standard | Approved, backup capacity |

### Inventory ABC Classification
| Class | Velocity | Typical Location |
|-------|----------|------------------|
| A | High (top 20%) | Prime pick locations |
| B | Medium (next 30%) | Secondary locations |
| C | Low (bottom 50%) | Bulk/overflow storage |

---

## System Mapping

| Data File | Source System | Integration |
|-----------|---------------|-------------|
| tms_shipments.csv | Oracle OTM | EDI 204/214 |
| wms_inventory.csv | Manhattan SCALE | Real-time API |
| lane_rates.csv | Oracle OTM + DB2 | Manual + Query |
| cycle_counts.csv | Manhattan SCALE | Batch export |
| carriers.csv | Oracle OTM | Master data sync |
| dispatch_queue.csv | Oracle OTM | Real-time |
| customers.csv | SAP S/4HANA | Daily sync |
| rate_shopping.csv | Oracle OTM | Transaction log |

---

## AI/ML Use Cases

### Demonstrated in This Data

1. **Rate Prediction**
   - Input: `lane_rates.csv`, `rate_shopping.csv`
   - Goal: Predict optimal carrier/rate for new shipments

2. **Inventory Accuracy**
   - Input: `wms_inventory.csv`, `cycle_counts.csv`
   - Goal: Predict variance, prioritize counts

3. **Carrier Performance**
   - Input: `carriers.csv`, `tms_shipments.csv`
   - Goal: Score/rank carriers, predict acceptance

4. **Exception Detection**
   - Input: `dispatch_queue.csv`, `tms_shipments.csv`
   - Goal: Flag at-risk shipments before delay

5. **Process Optimization**
   - Input: `value_stream_map.md`, SOPs
   - Goal: Identify bottlenecks, suggest improvements

---

## Sample Queries

### Find shipments at risk of delay
```sql
SELECT shipment_id, customer_name, dest_city, delivery_date, status
FROM tms_shipments
WHERE status IN ('Tendered', 'Pending')
  AND pickup_date <= CURRENT_DATE;
```

### Carrier performance ranking
```sql
SELECT carrier_name, on_time_delivery_pct, tender_acceptance_pct, 
       claims_rate_pct, preferred_status
FROM carriers
ORDER BY on_time_delivery_pct DESC;
```

### Inventory with high variance
```sql
SELECT sku, description, system_qty, actual_qty, variance_pct, variance_value
FROM cycle_counts
WHERE ABS(variance_pct) > 0.5
ORDER BY ABS(variance_value) DESC;
```

---

## Glossary

| Term | Definition |
|------|------------|
| **ASN** | Advanced Ship Notice - electronic notification of incoming shipment |
| **BOL** | Bill of Lading - shipping document/contract |
| **Cross-dock** | Facility where freight is transferred between trucks without storage |
| **EDI** | Electronic Data Interchange - standard B2B messaging |
| **FTL** | Full Truckload - shipment using entire trailer |
| **Lane** | Defined freight route (origin → destination) |
| **LTL** | Less Than Truckload - consolidated shipments |
| **PRO** | Progressive/Tracking number assigned by carrier |
| **Reefer** | Refrigerated trailer |
| **TMS** | Transportation Management System |
| **WMS** | Warehouse Management System |

---

## Notes

- All data is fictional and for demonstration purposes only
- Company names, addresses, and contact information are fabricated
- Financial figures are representative of industry norms
- Dates are set around January 2026 for consistency

---

*Created: January 2026*
*Version: 1.0*
