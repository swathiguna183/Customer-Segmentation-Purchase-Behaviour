# Customer Segmentation Based on Purchase Behaviour

## 📌 Project Overview
This project analyzes historical retail transaction data to segment customers based on their shopping behavior—specifically **Purchase Frequency**, **Spending Amount**, **Recency**, and **Product Preferences**. Instead of sending uniform promotions to all shoppers, data-driven segmentation enables businesses to deliver targeted offers, retain high-value buyers, and reduce wasted discount spend.

---

## 🎯 Problem Statement
Customers vary widely in income, product preferences, shopping frequency, and spending levels. Sending the same generic promotion to every customer is inefficient because:
- **Frequent buyers** do not need heavy discounts to return.
- **Occasional buyers** require targeted incentives to shop again.
- **High-value customers** expect personalized service and exclusive loyalty rewards.

---

## 🛠️ Tools & Technologies Used
- **Python** (Pandas, NumPy, `difflib`, `re`)
- **Jupyter Notebook**
- **Microsoft Excel** (Raw data storage & validation reporting)

---

## 🧹 20-Step Data Cleaning & Validation Pipeline
Starting with **4,000 raw transaction records**, I built a structured Python cleaning workflow to prepare a verified dataset of **3,750 records**:
1. **Deduplication & Structural Cleanup:** Removed 80 exact duplicate rows, deleted 20 completely blank rows, dropped the empty `Remarks` column, and standardized 14 column headers to `snake_case`.
2. **Text & Category Standardization:** Trimmed extra spaces, standardized IDs to uppercase, stripped special characters, mapped category variants into 6 clean categories, and used fuzzy matching (`difflib`) to fix spelling typos (e.g., `'Yoga Mt'` → `'Yoga Mat'`).
3. **Date & Numeric Parsing:** Parsed 6 mixed date formats into standard `YYYY-MM-DD` dates and converted currency/unit strings (e.g., `'Rs. 1,200.00'`, `'2 units'`) into clean numeric values.
4. **Outlier Handling & Smart Imputation:** Flagged invalid values and IQR outliers, recovered customer details across matching records, and mathematically re-derived missing financial fields using `Total = (Quantity × Unit Price) - Discount`.
5. **Automated Validation:** Executed automated quality checks (zero nulls, unique invoice IDs, valid formats, and exact financial math)—all passed with 0 failures.

---

## 💡 Expected Business Impact
- **Personalized Marketing:** Match each customer segment with tailored promotions and product recommendations.
- **Cost Efficiency:** Eliminate unnecessary discounts for loyal, full-price buyers.
- **Higher Retention & Revenue:** Re-engage lapsed shoppers with win-back offers and reward top spenders to maximize lifetime value.
