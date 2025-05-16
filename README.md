🚔 Predictive Analysis of Drug-Related Police Arrests

📌 Project Overview:

This project applies machine learning techniques to predict whether a police arrest is drug-related based on demographic, temporal, and contextual information. Using over 113,000 arrest records from the Dallas Open Data Portal, we built and evaluated classification models to assist public safety efforts and decision-making.



🗃️ Dataset:

Source: Dallas Open Data Portal
Records: 113,299 (from January 2014 to April 2025)
Attributes: 65 features including age, gender, arrest location/time, and drug involvement indicators.


📊 Key Features Analyzed:

Demographics: Age, Sex, Height, Weight
Time Factors: Hour, Weekday, Month
Location: City, ZIP Code, Arrest Address
Drug Involvement: Target variable - DrugRelated

🔍 Methodology:

Data Cleaning: Null removal, label encoding, duplicate dropping
Exploratory Data Analysis: Python (Seaborn/Matplotlib) & Power BI
Feature Engineering: Age binning, height scaling, IQR filtering
Resampling: SMOTE used to balance class labels

Model Development:

Logistic Regression
Random Forest
XGBoost (best overall performance)

🧪 Model Performance Summary:

Model	Accuracy	ROC-AUC	Recall (>Drug)	F1-Score (>Drug)
Logistic Regression	53–68%	0.63	0.38–0.71	0.34–0.40
Random Forest	~77%	~0.68	~0.10–0.11	~0.16–0.17
XGBoost	78%	0.71	~0.11	~0.17

⚠️ Note: All models struggled with the minority class, despite applying SMOTE. Further improvements are needed.

💡 Key Insights:

Arrests peak between 4 PM – 2 AM, especially Thursday–Saturday and in summer months.
Age group 21–30 has the highest drug-related arrest frequency.
Time of arrest and location are strong indicators.
XGBoost offered the best balance of performance metrics.

🔮 Future Enhancements:

Try advanced resampling techniques (e.g., ADASYN, BalancedBagging).
Add socioeconomic and geographic data to enrich context.
Conduct geospatial clustering with GIS tools.
Explore time series forecasting using LSTMs.
Perform bias/fairness audits across race and gender.
Build a Power BI/Streamlit dashboard for real-time insights.


📚 References:

Dallas Police Arrest Dataset
Géron, A. Hands-On Machine Learning
Chawla et al. (2002). SMOTE: Synthetic Minority Over-sampling Technique
Chen & Guestrin (2016). XGBoost: A Scalable Tree Boosting System
