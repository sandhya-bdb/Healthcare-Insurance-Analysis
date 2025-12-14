# Healthcare Cost Prediction and Analysis

## Project Overview

This repository contains a data science and machine learning project focused on **predicting patients’ healthcare/hospitalization costs** and **identifying key factors contributing to cost variation**. The goal is to support healthcare institutions, insurance companies, and analysts with cost estimation, decision-making, and strategic planning.

The project follows a structured workflow involving data cleaning, exploratory analysis, visualization, statistical hypothesis testing, machine learning, SQL analytics, and interactive storytelling.

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
- [Contributing](#contributing)  
- [Acknowledgments](#acknowledgments)  


---

## Business Scenario

**Problem Statement:**  
Rising healthcare costs are a significant public health concern. Predicting future hospitalization costs and understanding their causes is critical for effective resource planning and management.

**Objective:**  
- Predict hospitalization costs for patients.  
- Identify significant factors that contribute to cost variation.  
- Understand relationships between demographic, clinical, and behavioral predictors.  
- Apply data science and machine learning methodologies to a real-world case.

---

## Dataset Description

The project uses linked datasets describing patient demographics, medical examinations, hospitalization details, and outcomes.

### Included Data Files

| Filename | Description |
|----------|-------------|
| `data/Hospitalisation_details.csv` | Hospitalization charge records with patient demographics and tier information. |
| `data/Medical_Examinations.csv` | Medical measures including BMI, HbA1c, and clinical history. |
| `data/Names.xlsx` | Patient names and salutations (used to derive gender). |

Datasets are merged on the `Customer ID` primary key to form a unified analytical dataset.

---

## Project Workflow

### Week 1: Data Preparation & Exploration

1. **Data Integration:**  
   Consolidate all raw data files into a single analytical dataset.

2. **Data Cleaning:**  
   - Detect and handle missing and trivial values (e.g., `?`).  
   - Standardize and transform categorical variables.  
   - Create dummy variables for key state IDs (R1011, R1012, R1013).  
   - Clean and reformat fields such as `NumberOfMajorSurgeries`.

3. **Feature Engineering:**  
   - Calculate patient age from date of birth.  
   - Extract gender from salutations in names.

4. **Exploratory Data Analysis (EDA):**  
   - Histograms, box plots, and swarm plots for cost distribution.  
   - Comparisons across gender and hospital tiers.  
   - Radar charts showing median costs by tier.  
   - Frequency and stacked bar charts for city and hospital tiers.

5. **Hypothesis Testing:**  
   - Test differences in average costs across hospital tiers.  
   - Test differences across city tiers.  
   - Compare costs for smokers vs. non-smokers.  
   - Test independence between smoking and heart issues.

---

### Week 2: Machine Learning & SQL Tasks

#### Machine Learning

1. **Correlation Analysis:**  
   Check predictor correlations and visualize with a heatmap.

2. **Model Development:**  
   - Train Linear and Ridge regression models.  
   - Apply stratified 5-fold cross validation.  
   - Standardize features; tune hyperparameters.  
   - Use sklearn pipelines for workflow automation.  
   - Address bias-variance trade-off using regularization techniques.

3. **Gradient Boost Model:**  
   - Build Gradient Boosting model.  
   - Extract feature importance and identify redundant variables.

4. **Case Scenario Prediction:**  
   Estimate hospitalization cost for a given patient profile using the best model.

#### SQL Analytics

1. Construct database schema and enforce primary keys.  
2. Run SQL queries to:
   - Retrieve diabetic patients with heart issues and compute average age, BMI, and cost.  
   - Calculate average cost by hospital and city tier.  
   - Count patients with major surgeries and cancer history.  
   - Find the number of tier-1 hospitals per state.

---

### Week 2: Dashboard & Storytelling

Create a **Tableau dashboard** highlighting:

- Key cost drivers and trends  
- Visual summaries of clinical and demographic impacts  
- Comparative insights across groups

Focus on **effective storytelling** for stakeholders.

---

## Key Features

- Robust data cleaning and preprocessing  
- Comprehensive exploratory analysis with visualizations  
- Statistical hypothesis testing  
- Regression and machine learning models  
- SQL analytics for business questions  
- Interactive Tableau dashboard  

---

## Usage Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/<your_username>/Healthcare-Insurance-Analysis.git
   cd Healthcare-Insurance-Analysis

2. Install required packages using:
   ```bash
   pip install -r requirements.txt
   
### Getting Started

- [ ] Place dataset files in the `data/` directory
- [ ] Run notebooks in the `notebooks/` folder (start with `capstone1.ipynb`)
- [ ] Review analytical queries in the `sql/` directory
- [ ] Explore dashboard visuals in the `images/` folder

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






