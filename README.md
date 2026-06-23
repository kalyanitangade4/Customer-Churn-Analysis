# 📉 Customer Churn Analysis

A data analysis project that digs into customer-level data to identify the behavioral, contractual, and demographic factors driving churn and turns those findings into recommendations a retention team can act on.

## 📌 Problem Statement
Customer churn directly erodes recurring revenue, and acquiring a new customer typically costs far more than retaining an existing one. Rather than guessing why customers leave, this project uses structured analysis to answer a concrete question: **which customer segments are most likely to churn, and what's driving it?**

## 🗂️ Dataset
The analysis uses a customer-level dataset (e.g., the widely-used Telco Customer Churn dataset structure) containing fields such as:

| Category | Example Fields |
|---|---|
| Demographics | Gender, SeniorCitizen, Partner, Dependents |
| Account Info | Tenure, Contract type, PaymentMethod, PaperlessBilling |
| Services | InternetService, OnlineSecurity, TechSupport, StreamingTV |
| Billing | MonthlyCharges, TotalCharges |
| Target | Churn (Yes/No) |

~7,000 customer records, with churn as a binary outcome.

## 🎯 Objectives
- Quantify the overall churn rate and how it varies across customer segments.
- Identify which contract types, tenure ranges, and services correlate most strongly with churn.
- Determine whether billing factors (monthly charges, payment method) influence attrition.
- Translate statistical patterns into plain-language, actionable retention recommendations.

## 🔍 Methodology
1. **Collect the data** – Gather customer records including demographics, account details, services used, and whether they churned.
2. **Clean the data** – Fix missing values, correct data types, and remove duplicates so the data is ready to analyze.
3. **Explore the data** – Look at how many customers churned overall, and break that down by groups like contract type, tenure, and payment method.
4. **Find patterns** – Compare churned vs. retained customers to see which factors (like short tenure or high monthly charges) show up most often among those who left.
5. **Summarize findings** – Turn the patterns into simple, clear takeaways (e.g., "customers on month-to-month plans churn more").
6. **Give recommendations** – Suggest practical actions the business can take based on what the data shows.

## 📊 Key Findings (Illustrative)
- **Contract type is the single biggest lever:** Month-to-month customers churn at far higher rates than one- or two-year contract holders. Incentivizing a switch to longer commitments (even a modest discount) is likely the highest-leverage retention action available.
- **Early tenure is the danger zone:** Churn risk is concentrated in the first several months. A structured onboarding or check-in program in months 1–3 could catch dissatisfaction before it turns into a cancellation.
- **Fiber-optic customers churn more despite paying more:** This is usually a signal of a service-quality or pricing-perception issue rather than a customer-fit issue — worth investigating with a satisfaction survey or support-ticket analysis for that segment specifically.
- **Suggested next step:** score the current customer base with this model, rank by predicted churn probability, and route the top-decile at-risk customers to a retention team — focusing first on month-to-month, low-tenure, fiber customers, since that's where the model and the EDA agree the risk concentrates.

## 📈 Visualizations Produced
- Churn rate by contract type (bar chart)
- Churn rate by tenure bucket (bar chart / line chart)
- Monthly charges distribution: churned vs. retained customers (box plot)
- Correlation heatmap of numeric features against churn
- Churn breakdown by payment method (stacked bar chart)

## 🛠️ Tools & Technologies
- **Language:** Python 3.x
- **Data Handling:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Statistical Testing:** SciPy (chi-square, t-tests)
- **Environment:** Jupyter Notebook

## ▶️ How to Run

```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Launch the analysis notebook
jupyter notebook churn_analysis.ipynb
```

Or run as a script pipeline:
```bash
python clean_data.py        # prepares the dataset
python eda_analysis.py      # generates charts and summary stats
```

## 💡 Business Recommendations

- Offer **incentives to shift month-to-month customers onto annual contracts** (e.g., discounts), since contract length is the strongest churn signal found.
- Proactively reach out during a **customer's first 90 days**, the period of highest churn risk.
- **Bundle tech support and security add-ons** at low/no extra cost for at-risk segments, since their absence correlates with higher churn.
- Encourage migration away from electronic check payments toward **autopay methods**, which show stronger retention.

## ✅ Conclusion

This analysis shows that churn isn't random — it concentrates heavily among new, month-to-month customers paying higher bills without support add-ons. These are concrete, addressable levers rather than abstract risk factors, which is what makes the findings useful for a retention strategy rather than just a descriptive report.

## 👨‍💻 Author

**Kalyani Tangade**
B.Tech IT Graduate | Aspiring Data Analyst
Mumbai, India
kalyanitangade4@gmail.com
