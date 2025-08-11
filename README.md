# Task 5 – Exploratory Data Analysis (Titanic Dataset)

## 📌 Objective
Perform an in-depth **Exploratory Data Analysis (EDA)** on the Titanic dataset to understand data distributions, relationships between features, and key factors influencing survival.  
Deliverables include a **Google Colab/Jupyter Notebook** and a **PDF report** containing plots with written observations.

---

## 📂 Files in Repository
- `task5_eda.ipynb` – Google Colab/Jupyter Notebook with full EDA steps.
- `train.csv` – Titanic dataset used for analysis.
- `report.pdf` – PDF version of the analysis with plots and observations.
- `README.md` – This file, explaining the project.
- `requirements.txt` – List of Python libraries used.

---

## 🛠 Tools & Libraries
- **Python** 3.x
- **Pandas** – Data manipulation & cleaning
- **NumPy** – Numerical operations
- **Matplotlib** – Data visualization
- **Seaborn** – Advanced visualization
- **Statsmodels** – Multicollinearity (VIF calculation)
- **Google Colab** – Environment used for analysis

---

## 📊 EDA Process

### 1. **Data Loading & Inspection**
- Used `.info()`, `.describe()`, `.value_counts()` to understand dataset structure and statistics.
- Checked for missing values and data types.

### 2. **Missing Value Analysis**
- Visualized missingness using `sns.heatmap()`.
- Noted high missing values in `Cabin`, moderate in `Age`, minimal in `Embarked`.

### 3. **Univariate Analysis**
- Histograms for `Age`, `Fare`.
- Countplots for `Sex`, `Pclass`, `Embarked`.
- Observed skewness in `Fare`.

### 4. **Bivariate Analysis**
- Compared survival rate across categorical features (`Sex`, `Pclass`, `Embarked`) using `groupby()` and `sns.barplot()`.
- Used boxplots for numerical features (`Age`, `Fare`) against survival.

### 5. **Multivariate Analysis**
- Created correlation heatmap using `sns.heatmap()`.
- Generated `sns.pairplot()` for selected features to visualize trends.
- Calculated VIF scores to check multicollinearity.

### 6. **Feature Engineering**
- Created new features: `FamilySize`, `IsAlone`, `Title`, `Deck`.
- Imputed missing values using median/mode and grouped medians for `Age`.

### 7. **Outlier & Skewness Handling**
- Identified outliers in `Fare` using IQR method.
- Applied `log1p` transformation to reduce `Fare` skewness.

---

## 📌 Summary of Key Insights
- **Sex**: Females had a much higher survival rate.
- **Pclass**: Higher class passengers had better survival chances.
- **Fare**: Higher fares generally correlated with survival.
- **Family Size**: Very large families or solo travelers had lower survival chances.
- **Embarked**: Passengers from 'C' port had higher survival rates.
- Missing values in `Cabin` make it less reliable without transformation.

---



---
