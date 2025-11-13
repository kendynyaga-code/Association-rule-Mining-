# 🛍️ Market Basket Analysis — Retail Transaction Data

### 👩🏽‍💻 Author
**Kendi Nyaga**  
Data Science & Analytics   
Project: Association Rule Mining for Retail Insights

---

##  Dataset Description

**Dataset Name:** Retail Transactions Dataset  

**Source:** Online Retail Data from Kaggle 

**Description:**  
The dataset contains transactional records from a UK-based online store, including product descriptions, quantities, and invoice numbers. Each transaction represents items purchased together in a single order.  

**Main Columns:**
- `InvoiceNo` — Unique identifier for each transaction  
- `Description` — Name of the product purchased  
- `Quantity` — Number of units sold  
- `InvoiceDate` — Date and time of the transaction  
- `UnitPrice` — Price per unit  
- `CustomerID` — Unique customer identifier  
- `Country` — Country where the transaction occurred  

---

## ⚙️ Key Steps & Libraries Used

| **Phase** | **Step** | **Tools/Libraries** |
|:-----------|:-----------|:--------------------|
| Phase 1 | Importing and inspecting data | `pandas`, `numpy` |
| Phase 2 | Data cleaning and basket conversion | `pandas`, `re` |
| Phase 3 | Frequent itemset mining and association rules | `mlxtend.frequent_patterns`, `matplotlib` |
| Phase 4 | Business insights & reporting | Markdown documentation, `matplotlib` |

---

## 🔍 Summary of Analysis Steps

### **1️⃣ Data Cleaning & Preparation**
- Removed duplicates and missing values.
- Filtered transactions for the **United Kingdom**.
- Standardized product descriptions (lowercase, trimmed text, removed symbols).
- Converted data into **basket format** using one-hot encoding for each product.

### **2️⃣ Frequent Itemset Mining**
- Applied **Apriori Algorithm** to identify items often purchased together.
- Tested with **two minimum support thresholds (0.02 and 0.05)** for comparison.
- Extracted **frequent itemsets** and their support values.

### **3️⃣ Association Rules**
- Generated rules using metrics: **support**, **confidence**, and **lift**.
- Identified strong associations (lift > 10) between complementary items.
- Example Rule:  
  `{pink regency teacup and saucer} → {green regency teacup and saucer}`  
  - Confidence: 0.82  
  - Lift: 15.9  
  - Interpretation: Customers who buy the pink teacup are very likely to buy the green one as part of a collection.

### **4️⃣ Insights & Business Implications**
- High support items indicate popular bestsellers.
- Strong lift scores reveal natural bundling opportunities.
- Recommended bundling and personalized marketing strategies.

---

## 📈 Sample Outputs

### **Frequent Itemsets (Top 5)**
| Support | Itemsets |
|:--:|:--|
| 0.119 | White Hanging Heart T-Light Holder |
| 0.106 | Jumbo Bag Red Retrospot |
| 0.093 | Regency Cake Stand 3 Tier |
| 0.088 | Party Bunting |
| 0.076 | Lunch Bag Red Retrospot |

### **Top 5 Association Rules**
| Antecedents | Consequents | Support | Confidence | Lift |
|:--|:--|:--:|:--:|:--:|
| {Pink Regency Teacup and Saucer} | {Green Regency Teacup and Saucer} | 0.031 | 0.821 | 15.99 |
| {Jumbo Bag Pink Polkadot, Jumbo Storage Bag Suki} | {Jumbo Bag Red Retrospot} | 0.022 | 0.802 | 7.53 |
| {Roses Regency Teacup and Saucer, Pink Regency Teacup and Saucer} | {Green Regency Teacup and Saucer} | 0.027 | 0.903 | 17.59 |

---

## 🧠 Business Interpretation

1. **Product Bundling Opportunities**
   - Teacup collections and decorative sets often co-occur.
   - Suggests curated bundles for multi-item purchases.

2. **Cross-Selling Strategies**
   - Bags and decorative homeware show consistent co-purchase patterns.
   - Highlight “Frequently Bought Together” suggestions on product pages.

3. **Inventory Optimization**
   - High-support items should always be restocked to prevent lost sales.
   - Complementary products can be displayed side-by-side in stores.

---
- **Notebook Link (Google Colab):** [Open in Google Colab]- **Notebook Link (Google Colab):** [🧠 Open in Google Colab] https://colab.research.google.com/drive/1nHiNhFWEZiXpROjEjw6slOBgN8892CsE?usp=sharing
