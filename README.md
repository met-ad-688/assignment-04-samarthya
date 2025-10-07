# Assignment 04 - Salary Prediction Analysis using PySpark

## Project Overview

This project implements a machine learning pipeline using **PySpark** to predict job salaries from the Lightcast job postings dataset, demonstrating distributed data processing, feature engineering, and model comparison techniques.

## Objectives

- **Data Processing**: Process large-scale job postings dataset using PySpark distributed computing
- **Feature Engineering**: Create meaningful features from job characteristics using PySpark ML  
- **Model Comparison**: Evaluate Linear Regression, Polynomial Regression, and Random Forest using PySpark MLlib
- **Performance Analysis**: Assess model effectiveness using RMSE, R², and MAE metrics

## Dataset

- **Source**: Lightcast job postings dataset (684MB, 131 columns)
- **Valid Records**: ~32,000 salary records after cleaning
- **Target Variable**: SALARY_AVG (engineered from salary ranges using PySpark)

## Methodology

The analysis follows a PySpark-based approach:

1. **PySpark Session Setup** - Initialize distributed computing environment
2. **Data Loading and Quality Assessment** - Load large dataset into Spark DataFrame
3. **Target Variable Engineering** - Create SALARY_AVG using PySpark SQL functions  
4. **Feature Engineering** - Select and prepare features using PySpark ML transformers
5. **Model Development** - Train regression models using PySpark MLlib
6. **Performance Evaluation** - Compare models using PySpark ML evaluation metrics

## Model Performance

**Best Performing Model**: Random Forest
- **R² Score**: 0.3246 (explains 32.5% of salary variance)
- **RMSE**: $37,888 (±33.1% of mean salary)
- **MAE**: $29,238

## Key Findings

- **Experience Requirements**: Dominant factor (63% importance)
- **Job Duration**: Secondary factor (11% importance)  
- **Geographic Location**: Moderate impact (7% importance)

## File Structure

```bash
assignment-04-samarthya/
├── assignment04-samarthya.qmd      # Main analysis document
├── assignment04-samarthya.ipynb    # Jupyter notebook version
├── data/lightcast_job_postings.csv # Source dataset
└── README.md                       # Project documentation
```

## Usage

1. **Quarto Document**: `quarto render assignment04-samarthya.qmd`
2. **Jupyter Notebook**: Open `assignment04-samarthya.ipynb` for interactive analysis

**Note**: Ensure Java and PySpark are properly configured before running the analysis.

---

**Course**: MET AD 688 | **Institution**: Boston University | **Semester**: Fall 2025
