# 🚚 Reconex — Company & Logistics Product Suite One-Pager

**Company Name:** Reconex (Recon Logistics LLC)  
**Headquarters:** Solon, OH (31200 Carter Street)  
**Website:** [reconex.io](https://reconex.io)  
**Core Mission:** Providing data-driven "Freight Intelligence" and web-based Transportation Management System (TMS) software to give mid-market shippers total control, cost transparency, and automated execution over their shipping operations.

---

## 📦 Reconex Logistics Product Suite

Reconex builds proprietary software products that transform raw freight and carrier data into actionable shipping intelligence.

### 1. **tmsConnect™ (Cloud Transportation Management System)**
* **What It Is:** Reconex’s centralized web portal and control panel for mid-market shippers.
* **Core Capabilities:** Single-pane-of-glass interface for load creation, carrier dispatch, real-time shipment tracking, compliance, and document management.
* **Data Engineer Relevance:** Operates on live transaction event streams (shipment tenders, status updates, carrier receipts).

### 2. **TrueMark™ (Proprietary Freight Intelligence & Benchmarking)**
* **What It Is:** The flagship analytics engine powering Reconex's freight intelligence value proposition.
* **Core Capabilities:** 
  * Captures **move-by-move carrier performance data** independently (missed pickups, transit delays, damage/shortages, service failures) backed by delivery receipts.
  * Provides independent carrier benchmarking, cost transparency, and service compliance scorecards.
  * Audits carrier invoices (matching contracted rates against actual billed amounts) to detect overcharges.
* **Data Engineer Relevance:** **This is the exact product powered by the Databricks Lakehouse.** Raw EDI streams and invoice logs are transformed in Delta Lake into Gold tables feeding TrueMark™ analytics dashboards.

### 3. **Smart Select™ (Intelligent LTL Carrier Routing Engine)**
* **What It Is:** A dynamic carrier selection module embedded within tmsConnect™.
* **Core Capabilities:** 
  * Optimizes Less-Than-Truckload (LTL) and full truckload carrier selection during load tendering.
  * Algorithmically balances three key variables: **Cost (Contracted Tariffs)**, **Transit Speed**, and **TrueMark™ Carrier Performance Scorecards**.
* **Data Engineer Relevance:** Requires low-latency, accurate carrier scorecard data from the Lakehouse to drive real-time routing decisions.

### 4. **Freight Audit & Rate Engine**
* **What It Is:** Automated billing reconciliation engine.
* **Core Capabilities:** Ingests carrier invoices (EDI 210), parses line-item accessorial fees (fuel surcharges, detention, liftgate fees), and validates them against master contract rate tables.
* **Data Engineer Relevance:** Requires zero-data-loss financial reconciliation pipelines—structurally identical to Visa transaction clearing pipelines!

---

## 🔄 Freight Data Lifecycle: Raw Events ➔ Databricks Lakehouse ➔ Product Output

To speak like an insider in your interview, keep this data flow in mind:

```
[ Freight Event Sources ]                     [ Databricks Lakehouse ]                    [ Customer Products ]
-------------------------                     ------------------------                    -------------------
• EDI 204 (Load Tender)          ───►          • Bronze: Raw Ingestion Streams  ───►       • tmsConnect™ Dashboards
• EDI 214 (Shipment Status)      ───►          • Silver: Cleaned, Deduplicated  ───►       • TrueMark™ Benchmarks
• EDI 210 (Carrier Invoice)      ───►            & Quarantined Data               ───►       • Smart Select™ Engine
• Carrier API Webhooks           ───►          • Gold: Carrier Scorecards         ───►       • Executive BI Reports
                                                 & Audited Rate Tables
```

---

## 🎯 How Your Lead Data Engineer Role Connects to the Product Suite

When Anthony and Steven ask about your vision for the platform, you can connect your experience directly to their products:

1. **Powering TrueMark™ Scorecards:**  
   *"The data quality quarantine pattern I built for Medallion architecture directly protects products like TrueMark™. If an EDI 214 status update comes in corrupted or out of sequence, filtering it in Silver guarantees carrier scorecards are built on 100% verifiable data."*

2. **Fueling Smart Select™ Routing:**  
   *"Smart Select™ depends on fresh, accurate carrier performance metrics. Optimizing Delta Lake Z-Ordering and cluster job performance ensures carrier rating tables refresh quickly and reliably."*

3. **Reconciling Invoices (Freight Audit):**  
   *"Auditing carrier invoices (EDI 210) against rate tariffs requires zero data loss and strict schema enforcement—the exact type of high-integrity processing I managed for financial clearing systems at Visa."*

---

## 🗣️ Killer Questions to Ask Anthony & Steven About Their Product Suite

1. *"How closely does the Lakehouse team work with the product engineers building **TrueMark™** and **Smart Select™**? Are scorecards served directly from Databricks Gold tables or pushed to an operational data store?"*
2. *"What does your current EDI ingestion pipeline look like for **EDI 214 tracking** and **EDI 210 invoicing**—is it streaming into Delta Lake via Structured Streaming/Kafka or micro-batch Databricks Workflows?"*
