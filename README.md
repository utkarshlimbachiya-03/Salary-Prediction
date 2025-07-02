**Salary Prediction Using Linear Regression**

This project focuses on predicting employee salaries based on features like:
Age
Gender
Education Level
Job Title
Years of Experience

The entire workflow includes:
1. Data exploration & cleaning
2. Statistical analysis & preprocessing
3. Model training, evaluation, and visualization

---

**Dataset Overview**

**Rows**: 6,704
**Features**: 6 ('Age', 'Gender', 'Education Level', 'Job Title', 'Years of Experience', 'Salary')
**Problem**: Predict Salary (continuous variable)


**Phase 1: Data Cleaning & Exploration**

**Data Structure:**
'Age', 'Years of Experience', 'Salary' =**Numeric**
'Gender', 'Education Level', 'Job Title' = **Categorical**

**Data Cleaning:**
Filled missing 'Years of Experience' using average by Age
Filled missing 'Salary` based on average' by 'Job Title'
Imputed missing 'Education Level' using mode from the same job group
Removed 73% duplicate rows for clean analysis
Replaced inconsistent entries (e.g., "Bachelor's" vs "Bachelor's Degree")



**Phase 2: Statistical Processing**

**Skewness Correction:**
Applied **log(x + 1)** transformation to `Age` and `Years of Experience`
Reduced skewness to < 0.5 for normality approximation

**Normalization:**
Applied **StandardScaler** to standardize:
Mean = 0
Std Dev = 1

**Categorical Encoding:**
Education Level: Ordinal Mapping (Unknown: 0, Bachelor's: 1, ...)
Gender: One-Hot Encoding (Male, Female, Other)
Job Title: Frequency Encoding (handles 193 unique titles)

**Phase 3: Model Training & Evaluation**

**Model Used:**
**Linear Regression**
Trained on 80% of the dataset, tested on 20%

**Evaluation Metrics:**
Train Accuracy: 0.7910765074301789
Test Accuracy: 0.7849867723021282
Mean Absolute Error: 17476.670709373662
Mean Squared Error: 581026398.4149253


**Data Visualizations**
**Actual vs Predicted Salary (Standardized Experience)**
Shows how predicted salaries compare against actual, with standardized experience on the x-axis.

**Actual vs Predicted Salary (All Features)**
A scatter plot with a reference line to show prediction closeness. Ideal predictions would lie on the red line.

**Key Learnings**
Data preparation is **more complex and more important** than model training.
Encoding high-cardinality features (Job Titles) with **frequency encoding** helped avoid sparse matrices.
**Log transformation** reduced skewness and helped the regression model generalize better.
A **Linear Regression** model can still perform well with **proper preprocessing**.

**Tools & Libraries**
Python 3
Pandas, NumPy
Matplotlib, Seaborn
scikit-learn

**Future Work**
Try **Ridge, Lasso, or ElasticNet** for regularization
Add **cross-validation** and **grid search**
Build an interactive **dashboard using Streamlit or Power BI**
Convert notebook to an **end-to-end pipeline**





