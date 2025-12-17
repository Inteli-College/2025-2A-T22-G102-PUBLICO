# **Project Status Report – Data Platform for St. Paul’s School**

## **Project Overview**

The project aims to design and implement a **centralized and auditable data architecture** for St. Paul’s School, focused on consolidating academic and administrative data around a **student-centric model**.
The solution prioritizes governance, scalability, and compliance with LGPD, while minimizing adoption friction for teachers and staff.

At the current stage, the project is focused on establishing a **solid Bronze Layer foundation**, which is a prerequisite for all future analytical and reporting capabilities.

---

## **Current Project Status**

### **Overall Status**

**🟡 In Progress – Bronze Layer Implementation**

The project has successfully implemented the **first functional integration** between the school’s ERP (**iSAMS**) and **SharePoint**, using **Power Automate**.
Due to technical constraints related to the **on-premises Data Gateway**, the scope of this phase was adjusted to prioritize reliability and auditability over full data warehouse integration.

---

## **Completed Deliverables**

### **1. Architecture and Strategy**

* Definition of a **student-centric data architecture**, with a single master entity for student identity.
* Formal definition of **SharePoint as the Bronze Layer**, responsible for raw data storage and audit.
* Logical separation between Bronze (SharePoint), future Silver (SQL transformations), and Gold (analytics).

**Status:** ✅ Completed

---

### **2. SharePoint Bronze Layer**

* Creation of the primary SharePoint list:

  * **`Datawarehouse_Isams_Pupils`**
* This list acts as the **central repository of student data**, containing:

  * Real and production data
  * ERP identifiers
  * Demographic and enrollment information
  * Metadata for auditing and traceability

**Status:** ✅ Completed

---

### **3. iSAMS ERP Integration**

* Successful connection to the **iSAMS API**.
* Definition of iSAMS as the **authoritative source** for student master data.
* Secure API consumption design.

**Status:** ✅ Completed

---

### **4. Power Automate Ingestion Flow**

* Implementation of a **Power Automate flow** to:

  * Consume data from the iSAMS API
  * Parse and validate responses
  * Create and update records in SharePoint
* Storage of **real student data** in the Bronze Layer.

**Status:** ✅ Completed

---

## **Partially Completed / Adjusted Scope**

### **5. Data Warehouse & SQL Integration**

* Planned integration with SQL Data Warehouse postponed.
* Main blocker:

  * **On-premises Data Gateway complexity and environment constraints**
* Decision taken:

  * Prioritize SharePoint as a **stable and auditable Bronze Layer**
  * Defer SQL integration to a later phase

**Status:** ⚠️ Deferred (Technical Constraint)

---

## **Key Technical Constraints Identified**

| Constraint                    | Impact                         | Mitigation Decision              |
| ----------------------------- | ------------------------------ | -------------------------------- |
| Data Gateway setup complexity | Blocked SQL ingestion          | Focus on SharePoint Bronze Layer |
| Environment limitations       | Delayed Silver/Gold layers     | Modular architecture preserved   |
| Sensitive data handling       | Required careful scope control | Raw data stored with audit       |

---

## **Data Maturity Achieved**

| Capability                      | Status                |
| ------------------------------- | --------------------- |
| Centralized student master data | ✅                     |
| Automated ERP ingestion         | ✅                     |
| Real production data available  | ✅                     |
| Audit and traceability          | ✅                     |
| Teacher-friendly interface      | ✅                     |
| Analytical dashboards           | ❌ Not yet implemented |
| Cross-domain analytics          | ❌ Not yet implemented |

---

## **Next Planned Steps**

1. Stabilize and document the Bronze Layer structure
2. Expand ingestion to additional iSAMS endpoints (grades, attendance)
3. Re-evaluate SQL integration and Data Gateway feasibility
4. Implement Silver transformations (data quality, normalization)
5. Build Power BI semantic model and dashboards

---

## **Conclusion**

Despite infrastructure limitations, the project successfully delivered a **real, working data ingestion pipeline** using **production data**, which is a critical milestone.

The decisions made during this phase demonstrate:

* Technical maturity
* Architectural flexibility
* Strong governance awareness
* Real-world problem-solving

The current solution provides a **solid foundation** for future analytical layers, ensuring that the platform can evolve incrementally without rework.

---