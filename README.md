# Falcon-9-Reusability-Cost-Prediction-Framework

## 🚀 Project Overview
SpaceX has disrupted the aerospace industry by offering Falcon 9 launches at **$62 million**, significantly lower than the industry standard of **$165 million**. This competitive advantage is driven by the company's ability to recover and reuse the rocket's first stage. 

This project implements an end-to-end data science pipeline to predict the probability of a successful first-stage landing. By quantifying these outcomes, we can accurately estimate launch costs and provide strategic intelligence for organizations competing in the commercial space sector.

## 🛠️ Technical Workflow

### 1. Data Acquisition & Refinement
* **Multi-Source Ingestion:** Integrated data via REST API calls to the SpaceX database and automated web scraping of legacy launch records using **BeautifulSoup**.
* **Data Wrangling:** Executed rigorous cleaning protocols in **Pandas** to handle missing telemetry and normalize mission parameters for downstream modeling.

### 2. Exploratory Data Analysis (EDA) & Database Management
* **SQL Integration:** Migrated processed datasets into an **IBM Db2** instance to perform structured querying and relational analysis.
* **Statistical Visualization:** Utilized **Matplotlib** and **Seaborn** to identify mission success correlations across payload mass, orbit types, and launch sites.

### 3. Geospatial & Visual Analytics
* **Interactive Mapping:** Developed spatial visualizations using **Folium** to analyze geographical patterns in launch site success rates.
* **Dashboarding:** Engineered a real-time analytical interface using **Plotly Dash**, featuring interactive sliders and dropdowns for dynamic data exploration.

### 4. Predictive Modeling & Optimization
We evaluated multiple classification algorithms to determine the most reliable predictor of landing success:
* **Preprocessing:** Applied data standardization and feature engineering to enhance model sensitivity.
* **Hyperparameter Tuning:** Optimized models using **GridSearchCV** across Logistic Regression, SVM, and Decision Trees.

## 📊 Key Results
The predictive models were benchmarked on a hold-out test set to ensure robustness:

| Model | Accuracy |
| :--- | :--- |
| **Decision Tree Classifier** | **94.44%** |
| **SVM (Support Vector Machine)** | **83.33%** |
| **K-Nearest Neighbors** | **83.33%** |
| **Logistic Regression** | **83.33%** |

## 📁 Repository Structure
```text
├── data/           # Raw and processed datasets
├── notebooks/      # Step-by-step Jupyter notebooks for each module
├── scripts/        # Python utilities for processing and modeling
├── dash_app/       # Source code for the interactive Plotly Dash app
└── README.md       # Project documentation
