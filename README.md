# Credit Card Default Prediction

## Project Overview
Predicting credit card defaults using logistic regression for proactive risk management. Complete analysis from data cleaning to business recommendations.

Dataset: [UCI Credit Card Default on Kaggle](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset)  
30,000 customers from Taiwan with 24 features including payment history, demographics, and billing data.

## Quick Start
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
jupyter notebook Credit_Risk_Analysis.ipynb

# Key Results and Insights

## Model Performance
- **ROC-AUC:** 0.74 (48% improvement over random guessing)
- **Optimal Threshold:** 0.55 probability
- **At this threshold:**
  - **Recall:** 58.6% (catches 972 of 1,659 defaults)
  - **Precision:** 44.7% (1,201 false alarms)
  - **Customers flagged:** 32% of portfolio

## Top Risk Factors
1. **Multiple late payments** - Each additional late month increases default odds by 141% (Odds Ratio: 2.41)
2. **Maximum payment delay** - Odds Ratio: 1.57
3. **High credit utilization** - Odds Ratio: 1.18
4. **Lower credit limits** - Odds Ratio: 0.81 (protective factor)

## Key Business Insights
- **Payment behavior matters more than demographics:** Customer actions (late payments, high utilization) predict risk better than age, education, or marital status
- **Consistency matters:** Isolated payment delays have less impact than multiple consecutive late months
- **Actionable thresholds:**
  - Flag customers with more than 2 late months
  - Monitor credit utilization above 60%
  - Review customers scoring above 0.55 default probability

## Business Implications
- **Early intervention:** Identify 59% of potential defaults before they occur
- **Resource allocation:** Focus collections efforts on the highest-risk 32% of customers
- **Risk-based decisions:** Adjust credit limits based on utilization and payment patterns
- **Compliance:** Transparent model with clear risk factors (no black-box decisions)

## Files
- `Credit_Risk_Analysis.ipynb` - Complete Jupyter notebook with analysis
- `requirements.txt` - Python dependencies
- `credit_card_default.csv` - Dataset (download from Kaggle link above)

## Technologies
- Python, pandas, numpy
- scikit-learn (logistic regression)
- matplotlib, seaborn for visualization

## Project Steps (Notebook Contents)
1. Data loading and exploration
2. Cleaning categorical variables
3. Feature engineering (8 new risk metrics)
4. Logistic regression modeling
5. Performance evaluation (ROC, precision-recall)
6. Business interpretation (odds ratios)
7. Threshold optimization
8. Actionable recommendations
