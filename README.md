Predictive Analytics for Claims Fraud Detection

🔍 Project Overview

The goal of this project is to predict the authenticity of warranty claims by analyzing multiple factors such as region, product category, claim value, and customer details.
Dataset Source: Kaggle
Dataset Size: 358 rows × 21 columns
Techniques Used: Exploratory Data Analysis (EDA) & Machine Learning (Decision Tree, Random Forest, Logistic Regression)

📊Data Dictionary
| Column Name         | Description                                     |
|---------------------|-------------------------------------------------|
| Unnamed: 0          | Index                                           |
| Region              | Region of the claim                             |
| State               | State of the claim                              |
| Area                | Area of the claim                               |
| City                | City of the claim                               |
| Consumer_profile    | Consumer profile (Business/Personal)            |
| Product_category    | Product category (Household/Entertainment)      |
| Product_type        | Product type (AC/TV)                            |
| AC_1001_Issue       | Issue with AC component 1 (0 - No issue/No component, 1 - repair, 2 - replacement) |
| AC_1002_Issue       | Issue with AC component 2 (0 - No issue/No component, 1 - repair, 2 - replacement) |
| AC_1003_Issue       | Issue with AC component 3 (0 - No issue/No component, 1 - repair, 2 - replacement) |
| TV_2001_Issue       | Issue with TV component 1 (0 - No issue/No component, 1 - repair, 2 - replacement) |
| TV_2002_Issue       | Issue with TV component 2 (0 - No issue/No component, 1 - repair, 2 - replacement) |
| TV_2003_Issue       | Issue with TV component 3 (0 - No issue/No component, 1 - repair, 2 - replacement) |
| Claim_Value         | Claim value in INR                              |
| Service_Center      | Service center code                             |
| Product_Age         | Product age in days                             |
| Purchased_from      | Purchased from (Dealer, Manufacturer, Internet) |
| Call_details        | Call duration                                   |
| Purpose             | Purpose of the call                             |
| Fraud               | Fraudulent (1) or Genuine (0) Conclusion       |

📈 Key Insights from EDA

-Warranty claims are most frequent in southern India (especially Andhra Pradesh & Tamil Nadu).
-Fraudulent claims are more common in urban regions like Hyderabad and Chennai.
-TVs have higher warranty claims (personal use) compared to ACs.
-Fraudulent AC claims occur even with no component issues.
-Fraudulent TV claims occur with or without component issues.
-Fraud is more frequent when purchases are made through the manufacturer.
-Fraudulent claims usually involve higher claim values.
-Service Center 13 had the highest number of fraud cases despite fewer overall claims.
-Fraudulent claims are more frequent when customer care calls last < 3–4 minutes.

🤖 Machine Learning Models Used

       Model	           Accuracy	          Observations
Decision Tree Classifier	~91%	    Lower recall for fraud cases
Random Forest Classifier	~92%	    Performed best overall
Logistic Regression	        ~91%	    Good accuracy but recall issues

Due to limited fraud cases and small dataset size, models showed lower recall for fraud detection. Collecting more data will significantly improve results.

✅ Conclusion

This project demonstrates the potential of machine learning in detecting fraudulent warranty claims. By leveraging predictive models, it helps save resources and improves the efficiency of claims processing. The study also highlights the importance of using balanced datasets for accurate fraud detection. For future work, the project can be enhanced by collecting more data, applying advanced techniques such as SMOTE, anomaly detection, and ensemble models, and ultimately deploying the model as a real-time fraud detection tool to streamline warranty claim verification.