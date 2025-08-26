# 🏡 Ames Housing Price Prediction  
**End-to-End Regression Modeling with Feature Engineering, Regularization, and Tree-Based Methods**

---

## 📌 Project Overview

This project presents a comprehensive regression modeling pipeline to predict housing prices in Ames, Iowa. It demonstrates the full lifecycle of a data science project — from raw data ingestion and cleaning to exploratory analysis, feature engineering, model training, evaluation, and interpretation. The goal is to build a robust, transparent, and reproducible model that balances performance with interpretability.

---

## 🎯 Objectives

- Predict log-transformed housing prices (`SalePrice_log`) using structured data
- Demonstrate proficiency in data preprocessing, feature engineering, and model selection
- Compare baseline, regularized, and tree-based models using consistent metrics
- Visualize feature importance and communicate insights effectively
- Build a recruiter-ready portfolio artifact with clean code and clear documentation

---

## 📁 Repository Structure
ames-housing-price-prediction/ 
```bash
├── data/                  # Raw and cleaned datasets 
├── notebooks/             # Jupyter notebooks for EDA and modeling 
├── scripts/                # set up the environment 
├── requirements.txt       # Python dependencies
```

---

## 📊 Dataset Description

- **Source**: [Ames Housing Dataset](https://www.kaggle.com/datasets/prevek18/ames-housing-dataset)
- **Observations**: ~2,900 residential properties
- **Features**: 80+ variables including lot size, year built, quality ratings, and neighborhood
- **Target Variable**: `SalePrice` (log-transformed to `SalePrice_log`)

---

## 🔍 Workflow Summary

### 1. Data Cleaning & Preprocessing
- Handled missing values using domain-informed strategies
- Converted categorical variables to appropriate types
- Dropped identifiers (`Order`, `PID`) and target columns from feature matrix
- Applied `np.log1p()` transformation to `SalePrice` to reduce skew

### 2. Exploratory Data Analysis (EDA)
- Visualized distributions and relationships using histograms, boxplots, and scatter plots
- Assessed correlations and feature relevance
- Identified top predictors and flagged outliers

### 3. Feature Engineering
- One-hot encoded categorical variables using `pd.get_dummies(drop_first=True)`
- Created derived features such as:
  - `Total SF` = `Total Bsmt SF` + `1st Flr SF` + `2nd Flr SF`
  - `Age` = `Yr Sold` - `Year Built`
  - `Remod Age` = `Yr Sold` - `Year Remod/Add`
- Ensured all features were numeric before modeling

### 4. Modeling
- **Baseline Model**: Linear Regression  
- **Regularized Models**: Ridge & Lasso Regression  
- **Tree-Based Model**: Random Forest Regressor

### 5. Evaluation Metrics
- Mean Squared Error (MSE)
- R² Score

### 6. Feature Importance
- Extracted top 20 features from Random Forest using `.feature_importances_`
- Visualized using Seaborn barplot

---

## 📈 Modeling Results

| Model               | MSE     | R² Score |
|--------------------|---------|----------|
| Linear Regression   | 0.02   | 0.8904  |
| Ridge Regression    | 0.01   | 0.9232   |
| Lasso Regression    | 0.02   | 0.9017   |
| Random Forest       | 0.01   | 0.9202   |


---

## 🧠 Key Insights

- Log transformation of `SalePrice` improved model stability and reduced skew
- Regularization helped mitigate multicollinearity and overfitting
- Tree-based models captured non-linear relationships and ranked feature importance
- Feature importance analysis revealed consistent top predictors such as `Overall Qual`, `Gr Liv Area`, and `Year Built`

---

## ⚖️ Limitations & Next Steps

This project focuses on structure and clarity over exhaustive optimization. The models are not tuned for peak performance, and cross-validation is not yet implemented. Future improvements could include:

- Hyperparameter tuning with `GridSearchCV`
- Cross-validation for more robust evaluation
- Advanced models (e.g., XGBoost, LightGBM)
- SHAP or permutation importance for interpretability
- Deployment via Streamlit or Flask

---

## 🛠️ Tools & Libraries

- **Language**: Python 3.9+
- **Data Manipulation**: Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn
- **Modeling**: Scikit-learn
- **Notebook Environment**: Jupyter Notebook

---

## 🚀 How to Run Locally

```bash
# Clone the repository
git clone https://github.com/nymisha/ames-housing-price-prediction.git

# Navigate to the project folder
cd ames-housing-price-prediction

# Install dependencies
pip install -r requirements.txt

# Launch the notebook
jupyter notebook notebooks/modeling.ipynb
```

## About Me

I'm Nymisha, a data science learner passionate about building transparent, business-relevant models. I specialize in Python-based workflows, feature engineering, and predictive modeling. My approach emphasizes clarity, reproducibility, and ethical modeling practices. This project reflects my commitment to professional-grade analysis and continuous learning.


## 🤝 Let's Connect

Thanks for checking out my project! I'm always open to feedback, collaboration, or just a good data science conversation. If you're working on something similar or have ideas to share, feel free to reach out — I'd love to connect.

- 💼 LinkedIn: Nymisha Lingamgunta  

