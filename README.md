# RuralCreditWorthiness: Assessing Credit Worthiness in Rural India Using Machine Learning

## 📌 Problem Statement
Traditional banks assess loan eligibility using credit scores. However, a large population in rural India has no formal credit history, making them ineligible despite their potential repayment capability.

This project addresses that gap by building a machine learning model to:
- Predict the **eligible loan amount** for individuals without prior credit history.
- Analyze and understand their **repayment capability** based on socio-economic features.

---

## 🎯 Objective
To enable **financial inclusion** by using alternative data (personal, financial, housing) to assess creditworthiness and recommend suitable loan amounts in the absence of formal credit scores.

---

## 📊 Dataset Overview
**Source:** Kaggle  
The dataset contains individual records with the following details:

### 1. **Personal Details**
- `city`, `age`, `gender`, `social_class`

### 2. **Financial Details**
- `primary_business`, `secondary_business`
- `annual_income`, `monthly_expenses`
- `old_dependents`, `young_dependents`

### 3. **Household Details**
- `home_ownership`, `type_of_house`, `occupants_count`, `house_area`
- `sanitary_availability`, `water_availability`

### 4. **Loan History**
- `loan_purpose`, `loan_tenure`, `loan_installments`, `loan_amount`

These loan details correspond to previously disbursed and successfully repaid loans.

---

## 🛠️ Solution Approach

### ✅ Step 1: Data Collection
- Imported and explored the dataset from Kaggle.

### ✅ Step 2: Data Preprocessing
- **Missing values**:
  - Categorical: Filled with mode.
  - Numerical: Filled with mean.
- **Encoding**:
  - One-hot encoding for features like `gender`, `type_of_house`.
  - Top 10 frequent `loan_purpose` values were binarized; others grouped into "other".
  
### ✅ Step 3: Descriptive Analysis
- Summary statistics: mean, median, mode, std. dev, and range.
- Visualizations:
  - Histograms, bar plots, boxplots
  - Correlation heatmaps
- Feature analysis:
  - Outlier detection
  - Missing value patterns
  - Feature relationships

### ✅ Step 4: Model Building & Evaluation
- Split dataset into training and test sets.
- Trained various regression models.
- **Best Model**: `Random Forest Regressor`
  - **Accuracy:** 86.6%
  - Evaluation Metrics:
    - **MSE**, **MAE**, **RMSE**

---

## 🧾 Codebase Structure

```bash
.
├── EDA_and_Model_Creation.ipynb   # Exploratory Data Analysis + Model Training
├── Main.py                        # OOP-based model pipeline
├── README.md                      # Project documentation (this file)
├── requirements.txt               # Txt file with project requirements
├── trainingData.csv               # Data from Kaggle

```
---

## 💡 Technologies Used

### Languages & Libraries
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

### Machine Learning Algorithms
- Random Forest Regressor

### IDEs / Tools
- Jupyter Notebook
- Visual Studio Code

---

## 📈 Results

- **Final Model**: Random Forest Regressor
- **Accuracy Achieved**: 86.6%
- Robust handling of heterogeneous features
- Strong generalization on unseen test data

---

## 🌍 Impact

This model can serve as a baseline for **AI-driven microfinance systems** in rural India, helping banks to:

- Confidently lend to individuals without prior credit scores
- Reduce Non-Performing Asset (NPA) risks through data-driven insights
- Promote **financial inclusion** in underserved and unbanked communities

---

## 🧠 Future Scope

- Integrate alternative data sources like mobile usage, utility bills, or transaction patterns
- Deploy the model as a **web-based decision support tool** for rural loan officers
- Use **Explainable AI (XAI)** techniques like SHAP or LIME for feature importance and transparency

---

