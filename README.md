# 🛍️ Customer Shopping Behavior Analysis

## 📄 Project Overview
This project analyzes **customer shopping behavior** using transactional data from **3,900 purchases** across various product categories.  
The goal is to uncover insights into:
- Spending patterns  
- Customer segmentation  
- Product preferences  
- Subscription trends  

These insights guide **data-driven business decisions** such as pricing strategies, customer loyalty programs, and targeted marketing.

---

## 📊 Dataset Summary
- **Rows:** 3,900  
- **Columns:** 18  
- **Key Features:**
  - Customer demographics — `Age`, `Gender`, `Location`, `Subscription_Status`
  - Purchase details — `Item_Purchased`, `Category`, `Purchase_Amount`, `Season`, `Size`, `Color`
  - Shopping behavior — `Discount_Applied`, `Promo_Code_Used`, `Previous_Purchases`, `Frequency_of_Purchases`, `Review_Rating`, `Shipping_Type`
- **Missing Data:** 37 missing values in `Review_Rating` column (imputed using category-wise median).

---

## 🧮 Exploratory Data Analysis (EDA) — Python
Performed in **Python** using:
- `pandas` for data cleaning and manipulation  
- `PowerBi` for visualization  

### 🔹 Steps:
1. **Data Loading:** Imported dataset using `pandas`.  
2. **Initial Exploration:** Used `.info()` and `.describe()` for structure and summary.  
3. **Missing Data Handling:** Filled missing `Review_Rating` using median per category.  
4. **Column Standardization:** Converted column names to snake_case.  
5. **Feature Engineering:**
   - Created `age_group` by binning age values.
   - Added `purchase_frequency_days` feature.
6. **Data Consistency Check:** Dropped redundant `promo_code_used`.
7. **Database Integration:** Loaded the cleaned dataset into **Mysql** for SQL-based analysis.

---

## 🗃️ SQL Analysis — Business Insights
Structured queries in **Mysql** answered key business questions:

| # | Analysis Goal | Insight |
|---|----------------|---------|
| 1 | Revenue by Gender | Compared total revenue of male vs. female customers |
| 2 | High-Spending Discount Users | Identified discount users spending above average |
| 3 | Top Products by Rating | Found top 5 products with highest average reviews |
| 4 | Shipping Type Comparison | Compared average spend between Standard & Express shipping |
| 5 | Subscribers vs. Non-Subscribers | Analyzed spending and revenue differences |
| 6 | Discount-Dependent Products | Found products most purchased with discounts |
| 7 | Customer Segmentation | Classified customers as New, Returning, Loyal |
| 8 | Top 3 Products per Category | Extracted most purchased items by category |
| 9 | Repeat Buyers & Subscriptions | Checked correlation between purchases >5 and subscriptions |
| 10 | Revenue by Age Group | Calculated total contribution of each age group |

---

## 📊 Power BI Dashboard
An **interactive Power BI dashboard** was built to visualize:
- Revenue by category, gender, and age group  
- Discount vs. purchase behavior  
- Customer segmentation (New, Returning, Loyal)  
- Subscriber vs. Non-subscriber trends  
- Top-rated & top-selling products  

---

## 💡 Business Recommendations
1. **Boost Subscriptions:** Promote exclusive benefits to increase subscription count.  
2. **Loyalty Programs:** Reward repeat buyers to increase retention.  
3. **Review Discount Policy:** Balance between sales volume and profit margin.  
4. **Product Positioning:** Highlight high-rated, high-demand products in marketing.  
5. **Targeted Marketing:** Focus on high-revenue age groups and express-shipping users.  

---

## 🛠️ Tools & Technologies
| Category | Tools Used |
|-----------|-------------|
| Programming | Python (Pandas, NumPy, Matplotlib, Seaborn) |
| Database | Mysql |
| Visualization | Power BI |
| Data Handling | Excel / CSV |
| Environment | Jupyter Notebook / VS Code |

---

## 🚀 How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/customer-shopping-behavior-analysis.git
   cd customer-shopping-behavior-analysis
