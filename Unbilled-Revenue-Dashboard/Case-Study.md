# Case Study: Automated Unbilled Revenue Analytics Pipeline
**Technology:** Power BI | Power Automate | SharePoint | Excel

## 📑 Overview
This analytics suite provides a macro-level view of the organization’s unbilled revenue, categorized by contract, status, and financial impact. It transforms a labor-intensive manual reporting process into a fully automated data pipeline.

## ⚙️ The Automation Pipeline (ETL Logic)
The system eliminates the manual "daily report hunt" through a chained automation sequence:
1. **Intake Trigger:** A Power Automate flow monitors the shared billing inbox for three specific daily reports.
2. **Automated Overwrite:** Upon receipt, the flow extracts the attachments and overwrites the existing master files in a secured SharePoint directory, maintaining a consistent file path for the BI service.
3. **Scheduled Refresh:** The Power BI Semantic Model is configured for a scheduled refresh following the file update, ensuring that management has an "at-a-glance" view of the current revenue state without manual intervention.

## 🗄️ Relational Data Modeling
To create a cohesive reporting system, the semantic model employs complex relational mapping:
* **Primary Key Synchronization:** Multiple disparate reports are linked via Work Order ID, allowing for cross-report data fusion.
* **Data Enrichment:** The model automatically populates contract details, aging thresholds, and status flags, ensuring that every Work Order is viewed through the correct financial lens.

## 🔍 Analytical Capabilities
* **Executive Summary:** High-level visualization of Unbilled Revenue by Contract and Status.
* **Drill-Through Reporting:** Users can right-click any data point to "Drill Through" into the raw record details for granular investigation.
* **Export-Ready Details:** Specialized "Detail Tabs" provide pre-formatted tables designed for rapid export to Excel, supporting ad-hoc deep-dives and administrative audits.

## 📈 Business Value
* **Efficiency:** Automated the ingestion and normalization of 21 manual reports per week.
* **Accuracy:** Eliminated manual data-merging errors by using standardized relational IDs.
* **Transparency:** Provided real-time visibility into the "Revenue Pipeline," allowing for proactive bottleneck identification.
