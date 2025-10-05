# Assignment 04 - Salary Prediction with PySpark

## 📋 Project Overview

This project implements a comprehensive salary prediction machine learning pipeline using PySpark and the Lightcast job postings dataset. The analysis compares three different regression models to predict job salaries based on various features.

## 🎯 Objectives

- **Data Processing**: Use PySpark to process large-scale Lightcast dataset (11.9M rows, 131 columns)
- **Feature Engineering**: Engineer features from structured columns for salary prediction
- **Model Training**: Train and evaluate Linear Regression, Polynomial Regression, and Random Forest models
- **Model Evaluation**: Assess models using RMSE, R², and MAE metrics
- **Visualization**: Create diagnostic plots for model interpretation

## 📊 Dataset

- **Source**: Lightcast job postings dataset
- **Size**: 684MB, 11,992,060 rows × 131 columns
- **Target Variable**: SALARY
- **Features Selected**: 10 variables including 3 continuous, 2 categorical, and additional engineered features

## 🔧 Technical Implementation

### Selected Features

1. **Continuous Variables (3)**:
   - MIN_YEARS_EXPERIENCE
   - MAX_YEARS_EXPERIENCE  
   - DURATION

2. **Categorical Variables (2)**:
   - EMPLOYMENT_TYPE_NAME
   - REMOTE_TYPE_NAME

3. **Additional Features (5)**:
   - EDUCATION_LEVELS_NAME (categorical)
   - STATE_NAME (categorical)
   - IS_INTERNSHIP (binary)
   - COMPANY_IS_STAFFING (binary)
   - MIN_EDULEVELS (ordinal)

4. **Engineered Features**:

   - MIN_YEARS_EXPERIENCE_SQ (polynomial feature)

### Data Preprocessing Pipeline

- **StringIndexer**: Convert categorical variables to numerical indices
- **OneHotEncoder**: Create binary vectors for categorical variables
- **VectorAssembler**: Combine all features into feature vectors
- **Data Split**: 80/20 train-test split with random seed 42

### Models Implemented

1. **Linear Regression**: Baseline interpretable model
2. **Polynomial Linear Regression**: Enhanced with squared experience term
3. **Random Forest Regressor**: Ensemble method (300 trees, max depth 6)

## 📁 Project Structure

```bash
assignment-04-samarthya/
├── salary_prediction_analysis.ipynb    # Main analysis notebook
├── data/
│   └── lightcast_job_postings.csv     # Dataset (684MB)
├── output/                             # Output directory
├── requirements.txt                    # Python dependencies
├── README.md                          # Project documentation
└── .gitignore                         # Git ignore file
```

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Java 8+ (for PySpark)
- Virtual environment recommended

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/met-ad-688/assignment-04-samarthya.git
   cd assignment-04-samarthya
   ```

2. Create and activate virtual environment:

   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Launch Jupyter:

   ```bash
   jupyter notebook salary_prediction_analysis.ipynb
   ```

## 🔍 Analysis Highlights

### Feature Engineering

- Created polynomial features to capture non-linear relationships
- Implemented comprehensive preprocessing pipeline
- Handled missing values and categorical encoding

### Model Evaluation

- Comprehensive comparison using multiple metrics
- Statistical significance testing for linear models
- Feature importance analysis for Random Forest
- Diagnostic plots for residual analysis

### Business Insights

- Identification of key salary predictors
- Feature importance for compensation strategy
- Model recommendations for production deployment

## 🛠️ Technologies Used

- **PySpark 4.0.1**: Distributed data processing and machine learning
- **Python**: Data analysis and visualization
- **Jupyter Notebook**: Interactive development environment
- **Matplotlib/Seaborn**: Data visualization
- **Pandas**: Data manipulation and analysis

## 📋 Assignment Requirements Fulfilled

✅ **Data Processing**: PySpark implementation for large dataset  
✅ **Feature Selection**: 10 variables (3 continuous, 2 categorical)  
✅ **Feature Engineering**: Polynomial features and preprocessing pipeline  
✅ **Model Training**: Linear Regression, Polynomial Regression, Random Forest  
✅ **Model Evaluation**: RMSE, R², MAE metrics with statistical analysis  
✅ **Visualization**: Diagnostic plots and model comparison  
✅ **Documentation**: Comprehensive notebook with interpretations  

## 🔗 Repository

- **GitHub**: [https://github.com/met-ad-688/assignment-04-samarthya](https://github.com/met-ad-688/assignment-04-samarthya)
- **Jupyter Notebook**: `salary_prediction_analysis.ipynb`

## 👨‍💻 Author

**Samarthya**  
Course: MET AD 688  
Assignment: 04 - Salary Prediction with PySpark

## 📝 License

This project is for educational purposes as part of MET AD 688 coursework.

---

**Note**: Run all cells in the Jupyter notebook sequentially to reproduce the complete analysis. The notebook includes detailed explanations, code comments, and interpretations for each step of the machine learning pipeline.
