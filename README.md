#  House Price EDA Analysis

This project performs Exploratory Data Analysis (EDA) on the King County House Price dataset using Python.

The analysis includes data understanding, distribution analysis, outlier detection using the IQR method, outlier treatment, and correlation analysis.

---

##  Dataset Information

- Dataset: King County House Sales
- Total Rows: 21,613
- Total Columns: 21
- No missing values found
- Date column converted to datetime format

---

##  EDA Steps Performed

### 1️ Data Understanding
- Checked dataset shape, data types, and statistical summary
- Verified absence of missing values

### 2️ Distribution Analysis
- Plotted histogram and boxplot for price
- Observed right-skewed distribution
- Identified presence of extreme high-value houses

### 3️ Outlier Detection (IQR Method)
- Q1 (25th percentile): 321,950
- Q3 (75th percentile): 645,000
- IQR: 323,050
- Upper Bound: 1,129,575
- Total Outliers Detected: 1,159

### 4️ Outlier Handling
- Applied capping (Winsorization) instead of removing rows
- Preserved dataset integrity
- Created `price_outlier_flag` column for tracking

### 5️ Correlation Analysis
Top features influencing house price:
- Grade (0.706)
- Sqft_living (0.695)
- Sqft_living15 (0.629)
- Sqft_above (0.606)
- Bathrooms (0.535)

Key Insight:
House quality and living area size strongly influence price.

---

## 🛠 Tools & Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab

---

##  Files Included

- `task10_eda.ipynb` – Complete EDA notebook
- `cleaned_dataset.csv` – Dataset after outlier treatment
- `eda_findings.txt` – Summary of key findings
- `README.md` – Project documentation

---

##  Conclusion

The dataset was successfully analyzed using statistical and visualization techniques. Outliers were detected using the IQR method and treated using capping. Correlation analysis revealed that house grade and living area are the strongest predictors of price.

The cleaned dataset is now ready for machine learning modeling.
