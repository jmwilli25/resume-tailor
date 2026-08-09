# Jeremy Williams
www.linkedin.com/in/jeremy-williams-9341a2a
4967 Mayfield Rd, Lyndhurst, OH 44124 | Tel: 330-418-4336 | Email: jmwilli25@gmail.com

## Summary
Staff Data Engineer with 10+ years of experience designing and implementing highly scalable data infrastructure that provides the highly-governed, unstructured data foundations that make advanced analytics and modeling possible. Expertise in processing massive unstructured datasets through medallion architectures, ensuring uncompromising data quality, governance, and availability for downstream data science teams. Adept at leveraging Apache Spark (Scala/PySpark) and Databricks to build robust data pipelines, with a proven track record of architecting global data localization strategies, optimizing cloud FinOps, and automating data workflows to lower MTTR.

## Skills and Technology
* **Large-Scale Data Processing:** Apache Spark (Scala/PySpark), Apache Kafka, Apache Airflow, Unstructured Data Processing, Data Quality Monitoring
* **Databricks Ecosystem:** Databricks Unity Catalog, Delta Tables, Medallion Architecture
* **Programming Languages:** Python, Scala, SQL, Java
* **Cloud & Infrastructure:** Amazon Web Services (S3, EC2, Lambda, SNS, SQS), Linux (Ubuntu, Redhat)
* **Data Governance & Security:** PII Masking, RBAC, Schema Enforcement, Data Localization
* **Databases:** Elasticsearch, Hive, InfluxDB, MySQL, MS SQL
* **Development & CI/CD:** GitHub, Jenkins, AI-Assisted Dev (Claude Code), Automated Lineage Generation

## Experience

### Staff Data Engineer – Visa Inc. 
*Mar 2020 – Present*

* Drive the architectural vision for large-scale data infrastructure, engineering scalable Spark and PySpark pipelines to process massive volumes of unstructured text data (80% of workload) to provide foundational Parquet datasets for downstream modeling and advanced analytics teams.
* Architect and maintain a robust Medallion data architecture, transforming raw unstructured data into structured, high-quality Bronze-tier Delta tables accessible via Databricks Unity Catalog.
* Implement advanced data quality monitoring pipelines downstream of processing jobs to automatically track source-to-destination counts, field population drift, and historical deviations, ensuring highly reliable datasets for downstream model consumption.
* Mentor a team of 6 data engineers in advanced development practices, spearheading an agentic coding initiative that integrated Jira with Claude Code to autonomously resolve tickets and generate GitHub PRs.
* Organize and lead 40+ small-group technology training sessions for Kibana and Databricks, democratizing data access for cross-functional teams.

**Key Initiatives & Enterprise Impact:**
* **Enterprise Data Governance & Privacy:** Engineered a strict "safelist-only" architecture for parsing unstructured data, applying robust schemas to mask and remove PII before storage. Administer Role-Based Access Control (RBAC) via Databricks Unity Catalog and Kibana for over 600 users.
* **Automated Data Lineage & Observability:** Developed an automated workflow leveraging AI prompts to scan GitHub repositories daily to track data flow changes, rendering dynamic JSON-to-HTML lineage graphs. This significantly lowered Mean Time To Resolution (MTTR) during investigations and enhanced deployment planning.
* **Enterprise Hub-and-Spoke Architecture:** Architected and deployed a massive-scale (10 billion daily records / 2TB) Kafka and MirrorMaker ecosystem to consolidate decentralized streams, ensuring quality data arrives reliably for hundreds of cross-functional users and downstream model teams.
* **Global Data Localization (KSA & India):** Owned the technical execution of high-stakes data localization mandates for Saudi Arabia and India, designing isolated regional spoke clusters that ensured strict regulatory compliance while maintaining global data integrity.
* **Pipeline Automation:** Accelerated the rollout of international datacenter pipelines by integrating AI-assisted development (Claude Code) to automatically generate and deploy bronze-level processing code from standardized templates.
* **Enterprise FinOps & Cloud Cost Optimization:** Spearheaded a cost-reduction initiative that decreased AWS and Databricks spend by 35% (saving $1.5M annually) by purging unused datasets, right-sizing Spark clusters, and implementing S3 storage tiering.

### Sr. Data Engineer / Data Engineer – CardinalCommerce, A Visa Solution 
*Jan 2016 – Mar 2020*

* Architected and developed a Kafka and Spark application log streaming pipeline from proof-of-concept to production in under 3 months.
* Planned and deployed a multi-node Apache Airflow cluster, driving a 300% improvement in parallel task execution.
* Engineered and optimized scalable Spark batch and streaming data processing pipelines using Scala, PySpark, and SQL.
* Maintained strict documentation for naming conventions, schema enforcement, deployment, and data pipeline flows.
* Administered and scaled Airflow, Elasticsearch, InfluxDB, and Kafka clusters.

**Key Initiatives & Enterprise Impact:**
* **Schema-Enforced Streaming:** Pioneered an early iteration of a schema-enforced hub-and-spoke data streaming model using Kafka, Spark, and custom connectors, drastically improving system flexibility and data quality for downstream analytics while reducing mean time to display.
* **Unified Observability:** Centralized application and server metric data for unified dashboarding and alerting using Telegraf, InfluxDB, Kapacitor, and Grafana, giving engineers a single pane of glass view of system and application health.

## Awards
* **Recipient:** 2022 CardinalCommerce Technology and Innovation award

## Education
* **B.Sc. Physics:** Kent State University, Kent, OH – May 2009
