# 🛒 Scrap products analysis in Bike Manufacturing Using PowerBI

<img width="1200" height="628" alt="cpo12207png" src="https://github.com/user-attachments/assets/292b9200-f739-47ae-b535-29af748b12ff" />

**Author:** Nguyễn Anh Huy  
**Date:** February 2025  
**Tools Used:** Power BI, DAX, Data Modeling  

---

## 📑 Table of Contents  
- 📌 [Background & Overview](#-background--overview)  
- 📂 [Dataset Description & Data Structure](#-dataset-description--data-structure)  
- 🧠 [Design Thinking Process](#-design-thinking-process)  
- 📊 [Key Insights & Visualizations](#-key-insights--visualizations)  
- 🔎 [Final Conclusion & Recommendation](#-final-conclusion--recommendation)  

---

## 📌 Background & Overview  

### 🎯 Objective  
This project delivers a **Power BI dashboard** built on the **AdventureWorks production dataset**, aimed at providing **production managers** with clear, data-driven insights into:  
- Production performance metrics across orders, quantity, and delivery timelines  
- Resource allocation and efficiency across locations and categories  
- Quality control and cost variance to optimize manufacturing processes  
- Operational improvements to reduce scrap rates and delays  

### 👤 Who is this project for?  
✔️ Production managers needing operational performance insights  
✔️ Data analysts focusing on manufacturing analytics  
✔️ Quality control teams targeting process improvements  
✔️ Operations leaders optimizing resource allocation and costs  

### ❓ Key Business Questions  
- What is the current **production performance** in terms of orders and quantity?  
- How are **resources and time** distributed across locations and categories?  
- What are the key factors affecting **quality and cost variance**?  
- How can **scrap rates and delays** be minimized in the production process?  

---

## 📂 Dataset Description & Data Structure  

### 📌 Data Source  
- **Source:** AdventureWorks production dataset (internal database)  
- **Size:** ~73K records  
- **Format:** CSV  

### 📊 Data Tables  
1. **BillOfMaterials** – Details of materials required for production  
2. **DimEndDate** – End date dimensions for production scheduling  
3. **DimStartDate** – Start date dimensions for production scheduling  
4. **Location** – Production location details  
5. **Parameter** – Configuration parameters for production processes  
6. **Product** – Product specifications and details  
7. **ProductCategory** – Product category classifications  
8. **ProductCostHistory** – Historical cost data for products  
9. **ProductInventory** – Inventory levels of products  
10. **ProductListPriceHistory** – Historical list price data for products  
11. **ProductSubcategory** – Product subcategory classifications  
12. **ProductTable** – Comprehensive product data table  
13. **ScrapReason** – Reasons for scrap occurrences  
14. **TransactionHistory** – Transaction records related to production  
15. **WorkOrder** – Work order details for production tasks  
16. **WorkOrderRouting** – Routing details for work orders  

### 🔗 Data Relationships  
| From Table    | To Table          | Join Key         | Relationship Type |  
|---------------|-------------------|------------------|------------------|  
| WorkOrder     | Product           | ProductID        | Many-to-One      |  
| WorkOrder     | Location          | LocationID       | Many-to-One      |  
| WorkOrder     | ScrapReason       | ScrapReasonID    | One-to-Many      |  
| Product       | ProductSubcategory| ProductSubcategoryID | Many-to-One |  
| ProductSubcategory | ProductCategory | ProductCategoryID | Many-to-One |  

---

## 🧠 Design Thinking Process  

1️⃣ **Empathize** → Understand production managers’ need for real-time performance and quality dashboards  
2️⃣ **Define** → Focus on efficiency, quality, and cost optimization  
3️⃣ **Ideate** → Map key KPIs (Orders, Quantity, On-Time Rate, Scrap Rate, Avg Production, Avg Delay Days)  
4️⃣ **Prototype & Review** → Build iterative dashboards with 3 lenses: **Manufacturing Overview, Process & Resource Performance, Quality & Cost**  

---

## 📊 Key Insights & Visualizations  

### I. Manufacturing Overview  
<img width="1429" height="802" alt="image" src="https://github.com/user-attachments/assets/976ccc53-ee7d-4996-bc5e-d7b829b258ad" />

📌 **Findings:**  
1. **Order Volume Growth** – Total orders at **73K (+11.9% vs LY)**, total quantity at **4M (+10.2% vs LY)**.  
2. **On-Time Rate Stable** – Maintained at **69%**, with a slight decline (-3.4% vs LY).  
3. **Scrap Rate Increase** – Rose to **0.24% (+16.9% vs LY)**, indicating quality concerns.  
4. **Production Efficiency** – Average production at **13.24 hours**, up slightly (+2% vs LY).  
5. **Delay Impact** – Average delay days at **5.6 days (+11% vs LY)**, affecting delivery timelines.  

---

### II. Process & Resource Performance  
<img width="1432" height="799" alt="image" src="https://github.com/user-attachments/assets/596edb61-0d4b-471a-805a-3ff0834c62b3" />

📌 **Findings:**  
1. **Resource Allocation** – Components dominate resource hours (e.g., 12K hours in December), Bikes at ~4K hours.  
2. **Work Order Completion** – Majority completed within 0-16 days, 7K orders >20 days.  
3. **Queue Time Variation** – Average queue time across locations ranges from **3.9 to 4.3 days**.  
4. **Time Share Distribution** – Operation sequence 8 has the highest average time share (0.83 days).  

---

### III. Quality & Cost  
<img width="1427" height="801" alt="image" src="https://github.com/user-attachments/assets/6992ffcc-f3d5-4199-8cd9-59c048c76192" />

📌 **Findings:**  
1. **Cost Variance** – Actual cost ($3.36B) exceeds standard cost ($125.1M) by **$3.36B**, driven by HL Road Handlebars.  
2. **Scrap Cost Distribution** – Final Assembly incurs the highest scrap cost (~145K), Specialized at ~15K.  
3. **Primary Scrap Reasons** – Trim length issues (673 units) and wheel misalignment (314 units) top the list.  
4. **Delay & Late Work Orders** – Sequence 4 shows 5.6 days delay and 22.4% late orders.  
5. **On-Time vs Scrap Rate** – Location 50 has the lowest on-time rate (0.11%) and highest scrap rate (0.18%).  

---

## 🔎 Final Conclusion & Recommendation  

### 📌 1. Market Expansion  
- **Insight:** Resource allocation shows Bikes as the primary focus, with Components underutilized.  
- **Recommendation:**  
  - Optimize **resource allocation** to balance Bikes and Components production.  
  - Invest in **automation for high-delay locations** (e.g., Location 50).  
  - Monitor **scrap cost trends** in Final Assembly to reduce waste.  

---

### 📌 2. Product Portfolio  
- **Insight:** HL Road Handlebars and HL Mountain Frame show significant cost variances.  
- **Recommendation:**  
  - Review **manufacturing processes** for high-variance products (e.g., Handlebars).  
  - Develop **quality checks** for Frames to reduce scrap (e.g., Trim length issues).  
  - Phase out or redesign **underperforming SKUs** with high scrap rates.  

---

### 📌 3. Operations & Efficiency  
- **Insight:** Delays (5.6 days) and scrap rates (0.24%) indicate inefficiencies in sequences 5 and 6.  
- **Recommendation:**  
  - Shorten **queue times** in high-delay locations (e.g., 4.4 days at Location 50).  
  - Implement **preventive measures** for top scrap reasons (Trim length, Wheel misalignment).  
  - Replicate **efficient processes** from low-delay locations (e.g., Location 10).  

---

### ✨ Overall Business Impact  
Implementing these recommendations will enable:  
- **Improved production efficiency** through optimized resource allocation and reduced delays.  
- **Reduced scrap and cost variance** via targeted quality improvements.  
- **Enhanced operational performance** through process optimization and waste reduction.
