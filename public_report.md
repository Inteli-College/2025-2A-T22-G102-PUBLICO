# Academic Data Hub – St. Paul’s School

## Executive Summary
St. Paul’s School seeks to modernize its academic and administrative reporting by implementing an **integrated data hub**.  
This initiative will centralize data from **teachers (SharePoint), the secretary’s office (academic and financial records), the infirmary, and turnstile systems**, providing interactive **Power BI dashboards**.  

The solution will reduce manual effort, improve reporting accuracy, and empower decision-making at **operational, tactical, and strategic levels**, while ensuring compliance with **LGPD** and data governance best practices.  

---

## Objectives
- Automate the generation of academic and administrative reports.  
- Consolidate multiple data sources into a single platform.  
- Provide teachers, coordinators, and leadership with dashboards tailored to their needs.  
- Reduce manual workload for staff.  
- Strengthen a data-driven culture for educational and operational management.  

---

## Project Backlog
- **Data Sources:**  
  - Teacher inputs via SharePoint.  
  - Academic and financial records from the secretary’s office.  
  - Infirmary logs (student visits and occurrences).  
  - Turnstile data (entries, exits, delays, and absences).  
  - External files and complementary systems.  

- **ETL:** Automated pipelines for data ingestion, transformation, and loading.  

- **Data Lake & Warehouse:**  
  - Data Lake for raw storage and traceability.  
  - Data Warehouse for structured and analytical models.  

- **Visualization:** Interactive Power BI dashboards with **role-based access** for different stakeholders (teachers, coordinators, directors).  

---

## Functional Requirements
- Centralize and integrate data from all sources.  
- Provide dashboards for student performance, attendance, financial history, and health records.  
- Enable filtering by student, class, subject, and academic year.  
- Support alerts and KPIs (academic risk, absenteeism, financial delays).  
- Allow exporting reports in Excel and PDF.  

---

## Non-Functional Requirements
- Ensure full compliance with **LGPD**.  
- Guarantee high availability and scalability.  
- Authentication integrated with Microsoft 365.  
- Role-Level Security (RLS) to restrict access by user profile.  
- Response time ≤ 5 seconds for standard queries.  

---

## Personas
- **Teacher (Operational):** Uses SharePoint to register inputs and monitors dashboards for class performance.  
- **Coordinator (Tactical):** Consolidates performance across classes, identifies patterns, and tracks improvements.  
- **Academic Director (Strategic):** Analyzes executive-level KPIs for institutional planning and decision-making.  
- **IT Staff (Technical):** Manages integrations, ETL, and ensures governance.  
- **Administrative Staff (Secretary):** Tracks financial records and attendance history.  
- **Support Staff (Infirmary):** Records visits and integrates health data into student history.  

---

## Architecture
1. **Data Sources:** SharePoint, secretary’s office (academic and financial), infirmary logs, turnstile systems, and external files.  
2. **ETL:** Automated ingestion using Airflow/dbt, with transformations and LGPD compliance (anonymization and pseudonymization).  
3. **Data Lake:** Stores raw, unprocessed data for auditing and traceability.  
4. **Data Warehouse:** Structured entities including:  
   - `students`  
   - `teachers`  
   - `classes`  
   - `grades`  
   - `attendance`  
   - `financial_history`  
   - `health_visits`  
   - `turnstile_logs`  
   - `indicators`  
   - `permissions`  
5. **Analytics Layer:** Optimized data models for reporting and Power BI integration.  
6. **Visualization:** Power BI dashboards segmented by role (teacher, coordinator, director).  
7. **Governance:** Microsoft 365 authentication, Row-Level Security, and audit logs for sensitive data access.  

---

## Expected Benefits
- **Efficiency:** Significant reduction of manual reporting tasks.  
- **Accuracy:** Reliable and consistent academic and administrative indicators.  
- **Strategic Insights:** Executive dashboards enabling faster and more data-driven decisions.  
- **Integration:** Unified view of academic, operational, and financial information.  
- **Compliance:** Full alignment with LGPD and security standards.  
