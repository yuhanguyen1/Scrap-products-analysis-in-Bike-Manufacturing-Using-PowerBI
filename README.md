# AdventureWorks-Scrap-Analysis
Used Power BI to visualize scrap products of AdventureWorks, including final products, components, creates meaningful insights.

Author: Nguyen Anh Huy

Date: 07/04/2025

Tools used: Power BI (DAX & Visualization)

## Table of Contents

[I. Background & Overview](https://github.com/yuhanguyen/AdventureWorks-Scrap-Analysis/blob/main/README.md#i-background--overview)

[II. Dataset Description & Data Structure](https://github.com/yuhanguyen/AdventureWorks-Scrap-Analysis/blob/main/README.md#ii-dataset-description--data-structure)

[III. Design Thinking Process](https://github.com/yuhanguyen/AdventureWorks-Scrap-Analysis/blob/main/README.md#iii-design-thinking-process)

[IV. Key Insights & Visualizations](https://github.com/yuhanguyen/AdventureWorks-Scrap-Analysis/blob/main/README.md#iv-key-insights--visualizations)

[V.  Final Conclusion & Recommendations](https://github.com/yuhanguyen/AdventureWorks-Scrap-Analysis/blob/main/README.md#v--final-conclusion--recommendations)

## I. Background & Overview

### Objective:

This project uses Power BI DAX & Visualization tool to analyze manufacturing data from AdventureWorks to:

✔️ Monitorize manufacturing performance, including components and bikes assembly.

✔️ Identify reasons that led to scrap products from each category, at what time of the year does the manufacturing record the most scrap products.

### Who is this project for?

✔️ Data analysts & business analysts

✔️ Manufacturing manager & stakeholders

## II. Dataset Description & Data Structure

The data is imported from Google Bigquery public dataset. Here is the Data dictionary:

**Table: Production.BillOfMaterials**

![image](https://github.com/user-attachments/assets/c2fed4df-dfd8-4280-9517-cdb44970fd4a)

![image](https://github.com/user-attachments/assets/41b04177-db0b-4a8a-8718-0ba06a214b7d)

**Table: Production.ScrapReason**

![image](https://github.com/user-attachments/assets/c55c030b-4f61-4a0e-b796-5a8f1d6b5e6f)

**Table: Production.WorkOrder**

![image](https://github.com/user-attachments/assets/d653e1fd-5c51-400c-baad-f01fdd67f375)

**Table: Production.WorkOrderRouting**

![image](https://github.com/user-attachments/assets/c3b7844e-b6ad-4d86-8168-6228c2c19556)

**Table: Product.Product**

![image](https://github.com/user-attachments/assets/edd1c6be-6f35-40d8-8281-48cba9b9f92b)

**Table: Product.ProductCategory**

![image](https://github.com/user-attachments/assets/a8dbf229-b3b8-460f-98c3-9c38e6cf3767)

**Table: Production.ProductSubcategory**

![image](https://github.com/user-attachments/assets/6180526b-247a-4dbe-b126-8e2479fd14f3)

**Data Model**

![image](https://github.com/user-attachments/assets/1237c58d-c44a-40bf-8c29-abfca2320bbf)


## III. Design Thinking Process
The Design Thinking Process was implied to understand dashboard viewers' need to create the best dashboard. The process consist of the following 4 steps:

1️⃣ Empathize

![image](https://github.com/user-attachments/assets/f0ec46df-6321-4f21-8fb7-1761a553be76)

![image](https://github.com/user-attachments/assets/f6360ea9-0c1a-4b00-afd2-ffd083331bce)

2️⃣ Define point of view

![image](https://github.com/user-attachments/assets/ef464ad9-ef4e-4020-8fe5-00805cfb73b0)

![image](https://github.com/user-attachments/assets/b0032eda-8954-44dc-badc-df17864324db)

3️⃣ Ideate

![image](https://github.com/user-attachments/assets/5bd5b47f-15d7-4352-93a9-a02b1365ca8c)

![image](https://github.com/user-attachments/assets/b9a990ca-e30f-4f0f-9268-71af360c6a89)

4️⃣ Prototype and review

![image](https://github.com/user-attachments/assets/93e87853-69fa-43f4-9f67-13365f9b9c1d)

## IV. Key Insights & Visualizations

**Dashboard**

**Manufacturing Overview**

![image](https://github.com/user-attachments/assets/dafef429-526b-4666-a878-924711e2294f)

**Bikes Analysis**

![image](https://github.com/user-attachments/assets/3c800061-390c-46c9-9fac-3917bc5d23b2)

**Component Analysis**

![image](https://github.com/user-attachments/assets/098b4670-353b-4ab8-ae4a-369522bdc065)

**Key Insights**

+ Production has good growth but fluctuates depending on the time of year. However, the more production, the more defective products and the higher the defect rate.

+ Road bikes are produced the most and are also the car models with the most defects.

+ Wheels are the most scrap components, significantly more than the remaining components.

+ The most common scrap reasons such as drilling, cutting raw materials are subjective errors due to human errors during the processing process.

## V.  Final Conclusion & Recommendations

+ Review production equipment (drilling tools, cutting machines, thermoforming furnaces).

+ Review production staff, if necessary, reduce or recruit replacement staff.

+ Review production staff training process, paying special attention to error-prone stages such as drilling, cutting. If necessary, retrain.

+ There should be close supervision of the production process, especially during peak periods to limit errors.

