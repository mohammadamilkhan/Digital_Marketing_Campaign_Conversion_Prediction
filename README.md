
#  Digital Marketing Campaign Conversion Prediction

##  Objective

The goal of this project is to build a robust machine learning model to predict customer conversions using demographic and engagement data. This enables:

-  **Improved campaign targeting**
-  **Higher conversion rates**


---

##  Problem Statement

Businesses struggle to efficiently target potential customers. By using machine learning to predict conversions, marketers can allocate resources more effectively and personalize outreach.

---

##  Dataset Overview

- **Rows:** 8000
- **Columns:** 20
- **Target Variable:** `Conversion` (1 = Yes, 0 = No)

### Feature Categories

- **Demographics:** Age, Gender, Income
- **Engagement Metrics:** Ad Spend, Click Through Rate, Conversion Rate, Website Visits, Pages per Visit, Time on Site
- **Campaign Details:** Channel, Type, Email Opens/Clicks, Social Shares

---

##  Exploratory Data Analysis (EDA)

### Highlights

- **Clean Data:** No missing, duplicate, or extreme outlier values.
- **Gender Distribution:** 60.5% Female, 39.5% Male
- **Top Channels:** Referral (21.6%), PPC (20.8%)
- **Top Campaign Type:** Conversion (26.6%)
- **Age Group with Highest Conversions:** 36–45

### Insights

- More time, visits, and pages correlate with higher conversions.
- Email campaigns (opens, clicks) significantly influence conversions.
- High-income users are more likely to convert.

---

##  Preprocessing Steps

-  Removed irrelevant features (e.g., CustomerID)
-  One-hot encoding for categorical features
-  Standard scaling for numerical features
- ⚖ Applied **SMOTE** for class imbalance
-  Split data into 80% train / 20% test sets

---

##  Model Training & Evaluation

### Models Used:

- Logistic Regression
- Decision Tree
- Random Forest
- Support Vector Machine (SVM)
- **XGBoost** (Best performer)

### Model Comparison

| Model                | Accuracy | Precision | Recall | F1 Score | AUC |
|---------------------|----------|-----------|--------|----------|-----|
| Logistic Regression | 93%      | 89%       | 98%    | 93%      | 0.97 |
| Decision Tree       | 87%      | 88%       | 86%    | 87%      | 0.87 |
| Random Forest       | 94%      | 91%       | 99%    | 95%      | 0.98 |
| SVM                 | 93%      | 90%       | 97%    | 94%      | 0.97 |
| **XGBoost**         | **95%**  | **92%**   | **99%**| **95%**  | **0.98** |

 **XGBoost was the most effective model**, offering high accuracy, precision, and AUC with minimal false negatives.

---

##  Power BI Dashboard Highlights

- **Total Ad Spend:** ₹4 Cr+
- **Total Website Visits:** 198,013
- **Average Time on Site:** 7.7 minutes
- **Top Channels:** Referral, PPC
- **Top Campaigns by Engagement:** Email & Conversion
- **Better Performing Audience:** Females, 26–65 years

---

##  Key Conclusions

- More engaged users (time, pages, visits) are more likely to convert.
- Referral and PPC channels are most effective.
- Email engagement strongly influences conversions.
- The 36–45 age group converts most frequently.
- **XGBoost** is the optimal model for deployment.

---

##  Recommendations

- Focus on high-income, engaged users aged 26–65.
- Prioritize referral and PPC channels.
- Leverage email insights for segmented targeting.
- Re-evaluate the strategy behind “Conversion” campaigns.

---

##  Tech Stack

- **Language:** Python
- **Libraries:** Pandas, Scikit-learn, Matplotlib, Seaborn, XGBoost
- **Dashboard:** Power BI
- **Notebook:** Jupyter

---

##  Project Structure

```bash
├── data/
│   └── digital_marketing_campaign_dataset.csv
├── model/
│   └── trained_model.pkl
├── notebooks/
│   └── Digital_marketing_project_ipynbfile.ipynb
├── reports/
│   ├── Presentation_PROJECT.pdf
│   └── Digital_Marketing_html_view.html
├── dashboard/
│   └── POWER_BI_DASHBOARD.pbix
├── README.md
