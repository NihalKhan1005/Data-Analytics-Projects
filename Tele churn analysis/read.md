## 📊 Business Problem

Customer churn costs telecom companies millions in lost revenue annually. This project analyzes the popular **IBM Telco Customer Churn dataset** (7,043 customers, 21 features) to:
- Identify why customers leave
- Build a simple predictive model to flag high-risk customers
- Visualize insights interactively in Power BI
- Provide actionable recommendations to improve retention

## 🎯 Key Objectives
- Perform exploratory data analysis (EDA) to uncover churn drivers
- Build and evaluate a basic machine learning model for churn prediction
- Query data with SQL for segmentation and profiling
- Create a stakeholder-ready Power BI dashboard
- Recommend business interventions (e.g., contract upgrades, pricing adjustments)

## 🛠️ Tech Stack
- **Languages & Analysis**: Python (pandas, numpy, scikit-learn)
- **Machine Learning**: Logistic Regression (baseline model)
- **SQL**: PostgreSQL, SQLite (aggregations, CTEs, window functions)
- **Visualization & Dashboard**: Power BI (DAX measures, Power Query, slicers, conditional formatting)
- **Other Tools**: Jupyter Notebook, Git/GitHub, Matplotlib/Seaborn for EDA plots

- ## 🔍 Key Insights & Findings
- **Overall Churn Rate**: 26.5% (1,867 customers churned out of 7,043)
- **Strongest Churn Drivers** (from correlations & model coefficients):
  - Month-to-month contracts: **42.7% churn** (vs. 2.8% in 2-year contracts)
  - Fiber optic internet: Correlation **0.308** (highest risk service)
  - Electronic check payments: Correlation **0.302**
  - Higher monthly charges: Churners pay **₹74.44** vs **₹61.27** for stayers
  - Shorter tenure: Churners average **~18 months** vs **~37.6 months** for stayers
- **Protective Factors**: Long-term contracts (-0.302), no internet service (-0.228), dependents/partner

## 📈 Predictive Modeling
- **Model**: Logistic Regression (scikit-learn)
- **Performance**:
  - Test Accuracy: **80.24%**
  - Recall for Churn (class 1): **57%** (catches more than half of actual churners)
  - Precision for Churn: **65%**
  - Confusion Matrix: [[916 TP-like stayers], [161 missed churners], [117 false alarms], [213 caught churners]]
- Feature importance aligns with EDA: contract type, payment method, and internet service dominate.

## 📊 Power BI Dashboard Highlights
- 4 interactive pages: Overview KPIs, Customer Segments, Billing & Services, High-Risk Recommendations
- DAX measures: Churn Rate %, Avg Tenure, Segmented Averages
- Slicers for Contract, Internet Service, Payment Method, Senior Citizen
- Conditional formatting (red for high churn)
- Cross-filtering & drill-down enabled

- ## 💡 Business Recommendations
1. **Promote Long-Term Contracts**: Offer discounts/incentives to convert month-to-month users → potential 20–30% churn reduction in this segment.
2. **Address Price Sensitivity**: Bundle services or loyalty discounts for high MonthlyCharges customers.
3. **Improve Fiber Optic Retention**: Investigate service issues or add value-adds (free streaming/tech support).
4. **Shift Payment Methods**: Encourage auto-pay/credit card over electronic checks.
5. **Early Intervention**: Target customers with <18 months tenure with proactive outreach.
6. 
