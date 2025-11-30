# Credit-Default Risk Scoring & Predictive Modelling (RiskScoreML)

## Overview
This project builds an end‑to‑end credit‑risk analytics pipeline for a fintech lender seeking to make data‑driven lending decisions.  Using historical application and credit‑bureau data, we engineer predictive features, train logistic‑regression models to estimate the probability of default (PD) and compare performance to tree‑based challenger models.  The project emphasises transparency, model evaluation and regulatory compliance, and includes dashboards and an executive summary.

## Business Problem
Fintech lenders need a bespoke scorecard to rank applicants by default risk.  Off‑the‑shelf scores are generic, while simple heuristics cannot capture complex relationships in the data.  The goal is to build a robust model that predicts default probability, segments borrowers into risk tiers and complies with explainability requirements.

## Features
- SQL ETL scripts to ingest and transform raw borrower data.
- Python modules for data cleaning, imputation, encoding and feature engineering.
- Logistic‑regression model that maps a linear combination of features to a PD using the logit function【388525786682809†L69-L83】; challenger models using decision trees for comparison.
- Model evaluation using ROC/AUC, precision‑recall, stability and fairness metrics.
- Generation of risk scores and borrower segments.
- Power BI/Tableau dashboard visualising score distributions, ROC curves and fairness diagnostics.
- Excel workbook for monitoring scorecard stability and calibration.
- Comprehensive documentation and PDF report summarising methodology and findings.

## Repository Structure

```
riskscoreml/
    data/           # raw & processed application and credit‑bureau data
    src/            # Python modules for preprocessing, feature engineering & model training
    notebooks/      # analysis notebooks for EDA, modelling & evaluation
    dashboards/     # Power BI/Tableau dashboards (.pbix/.twb) visualising performance
    docs/           # risk scorecard report, regulatory notes & PDF summary
    README.md
    requirements.txt
```

## Getting Started
1. Clone this repository and navigate into the folder.
2. Create a Python virtual environment and install dependencies:  
   ```bash
   python -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```
3. Load or generate sample application data in `/data`, then run the SQL scripts in `/src` to ingest the data into a local SQLite/PostgreSQL database.
4. Execute the Jupyter notebooks in `/notebooks` to perform exploratory data analysis, feature engineering and model training.  Update paths in the notebooks to point to your data.
5. Review the generated dashboards in `/dashboards` and export them as interactive reports for stakeholders.
6. Read the PDF executive summary in `/docs` for interpretation of model results and fairness considerations.

## Deliverables
- Cleaned and engineered dataset with training/test splits.
- Python scripts and notebooks implementing logistic regression and tree‑based models.
- Risk scores and PD estimates for each borrower.
- SQL and Excel files supporting data ingestion and scorecard monitoring.
- Interactive dashboard visualising ROC curves, score distributions and fairness metrics.
- PDF report documenting methodology, model performance and regulatory compliance.

## Extensions
To make this project more advanced, consider integrating gradient‑boosting or neural network models, scaling the score to a 300–850 range for deployment, adding a REST API for real‑time scoring and implementing monitoring scripts to track model drift and bias.
