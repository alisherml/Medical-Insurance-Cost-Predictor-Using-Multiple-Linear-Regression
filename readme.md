# 🏥 Medical Insurance Cost Predictor
### Multiple Linear Regression | End-to-End Machine Learning Project

This project builds a **Machine Learning model** to predict **medical insurance charges** based on demographic and health-related features. The project demonstrates a complete ML workflow including **data preprocessing, exploratory data analysis (EDA), feature engineering, model training, and evaluation**.

---

# 📌 Project Objective
The goal of this project is to analyze the **insurance.csv** dataset and develop a predictive model that estimates **medical insurance charges** using **Multiple Linear Regression**.

This project focuses on:
- Understanding relationships between health and demographic variables
- Preparing data for machine learning models
- Training a regression model
- Evaluating model performance using standard regression metrics

---

# 📂 Dataset Information

The dataset contains health and demographic attributes that influence insurance costs.

| Feature | Description |
|------|------|
| age | Age of the individual |
| sex | Gender |
| bmi | Body Mass Index |
| children | Number of dependents |
| smoker | Smoking status |
| region | Residential region |
| charges | Medical insurance charges (Target Variable) |

---

# 🛠️ Technologies Used

### Programming Language
- Python

### Libraries
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn

---

# 🔄 Machine Learning Workflow

## 1️⃣ Data Cleaning
To ensure data quality, the dataset was checked for inconsistencies.

Steps performed:
- Checked missing values using `isna()`
- Verified duplicate records using `duplicated()`
- Removed duplicates using `drop_duplicates()`

---

## 2️⃣ Exploratory Data Analysis (EDA)

EDA was performed to understand patterns and relationships in the dataset.

### Key Visualizations
- Distribution plots for **Age, BMI, and Charges**
- Correlation heatmap
- Comparative analysis of **smokers vs non-smokers**

### Key Insight
Smoking status has a **very strong influence on medical insurance charges**, with smokers paying significantly higher premiums.

---

## 3️⃣ Feature Engineering & Preprocessing

A preprocessing pipeline was implemented using **Scikit-Learn's ColumnTransformer**.

### Encoding Techniques

**Ordinal Encoding**
- `sex`
- `smoker`

**One-Hot Encoding**
- `region`

This prevents the **dummy variable trap** and prepares categorical variables for the regression model.

---

## 4️⃣ Train-Test Split

The dataset was split into:

- **Training Set:** 70%
- **Testing Set:** 30%

This ensures proper evaluation of the model on unseen data.

---

## 5️⃣ Model Training

### Algorithm Used
**Multiple Linear Regression**

The model was trained using **Scikit-Learn's LinearRegression** to learn the relationship between input features and insurance charges.

---

# 📈 Model Performance

The model was evaluated using common regression metrics.

| Metric | Value |
|------|------|
| R² Score | **0.7696** |
| Mean Squared Error (MSE) | 33780509.5748 |
| Root Mean Squared Error (RMSE) | 5812.1003 |
| Mean Absolute Error (MAE) | 4145.4506 |
| Intercept | 11254.4033 |

### Interpretation
- The **R² score of 0.7696** indicates that the model explains approximately **76.9% of the variance** in medical insurance charges.
- The error metrics show the difference between **predicted and actual values**.

---

# 🔍 Feature Coefficients (Slopes)

The regression coefficients represent how each feature affects insurance charges.

| Feature | Coefficient |
|------|------|
| sex | 104.8118 |
| smoker | -23628.3672 |
| region_northwest | -486.9346 |
| region_southeast | -970.9688 |
| region_southwest | -926.3229 |
| age | 261.2969 |
| bmi | 348.9069 |
| children | 424.1191 |

### Insights
- **Age** and **BMI** positively influence insurance charges.
- **Number of children** slightly increases insurance costs.
- **Smoking status** has the **strongest impact on insurance charges**.

---

# 📊 Model Visualization

To evaluate model behavior, the following plots were used:

### 1️⃣ Actual vs Predicted Plot
Shows how closely the predicted values match the actual insurance charges.

### 2️⃣ Residual Plot
Helps analyze prediction errors and check regression assumptions.

---

# 🚀 How to Run the Project

### Clone the repository
# 1️⃣ Open the command prompt
git clone https://github.com/alisherml/Medical-Insurance-Cost-Predictor-Using-Multiple-Linear-Regression.git

# 2️⃣ Move into the project folder
cd Medical-Insurance-Cost-Predictor-Using-Multiple-Linear-Regression

# 3️⃣ Install required Python libraries
pip install pandas numpy matplotlib seaborn scikit-learn

# 4️⃣ Launch Jupyter Notebook
jupyter notebook
