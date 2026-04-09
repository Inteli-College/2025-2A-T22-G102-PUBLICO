# **Project Status Report – Data Platform for St. Paul’s School**

## **Project Overview**

The project aims to design and implement a **centralized, scalable, and auditable data platform** for St. Paul’s School, focused on consolidating academic and administrative data through a **student-centric model**.

The solution integrates multiple data sources, enabling **data-driven decision-making** across operational, tactical, and strategic levels. It prioritizes:

- Data governance and LGPD compliance  
- Scalable architecture (Bronze / Silver / Gold layers)  
- Analytical consistency through KPI standardization  
- Usability and accessibility in the frontend layer  

At the current stage, the project has evolved from a **data ingestion foundation** into a **structured analytical platform in development**, with ongoing improvements in analytics, architecture, and product maturity.

---

## **Current Project Status**

### **Overall Status**

**🟡 In Progress – Transition from Data Foundation to Analytical Platform**

The project has successfully implemented a **functional data ingestion pipeline** using real data from the school’s ERP (**iSAMS**) into **SharePoint (Bronze Layer)** via **Power Automate**.

Additionally, the project has progressed into:

- KPI review and analytical structuring  
- Architecture evolution planning  
- Frontend documentation and UX improvements  
- Accessibility validation and enhancements  

---

## **Completed Deliverables**

### **1. Architecture and Strategy**

- Definition of a **student-centric architecture**
- Clear separation of:
  - Bronze Layer (SharePoint – raw data)
  - Silver Layer (planned transformations)
  - Gold Layer (analytics and BI)
- Initial architecture evolution roadmap defined

**Status:** ✅ Completed

---

### **2. SharePoint Bronze Layer**

- Creation of the main SharePoint list:

  - **`Datawarehouse_Isams_Pupils`**

- Implementation of:
  - Raw data storage
  - Audit fields (timestamps, source, metadata)
  - Real production data ingestion

**Status:** ✅ Completed

---

### **3. iSAMS ERP Integration**

- Successful integration with **iSAMS API**
- Definition of ERP as **single source of truth for student data**
- Implementation of secure API ingestion logic

**Status:** ✅ Completed

---

### **4. Power Automate Ingestion Flow**

- Automated pipeline implemented to:
  - Extract data from iSAMS
  - Parse and validate responses
  - Insert/update records in SharePoint

- Supports:
  - Incremental updates
  - Data traceability

**Status:** ✅ Completed

---

### **5. KPI Review and Analytical Framework**

- Identification of inconsistencies in KPI definitions
- Proposal of KPI standardization model
- Definition of comparability structures (e.g., class vs class, year vs year)

**Status:** 🟡 In Progress

---

### **6. Frontend Documentation and UX Analysis**

- Initial documentation of dashboard structure
- Identification of usability gaps:
  - Lack of KPI explanation
  - High cognitive load
  - Limited analytical guidance

- Proposal of improvements:
  - Tooltips for KPI explanation
  - Trend indicators (↑ ↓)
  - Improved filtering logic

**Status:** 🟡 In Progress

---

### **7. Accessibility Evaluation**

- Validation of color palette against **color blindness scenarios**
- Identification of critical improvement points:
  - Need for icons alongside colors
  - Need for labels and text support

- Initial accessibility recommendations defined

**Status:** 🟡 In Progress

---

## **Partially Completed / Adjusted Scope**

### **8. Data Warehouse & SQL Integration**

- Planned migration to SQL-based Data Warehouse postponed

**Reason:**

- Complexity of **on-premises Data Gateway**
- Environmental constraints

**Decision:**

- Maintain SharePoint as **Bronze Layer**
- Defer structured warehouse implementation

**Status:** ⚠️ Deferred (Technical Constraint)

---

## **Key Technical Constraints Identified**

| Constraint                    | Impact                         | Mitigation Decision              |
|-----------------------------|--------------------------------|---------------------------------|
| Data Gateway complexity     | Blocked SQL integration        | Focus on Bronze Layer stability  |
| Environment limitations     | Delayed Silver/Gold layers     | Maintain modular architecture    |
| KPI inconsistency           | Reduced analytical reliability | Introduce KPI standardization    |
| UI limitations              | Reduced usability              | Improve UX and documentation     |

---

## **Data & Product Maturity Achieved**

| Capability                              | Status                |
|----------------------------------------|----------------------|
| Centralized student data               | ✅ Completed          |
| Automated ERP ingestion                | ✅ Completed          |
| Real production data                   | ✅ Completed          |
| Audit and traceability                 | ✅ Completed          |
| Bronze Layer architecture              | ✅ Completed          |
| KPI standardization                    | 🟡 In Progress        |
| Analytical dashboards                  | 🟡 Partial            |
| UX and frontend documentation          | 🟡 In Progress        |
| Accessibility implementation           | 🟡 In Progress        |
| Data warehouse (Silver/Gold)           | ❌ Not implemented    |

---

## **Next Planned Steps**

1. Finalize **KPI Catalog with formulas and examples**
2. Implement **comparative KPI analysis (time, class, subject)**
3. Define **Current vs Future architecture clearly**
4. Implement **Silver Layer transformations (data cleaning and normalization)**
5. Improve **frontend UX with tooltips, trends, and navigation clarity**
6. Apply **accessibility standards (icons, contrast, labels)**
7. Expand data ingestion to:
   - Grades
   - Attendance
   - Behavioral data
8. Reassess **SQL integration feasibility**

---

## **Conclusion**

The project has successfully evolved from a **data ingestion initiative** into a **structured data platform in development**, with clear direction toward analytics and governance maturity.

Key strengths demonstrated:

- Strong architectural foundation  
- Real data integration with production systems  
- Clear evolution roadmap  
- Proactive identification of limitations  
- Focus on usability and accessibility  

Despite technical constraints, the project ensures a **robust and scalable foundation**, enabling incremental evolution toward a **fully integrated academic analytics platform**.

---