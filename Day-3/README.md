# Day 3: Enterprise Data Modeling, Relational Architecture & No-Code Business Logic
## 1. Architectural Core Definitions
### 🔹 App vs. Object vs. Tab vs. Record vs. Field
To understand how enterprise systems function on the Salesforce multi-tenant infrastructure, we must break down the hierarchy of data presentation and storage layers:
* **App (Application):** A logical collection of components (Objects, Tabs, Dashboards) curated to deliver a specific business workflow. It serves as the container interface but does not store data itself.
* **Object:** The foundational database table template within the Salesforce schema architecture. It defines the structure, access policies, and metadata layer for specific entities (e.g., `Student__c`).
* **Tab:** The visual navigation endpoint that renders an Object visible within a Lightning Application interface. It maps user-facing navigation to backend database tables.
* **Record:** A single discrete row instance generated inside an Object matrix. It represents a single, concrete entity containing real-world values (e.g., a specific student profile).
* **Field:** An individual column attribute residing inside an Object structure. It enforces explicit datatype parameters (e.g., Currency, Text, Date) for any incoming record data.
## 2. Platform Architecture: Standard vs. Custom Objects
Enterprise scalability requires balancing out-of-the-box functionality with custom platform engineering:
| Architectural Attribute | Standard Objects | Custom Objects |
| :--- | :--- | :--- |
| **Origin Layer** | Shipped natively out-of-the-box by the Salesforce Core Platform framework. | Created dynamically by developers/administrators to meet custom requirements. |
| **Naming Conventions** | Direct system strings (e.g., `Account`, `Contact`, `Lead`). | System appends the distinct programmatic suffix **`__c`** (e.g., `House__c`). |
| **Flexibility / Deletion** | Cannot be deleted from the system core workspace; can only be hidden or renamed. | Fully mutable; can be programmatically deleted, migrated, or packaged into version control. |
| **Standard Automation** | Comes pre-wired with default platform business logic, standard layouts, and relationships. | Requires explicit custom definition for layouts, security matrices, automation rules, and tab routing. |
---
## 3. Relational Blueprint: College Management System Data Model
Designing a clean relational database schema prevents anomalies and ensures absolute referential integrity across college operations.
### 🏢 Entity Relationship Diagram (ERD) Blueprint Matrix
* **Department (`Department__c`)** $\rightarrow$ *One-to-Many* $\rightarrow$ **Course (`Course__c`)**
* **Department (`Department__c`)** $\rightarrow$ *One-to-Many* $\rightarrow$ **Faculty (`Faculty__c`)**
* **Course (`Course__c`)** $\rightarrow$ *One-to-Many* $\rightarrow$ **Student (`Student__c`)**
* **Faculty (`Faculty__c`)** $\rightarrow$ *One-to-Many* $\rightarrow$ **Course (`Course__c`)** *(Assigned Instructor)*
  ScreenShots:
<img width="1861" height="703" alt="Screenshot 2026-05-14 210221" src="https://github.com/user-attachments/assets/059362e3-33da-4327-80fd-eaf7bfd1ba8f" />
<img width="1891" height="684" alt="Screenshot 2026-05-14 210251" src="https://github.com/user-attachments/assets/dd87e606-701a-4539-8d4a-b7cc4e9c8047" />
