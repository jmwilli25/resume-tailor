# Professional Context: Jeremy Williams
*Use this document as context alongside the base resume (`Jeremy-Williams_Resume_Staff.pdf`) when generating tailored resumes or cover letters for new job applications.*

## Core Identity & Value Proposition
*   **Role:** Staff Data Engineer (Currently at Visa).
*   **Focus:** Building massive-scale, highly-governed, unstructured data foundations that power advanced analytics and downstream machine learning/modeling teams. 
*   **Key Strength:** Bridging the gap between raw, messy data and the high-quality datasets that AI/Data Science teams rely on. Jeremy builds the *infrastructure* for AI, rather than the models themselves.

## Tech Stack & Preferences
*   **Primary Processing:** Apache Spark (Scala and PySpark). Datasets are too large for standard Pandas; requires distributed processing.
*   **Ecosystem:** Databricks (Unity Catalog, Delta Tables), Apache Kafka, Apache Airflow.
*   **Language Comfort:** Highly proficient in Scala and SQL. Comfortable with Python/PySpark, but does not use Python daily for standard scripting (not highly proficient in native Python/Pandas).
*   **What to avoid:** Do not claim deep expertise in MLOps, Model Lifecycle Management, or Feature Engineering. Avoid highlighting a past 3-day hackathon involving vector DBs/Langchain unless the role specifically asks for experimental exposure to RAG.

## Deep Dive: Key Experience & Projects

### 1. Data Processing & Architecture (The Medallion Architecture)
*   **Domain:** EMVCo 3DS authentication datasets.
*   **Data Type:** ~80% of the data processed is unstructured text data.
*   **Process:** Raw data is processed through a Medallion architecture using Spark. It is made available as a minimally processed "Bronze tier" stored as Spark-generated Delta files, which are queryable through Databricks Unity Catalog. 
*   **Impact:** Ensures quality data arrives where it is expected, when it is expected, providing the foundational Parquet datasets used by downstream model teams.

### 2. Data Governance, Privacy, & Localization
*   **Localization:** Led major data localization efforts for the Kingdom of Saudi Arabia (KSA) and India.
*   **Safelist Architecture:** Implemented a strict "safelist-only" architecture. Raw unstructured data is parsed and a schema is applied to only allow approved fields through. 
*   **PII:** Personally identifiable information (PII) and personal account information are strictly masked or removed before storage.
*   **RBAC:** Manages Role-Based Access Control (RBAC) for Databricks Unity Catalog and Kibana, limiting different groups to different datasets. Defines and manages roles for ~600 users.

### 3. Automated Data Lineage & Observability
*   **Lineage Tooling:** Created an automated AI workflow (a daily prompt) that scans all GitHub repos to track changes in data flows.
*   **Output:** The flows and metadata related to each node in the graph are stored as JSON and rendered into an HTML page.
*   **Impact:** This dramatically lowers Mean Time To Resolution (MTTR) during issue investigations. The AI-generated flow JSON is also used for planning changes, writing deployment instructions, and post-testing.

### 4. Data Quality & QA
*   **Automated QA:** Built a QA task that runs downstream of every batch processing task.
*   **Metrics Tracked:** It compares source count to destination count, field population percentages, field enumeration count drift, and compares current field population to historical population (allowing for a small deviation).
*   **Impact:** Guarantees absolute reliability and catches data drift before it impacts downstream consumers.
