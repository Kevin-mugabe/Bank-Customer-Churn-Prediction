
 # Bank Customer Churn Prediction

This project analyzes and predicts bank customer churn using a dataset of 10,000 records.  
It demonstrates an end-to-end workflow: **data exploration, machine learning model building, evaluation, and dashboard visualization**.  
The goal is to help banks identify customers at risk of leaving and take proactive retention measures.

---

## 📂 Project Structure
---

## 📊 Problem Statement
Banks lose significant revenue when customers close their accounts (“churn”).  
The aim of this project is to **predict customer churn likelihood** and **highlight key drivers** (e.g., inactivity, satisfaction, geography) so management can take targeted action.

---

## 📑 Dataset
- **Rows:** 10,000  
- **Columns:** 18 (demographics, account info, products, complaints, satisfaction score, etc.)  
- **Target Variable:** `Exited` (1 = churned, 0 = retained)

---

## 🔎 Methods
1. **Exploratory Data Analysis (EDA)**
   - Calculated churn rate
   - Plotted churn by age, geography, number of products, and satisfaction
2. **Preprocessing**
   - Dropped identifier columns
   - One-Hot Encoding for categorical variables (`Geography`, `Gender`, `Card Type`)
   - Standard Scaling for numeric variables
3. **Modeling**
   - Logistic Regression (baseline)
   - Random Forest (improved predictive power)
   - Evaluation with **classification report, confusion matrix, ROC-AUC**
4. **Single-Customer Prediction**
   - Function to input customer details and output churn probability
5. **Visualization**
   - Power BI dashboard showing churn KPIs, churn rates by segments, and high-risk customers

---

## 📈 Results
- Overall churn rate: **~20%**  
- **Key drivers of churn:**
  - Inactive membership
  - Low satisfaction score
  - Certain geographies (e.g., Germany had higher churn rates)
- Model performance (Logistic Regression):
  - ROC-AUC: ~0.79
  - Balanced precision and recall
- Random Forest improved recall, useful for catching more churners

---

## 📊 Dashboard (Power BI)
**Dashboard Features (1 page):**
- KPIs: Total Customers, Actual Churn Rate, Predicted Churn Rate, Avg Predicted Probability
- Charts: Churn by Geography, Age Band, Satisfaction Band
- Table: High-risk customers sorted by churn probability
- Slicers: Geography, Gender, Age Band, Products, Active/Inactive, Satisfaction Band

![Dashboard Screenshot](reports/dashboard.png)  <!-- Add a PNG export for quick viewing -->

---

## 🛠️ Tools & Technologies
- **Python (Colab):** pandas, scikit-learn, matplotlib  
- **Machine Learning:** Logistic Regression, Random Forest  
- **Visualization:** Power BI  
- **Other:** joblib (model saving), GitHub for version control

---

## 🚀 How to Run
1. Open `notebooks/churn_analysis.ipynb` in Google Colab or Jupyter  
2. Upload the dataset (`bank_churn.csv`)  
3. Run all cells to reproduce the EDA and models  
4. Open `reports/dashboard.pbix` in Power BI Desktop to explore the interactive dashboard  

---

## 📌 Key Takeaways
- Churn can be predicted with reasonable accuracy using customer demographics + account behavior.  
- Business can reduce churn by focusing on **inactive, low-satisfaction customers**.  
- Combining **Python ML** + **Power BI dashboarding** creates a powerful technical + business story.  

---

## ✍️ Author
Mugabe Kobwila Kevin
kevinmugabe1@gmail.com | www.linkedin.com/in/kevin-mugabe-b80b3b203
