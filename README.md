
# Heart Attack Prediction with Diabetes and Lifestyle Management

## Project Overview
This project aims to predict the likelihood of having had a heart attack based on diabetic and lifestyle management factors. Using data from the 2020 Behavioral Risk Factor Surveillance System (BRFSS), we explore correlations between healthy lifestyle habits, diabetic management, and heart attack occurrence.

## Dataset
We used the **2020 BRFSS Survey Data**, which contains responses from individuals regarding their health conditions and habits. Our analysis targeted diabetic patients to examine how their lifestyle and diabetic management might influence heart attack risk.

- **Source:** [2020 BRFSS Data on Kaggle](https://www.kaggle.com)

## Hypothesis
- **Null Hypothesis:** Healthy lifestyle and diabetic management do not show an association with heart attack incidence.
- **Alternative Hypothesis:** Healthy lifestyle and diabetic management will show an association with heart attack incidence, enabling the prediction of who is more likely to have had a heart attack.

## Methodology
1. **Data Cleaning and Imputation:**
   - Handled null values and survey responses such as "refused" or "don't know" by treating them as null.
   - Used `SimpleImputer` with mode strategy to impute missing data.
   
2. **Statistical Analysis:**
   - **Chi-Square Test**: Evaluated the association between lifestyle/diabetic management factors and heart attacks.
   - **Mann-Whitney U Test**: Compared ranks of factors between heart attack and non-heart attack groups.

3. **Modeling:**
   - Initially tested several models including Logistic Regression, Random Forest, KNN, XGBoost, and Lasso/Ridge regression.
   - Due to class imbalance (only 6% of the population having had heart attacks), we used **SMOTE** oversampling to balance the dataset.
   - Post-oversampling, Logistic Regression showed the best precision but still suffered from low recall.

## Results
- We were able to reject the null hypothesis and show an association between heart attack incidence and certain factors like exercise, smoking, insulin usage, and gender.
- However, the associations were not strong enough to reliably predict heart attacks, as model performance remained poor across multiple approaches.

## Conclusion
While our analysis confirmed some associations between healthy living and diabetic management with heart attacks, the prediction of heart attacks in the diabetic population was challenging due to the complexity of the factors involved.

## References
- Centers for Disease Control and Prevention. (2023). Heart Disease Facts.
- Lassale C., et al. (2018). Obesity and metabolic health with coronary heart disease.
- Johns Hopkins Medicine. (2023). Smoking and cardiovascular disease.
