# Healthcare Cost Prediction and Analysis

## Project Overview

This repository contains a data science and machine learning project focused on **predicting patients’ healthcare/hospitalization costs** and **identifying the key factors contributing to cost variation**. The goal is to support healthcare institutions, insurance providers, and analysts in cost estimation, decision-making, and strategic planning.

The project follows a structured approach to data cleaning, exploratory analysis, visualization, hypothesis testing, model development, evaluation, and results communication.

---

## Table of Contents

- [Business Scenario](#business-scenario)  
- [Objectives](#objectives)  
- [Dataset Description](#dataset-description)  
- [Project Workflow](#project-workflow)  
  - [Week 1: Data Preparation & Exploration](#week-1-data-preparation--exploration)  
  - [Week 2: Machine Learning & SQL Tasks](#week-2-machine-learning--sql-tasks)  
  - [Week 2: Dashboard & Storytelling](#week-2-dashboard--storytelling)  
- [Key Features](#key-features)  
- [Usage Instructions](#usage-instructions)  
- [Tools & Technologies](#tools--technologies)  
- [Results](#results)  
- [Future Work](#future-work)  
- [License](#license)

---

## Business Scenario

**Problem Statement:**  
Rising healthcare costs are a significant public health concern. Predicting future costs and understanding their drivers is crucial for healthcare providers and insurance companies to make informed decisions.

**Objective:**  
- Predict hospitalization costs for patients.
- Identify significant variables influencing costs.
- Analyze interdependencies among healthcare, demographic, and behavioral features.
- Apply data science and machine learning techniques to derive actionable insights.

---

## Dataset Description

The project uses multiple linked data tables that describe patient demographics, clinical indicators, medical history, hospitalization details, and costs.

### Included Data Files

| File | Description |
|------|-------------|
| `Hospitalization_details.xlsx` | Contains patient IDs, service dates, hospitalization charges, hospital and city tiers, state IDs, etc. |
| `Medical_Examinations.xlsx` | Contains BMI, HbA1c, heart issues, transplant history, major surgeries, smoking status, etc. |
| `Names.xlsx` | Contains patient IDs and full names (used to derive gender). |

The `Customer ID` field is used as the primary key for merging datasets.

---

## Project Workflow

### Week 1: Data Preparation & Exploration

1. **Collate Data:**  
   Merge related tables by `Customer ID` to build a unified dataset.

2. **Data Cleaning:**  
   - Detect and handle missing values.
   - Remove trivial value rows (e.g., `?`).
   - Transform categorical variables (nominal and ordinal).
   - Create dummy variables for key state IDs (R1011, R1012, R1013).
   - Clean irregular fields like `NumberOfMajorSurgeries`.

3. **Feature Engineering:**  
   - Compute patient age from date of birth.
   - Extract gender from salutations in the names dataset.

4. **Exploratory Data Analysis (EDA):**  
   - Visualize distribution of hospitalization costs (histogram, box plots, swarm plots).
   - Compare distributions across gender and hospital tier.
   - Radar chart describing median cost by hospital tier.
   - Stacked bar and frequency charts showing counts by city and hospital tiers.

5. **Hypothesis Testing:**  
   - Test whether average hospitalization costs differ across hospital tiers.
   - Test whether average costs differ across city tiers.
   - Test whether costs differ between smokers and non-smokers.
   - Test independence between smoking and heart issues.

---

### Week 2: Machine Learning & SQL Tasks

#### Machine Learning

1. **Correlation Analysis:**  
   Generate a heatmap to identify highly correlated predictors.

2. **Model Development:**  
   - Build regression models (Linear, Ridge).
   - Apply stratified 5-fold cross validation.
   - Standardize features and optimize hyperparameters.
   - Use sklearn pipelines for workflow automation.
   - Integrate regularization to mitigate bias-variance trade-off.

3. **Gradient Boosting:**  
   - Train a Gradient Boost model.
   - Identify variable importance and eliminate redundant features.

4. **Case Scenario Prediction:**  
   Estimate the hospitalization cost for a specific patient profile using the best model.

#### SQL Analysis

1. Create database schema and enforce primary keys.
2. Run analytical SQL queries to:
   - Identify diabetic patients with heart conditions and compute average statistics.
   - Calculate average cost by hospital and city tier.
   - Count patients with major surgery and cancer history.
   - Count tier-1 hospitals by state.

---

### Week 2: Dashboard & Storytelling

Create a Tableau dashboard that highlights:
- Cost drivers and comparative metrics.
- Hospital tier performance.
- Visual summaries of statistical tests and model predictions.

Emphasis should be on clear data storytelling for stakeholders.

---

## Key Features

- End-to-end data cleaning and preprocessing
- Comprehensive EDA with advanced visualizations
- Hypothesis testing with statistical rigor
- Regression and machine learning models
- SQL analytics and database integration
- Interactive dashboards for stakeholder insights

---

## Usage Instructions

1. Clone this repository.
2. Install required packages using:
   ```bash
   pip install -r requirements.txt

## Tools & Technologies

This project leverages a mix of data science, machine learning, database, and visualization tools:

- **Python** — for data preprocessing, analysis, and modeling  
  - Key libraries: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, `plotly`
- **Jupyter Notebooks** — for exploratory analysis and model development
- **SQL** — for structured querying and database analytics (PostgreSQL or SQLite)
- **Tableau** — for interactive dashboards and data storytelling
- **Excel / OpenPyXL** — for reading and processing source datasets

---

## Results

The final deliverables from this project include:

- A unified and cleaned dataset ready for modeling
- Exploratory visualizations detailing cost distributions and feature relationships
- Results from hypothesis tests with statistical interpretations
- Predictive models for estimating hospitalization costs
- Performance evaluation metrics for all regression models
- SQL query outputs for key business questions
- An interactive Tableau dashboard summarizing insights for stakeholders

---

## Future Work

Potential directions for expanding or improving this project:

- Experiment with additional machine learning algorithms (e.g., Random Forest, XGBoost with optimized tuning)
- Deploy the predictive model through a simple web interface or REST API
- Integrate external socioeconomic or regional datasets for deeper insights
- Enhance the Tableau dashboard with dynamic filters, drill-downs, and user inputs
- Automate the data cleaning and preprocessing pipeline

---

## Contributing

Contributions are welcome! You can help by:

- Suggesting new features or improvements
- Submitting optimized models or visualizations
- Enhancing documentation and code modularity
- Filing bugs or issues via GitHub

Please follow standard GitHub contribution workflow (fork → branch → pull request).

---

## Acknowledgments

This project was completed as part of a structured data science capstone.  
Special thanks to:

- Dataset providers and instructors
- Open-source Python library maintainers
- Online resources and community contributions

---

## License

This project is released under the **MIT License**.  
See the `LICENSE` file in this repository for full details.




