# Reconex Executive Round — Interview Preparation Guide

**Candidate:** Jeremy Williams  
**Role:** Lead Data Engineer @ Reconex  
**Panel Interviewers:**  
* **Becky Durica** — Chief Operations Officer (COO)  
* **Chris Jones** — VP, Pricing & Carrier Relations  
* **Megan Varney** — VP, Product  

---

## 🎯 Executive Mindset Shift

In Round 1 with Anthony and Stephen, you proved your **technical depth** (Databricks, Spark, AI workflows, ground-up infrastructure). 

Round 2 with Becky, Chris, and Megan is about **business impact, product velocity, operational reliability, and cross-functional partnership**. 

> 💡 **The Golden Rule for this Round:**  
> Speak less about *how* code is written, and focus on *how reliable data drives revenue, product features, carrier trust, and operational efficiency*.

---

## 👤 Persona Breakdown & Customized Pitch Strategy

---

### 1. Becky Durica — Chief Operations Officer (COO)
* **What She Cares About:** Operational uptime, SLA compliance, risk mitigation, incident response (MTTR), cloud cost management, and building a lean, execution-focused culture.
* **Your Core Value Proposition for Becky:**
  * **Operational Reliability:** You don't just build pipelines; you build **circuit breakers** and automated QA checks that catch data anomalies *before* operational teams or customers ever see them.
  * **Proven FinOps Leadership:** You reduced AWS/Databricks cloud spend by **35% ($1.5M/year)** at Visa while maintaining Tier 2 (4-hour RTO) operational SLAs.
  * **Ground-Up Execution:** At CardinalCommerce, you built infrastructure from zero (provisioning servers, standing up Airflow & Kafka). You are a high-ownership lead who doesn't wait for resources.

#### Key Questions Becky Will Likely Ask (And How to Respond):
* **Q: "How do you ensure our customer operations aren't disrupted by data pipeline failures?"**
  * *Response Strategy:* Describe your quarantine pattern. Raw data enters Bronze; before it hits Silver/Gold, automated QA checks validate counts, schema integrity, and historical deviations. If an anomaly occurs, bad batches route to quarantine and trigger alerts, keeping operational dashboards clean while MTTR stays low.
* **Q: "How do you manage infrastructure costs as data volumes scale?"**
  * *Response Strategy:* Highlight your FinOps methodology—analyzing workload patterns, auto-scaling compute, tiering cold storage, and right-sizing clusters based on business SLAs.

#### Strategic Questions to Ask Becky:
1. *"From an operations standpoint, what are the biggest data visibility or reliability bottlenecks currently slowing down the team?"*
2. *"How do you measure success for the data platform team over the next 12 months in terms of operational efficiency and SLA compliance?"*

---

### 2. Chris Jones — VP, Pricing & Carrier Relations
* **What He Cares About:** Carrier performance scoring (`TrueMark™`), rate card & contract accuracy, automated freight auditing (EDI 210 invoice reconciliation), margin protection, and `Smart Select™` LTL routing efficiency.
* **Your Core Value Proposition for Chris:**
  * **Financial & Audit Accuracy:** Coming from Visa/CardinalCommerce, your career has been built on zero-data-loss financial event processing and strict schema enforcement.
  * **Carrier Data Integrity:** You understand that `TrueMark™` scorecards and `Smart Select™` LTL carrier recommendations depend on 100% verifiable data. If carrier status updates (EDI 214) or rate tables are inaccurate, carrier relationships and margins suffer.
  * **Rate Engine Governance:** Experience implementing strict safelist architectures and role-based governance to ensure rate tariffs and carrier contract data remain accurate and protected.

#### Key Questions Chris Will Likely Ask (And How to Respond):
* **Q: "How do you handle complex, messy data from hundreds of external carriers?"**
  * *Response Strategy:* Emphasize schema-enforced streaming and ingestion buffers (Kafka/Delta Bronze). External carrier formats vary widely; by enforcing strict validation and schema parsing at the boundary, downstream rate engines and carrier scorecards always consume standardized, trustworthy data.
* **Q: "How do you ensure rate auditing and pricing pipelines deliver zero errors?"**
  * *Response Strategy:* Connect this directly to your fintech payment settlement background at Visa. Financial reconciliation pipelines require automated reconciliation checks (comparing source tenders to final carrier invoices) to catch rate discrepancies instantly.

#### Strategic Questions to Ask Chris:
1. *"When carrier invoices (EDI 210) or shipment status updates (EDI 214) come in from carrier partners, what is the biggest data quality or pricing discrepancy headache your team faces today?"*
2. *"As Reconex expands carrier relationships, how can the data platform better support dynamic pricing models and `Smart Select™` routing decisions?"*

---

### 3. Megan Varney — VP, Product
* **What She Cares About:** Product feature velocity, customer dashboard responsiveness (`tmsConnect™`), data freshness, turning raw freight data into customer-facing value, self-service analytics for product teams, and AI-forward product innovation.
* **Your Core Value Proposition for Megan:**
  * **Product Partner & Enabler:** You view the data platform as the foundation for product features. You partner directly with product leadership to turn raw streams into high-performance Gold Delta tables that power customer dashboards.
  * **Data Democratization Leader:** At Visa, you didn't just build backend pipelines—you personally led **40+ training sessions** for Kibana and Databricks, empowering product and business teams to perform self-service analytics without filing engineering tickets.
  * **AI-Forward Velocity:** You leverage **Claude Code** to accelerate development, refactor code, and ship features faster, giving product teams shorter feedback loops.

#### Key Questions Megan Will Likely Ask (And How to Respond):
* **Q: "How do you collaborate with Product to deliver new data features quickly?"**
  * *Response Strategy:* Explain your agile, contract-first approach. You work with Product to define the Gold table schema and data requirements upfront, use Claude Code to accelerate pipeline development, and deliver clean, pre-aggregated datasets so UI/BI engineers can build customer-facing dashboards without waiting on complex backend refactoring.
* **Q: "How do you make data accessible to product managers and analysts?"**
  * *Response Strategy:* Highlight your experience establishing self-service analytics, Databricks Unity Catalog governance, and conducting hands-on training sessions so product teams can explore data independently and safely.

#### Strategic Questions to Ask Megan:
1. *"What is the product vision for `tmsConnect™` and `TrueMark™` over the next year, and what new data capabilities or analytics features are customers asking for most?"*
2. *"How do the product and data engineering teams currently collaborate when scoping new analytics features—is there a clear contract for Gold table schemas?"*

---

## 🏆 4 High-Impact STAR Stories (Tailored for Executives)

---

### Story 1: Safeguarding Customer Trust (Data Quality & Observability)
* **Context for Executives:** Focus on customer impact and brand reputation.
* **Narrative:** "At Visa, we processed unstructured payment authentication datasets where bad data could break downstream modeling and customer reports. I built automated post-processing QA tasks that compared field counts, population percentages, and statistical drift against historical baselines. If an anomaly occurred, the pipeline quarantined the data before it reached customer-facing tables. This approach protected customer trust and eliminated silent data corruption."

### Story 2: Driving Business Cost Efficiency (FinOps)
* **Context for Executives:** Focus on bottom-line impact.
* **Narrative:** "I led an enterprise FinOps initiative at Visa that reduced cloud infrastructure spend by 35%, saving $1.5M annually. Instead of just cutting resources, I analyzed workload execution patterns, right-sized compute clusters, tiered storage, and streamlined redundancy while strictly exceeding our Tier 2 4-hour RTO SLAs. I bring this same cost-conscious mindset to managing Reconex's Databricks platform as data volume grows."

### Story 3: Democratizing Data for Cross-Functional Teams
* **Context for Executives:** Focus on team empowerment and self-service culture.
* **Narrative:** "Engineering bottlenecks happen when product and ops teams have to file tickets for basic data answers. At Visa, I managed RBAC across Unity Catalog and Kibana for ~600 users, and personally conducted over 40 hands-on training sessions. Teaching product managers and analysts how to query data safely freed up engineering capacity while accelerating product decision-making."

### Story 4: Ground-Up Execution & Lean Team Ownership
* **Context for Executives:** Focus on agility and self-sufficiency.
* **Narrative:** "When I joined CardinalCommerce, my manager and I built our data infrastructure from scratch. I provisioned AWS servers, installed and configured Airflow, and stood up Kafka clusters from zero. I thrive in high-ownership environments where I am responsible for building, operating, and scaling the data platform end-to-end."

---

## 💬 Conversational Bridges for the Executive Panel

Remember your **secret weapon** from Round 1: end your answers with a conversational bridge question!

1. **To Becky (Operations):**  
   > *"...that kept our MTTR low and prevented bad data from reaching customer dashboards. **How is the operations team currently notified when a carrier data stream experiences a delay or outage?**"*

2. **To Chris (Pricing & Carrier Relations):**  
   > *"...which guaranteed zero data loss for financial clearing pipelines. **When carrier rate tariffs or invoice line-items have discrepancies, how much of that audit process is automated today versus manual review?**"*

3. **To Megan (Product):**  
   > *"...which allowed product managers to run their own queries without waiting on engineering sprint tickets. **What is the biggest data bottleneck product managers face today when trying to validate a new dashboard concept?**"*

---

## 📋 Pre-Interview Executive Checklist

- [ ] **Research Interviewers on LinkedIn:**
  * **Becky Durica:** Look up her career background at Reconex and previous operations/logistics roles.
  * **Chris Jones:** Note his experience in carrier relations, LTL pricing, and freight negotiations.
  * **Megan Varney:** Note her product leadership background and previous software/logistics products.
- [ ] **Review Reconex Product Suite One-Pager:** Re-read [`Reconex_Product_Suite_One_Pager.md`](file:///home/jeremy/genai/antigravity/applications/reconex/lead-data-engineer/Reconex_Product_Suite_One_Pager.md) (`tmsConnect™`, `TrueMark™`, `Smart Select™`).
- [ ] **Prepare Hard Copies of Base Resume:** Have printed copies of [`Jeremy-Williams_Resume_Staff.pdf`](file:///home/jeremy/genai/antigravity/base/Jeremy-Williams_Resume_Staff.pdf) on hand.
- [ ] **Post-Interview Follow-Up:** Plan to send personalized thank-you notes to Becky, Chris, and Megan (via email or through Liz).
