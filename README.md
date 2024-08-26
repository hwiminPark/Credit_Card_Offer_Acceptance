# Predictive Modeling for Credit Card Offer Acceptance

## Project Overview
This project involves developing a predictive model to estimate the likelihood of customers accepting credit card offers based on their demographic and financial characteristics. The goal is to identify key factors influencing acceptance to optimize marketing strategies and improve the efficacy of promotional campaigns.

## Data
- **Dataset Source:** [Data World Credit Card Dataset](https://data.world/gautam2510/credit-card-dataset)
- **Description:** The dataset consists of 18,000 customer records with 18 features, including:
  - **Customer Number:** Unique identifier for each customer (Integer)
  - **Offer Accepted:** Whether the customer accepted the credit card offer (Boolean)
  - **Reward:** Type of reward offered (String)
  - **Mailer Type:** Type of mailer used (String)
  - **Income Level:** Customer’s income level (String)
  - **# Bank Accounts Open:** Number of open bank accounts (Integer)
  - **Overdraft Protection:** Presence of overdraft protection (Boolean)
  - **Credit Rating:** Customer’s credit rating (Float/Integer/String)
  - **# Credit Cards Held:** Number of current credit cards (Integer)
  - **# Homes Owned:** Number of homes owned (Integer)
  - **Household Size:** Size of the household (Integer)
  - **Own Your Home?:** Homeownership status (Boolean)
  - **Average Balance:** Average balance across accounts (Float)
  - **Q1 Balance:** Balance in Q1 (Float)
  - **Q2 Balance:** Balance in Q2 (Float)
  - **Q3 Balance:** Balance in Q3 (Float)
  - **Q4 Balance:** Balance in Q4 (Float)

## Methodology
- **Exploratory Data Analysis (EDA):**
  - **Distribution Analysis:** The target variable is highly imbalanced. Most numerical features, excluding balances, show no significant correlation with the target.
  - **Feature Association:** Limited associations between features were found, except for balance-related metrics.
  - **Feature Importance:** Insights suggest that cash back rewards have lower acceptance rates compared to air miles or points. Mailers sent via postcard are more effective than letters. Customers with lower income and credit ratings show a higher likelihood of accepting offers.

- **Preprocessing:**
  - **Data Cleaning:** Addressed missing values and removed irrelevant columns.
  - **Encoding:** Applied one-hot and ordinal encoding to categorical variables for model compatibility.
  - **Scaling:** Standardized numerical features to ensure uniformity in model training.
  - **Data Splitting:** Divided the dataset into training and test sets for accurate model evaluation.

- **Modeling:**
  - **Model Selection and Evaluation:** Tested various models including Logistic Regression, SVC, GaussianNB, Decision Tree, Random Forest, XGBClassifier, AdaBoost, Stacking, and Voting classifiers.
  - **Performance Metrics:** The F1 scores for models ranged from 0.149 to 0.197. Logistic Regression and AdaBoost achieved the highest F1 score of 0.197.
  - **Feature Importance:** Key features influencing acceptance include 'Average Balance', 'Reward_Air Miles', and 'Reward_Cash Back'. Negative impacts were observed with features such as 'Credit Rating' and 'Reward_Cash Back'.

- **Cluster Analysis:** No significant differences between clusters for most categorical and numerical features, with the exception of balance-related metrics.

### Error Analysis
- **Confusion Matrix Analysis:**
  - **Logistic Regression:** High number of false positives (4587) and fewer true positives (590) suggest frequent misclassification of acceptance.
  - **AdaBoost:** Similar pattern with false positives (4357) and true positives (565), indicating consistent prediction challenges.

- **Residual Analysis:**
  - **Model Performance:** Overall poor performance across models, highlighting difficulties in distinguishing between accepted and non-accepted offers.
  - **Error Patterns:** Imbalance in the target variable and lack of strong feature correlations contribute to high false positive rates and reduced prediction accuracy.

## Results
- **Model Performance:** Logistic Regression performed best with an F1 score of 0.197, reflecting the challenges faced by all models in effectively predicting credit card offer acceptance.
- **Key Insights:**
  - Wealthier customers and specific reward types exhibited lower acceptance rates.
  - The lack of strong correlations between features suggests that additional data and feature engineering may be necessary to enhance model performance.

## Additional Resources
- **Detailed Write-Up:** [View Article](https://scribe.rip/@jazzed_olivine_llama_204/predicting-credit-card-offer-acceptance-a-data-science-approach-6b1b45b5da94)
- **PDF Version of Jupyter Notebook:** [View PDF](https://drive.proton.me/urls/CSYK55FQW8#y6m16JwjbJAL)
