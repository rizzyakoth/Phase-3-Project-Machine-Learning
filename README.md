# SYRIATEL CUSTOMER CHURN
In Syria, telecommunications services face a unique set of circumstances. The industry is highly regulated, with the government-owned Syrian Telecommunications Establishment (STE) maintaining a stronghold on fixed-line markets. This regulatory environment, combined with infrastructure disparities, particularly in remote areas relying on satellite communications, creates a complex landscape for telecom providers. This dynamic presents both challenges and opportunities. Despite initiatives to liberalize the market, fixed-line markets remain monopolized by STE. The mobile broadband landscape, though equipped with 3G and some LTE infrastructure, faces challenges in achieving widespread penetration. SyriaTel strives to provide reliable and innovative services to its diverse customer base.
# Problem Statement
SyriaTel, a prominent telecommunications company in Syria, is grappling with a pressing issue—increased customer churn. The emergence of customers discontinuing their services poses a significant risk to the company's stability and growth. To address this challenge, the key objective is to build a robust classifier capable of predicting whether a customer is likely to churn in the near future.
# Objectives
The objectives are to:
a.	Identify the key factors influencing customer churn by analyzing historical data.
b.	Develop a predictive model- Create a machine learning model to predict customer churn based on historical data.
c.	Enhance customer satisfaction by addressing specific issues contributing to churn.
d.	Implement proactive retention strategies- Utilize insights from the predictive model to develop and implement targeted retention strategies for at-risk customers.
# Data Understanding
The dataset is derived from SyriaTel’s customer records and interactions. The dataset is a csv file from https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset/code. It has 21 columns but we can mention a few of them (‘State’, ‘Account Length’, ‘Area code’, ‘Phone Number’, ‘International Plan’, ‘Voice Mail Plan’) etc. Each row represents an individual customer, capturing various aspects of their interactions with SyriaTel. 
Imagine scrolling through a list of customers and their details, seeing where they're located, how long they've been with SyriaTel, and their calling habits. Think of the dataset as a snapshot, providing a glimpse into customer behaviors and patterns. We start by cleaning the dataset before we go into data analysis by 
1.	Handling missing values - Imagine filling in gaps in information, ensuring we have a complete picture of each customer.
2.	Removing duplicates - Think of it like cleaning up identical entries, making sure each customer is unique.
# Data Analysis
1.Univariate analysis
![image](https://github.com/rizzyakoth/Phase-3-Project-Machine-Learning/assets/142317233/abe23cb4-b89b-4d8f-918d-e01585c23458)
This is the account length distribution
2. Bivariate Analysis
![image](https://github.com/rizzyakoth/Phase-3-Project-Machine-Learning/assets/142317233/4abc73d2-09a7-49c2-8cae-f0a06969cabe)
These are some of the categorical features and their relationship with target variable 'churn'.There is a high number of customers who have not churned from the services.
# Modeling
The best performing model is the XGBoost with an accuracy of 0.95 and f1 score of 0.79. In as much as it is a good metric, there might be overfitting and we need to perform hyperparameter tuning to reduce overfitting.
Below is feature importance for random forest, with total day charge in the lead.This model also had an accuracy score of 0.93 and F1 score of 0.67.
![image](https://github.com/rizzyakoth/Phase-3-Project-Machine-Learning/assets/142317233/12388a94-d660-427b-bbc1-4ec7a7fb4a2d)
# Evaluation
We evaluate using accuracy,precision and recall. In this case recall show how many positive cases were able to be predicted correctly.We are concerned with the false negative more than the false positives.Failure to predict the customer will churn, we are at risk of loosing money to a customer.Precision ensures targeted and accurate interventions, while recall captures a significant portion of actual churn instances. The balanced F1 score reflects a harmonized trade-off between precision and recall.
# Recommendations
We can draw some recommendations from our modeling:  
1.	Continuous monitoring: 
•	Establish a system for ongoing monitoring of the model's performance.  
•	Regularly update the model with fresh data to enhance its accuracy and relevance.
2.	Customer Feedback Integration:
•	Integrate customer feedback mechanisms to enhance the model's predictive capabilities.  
•	Incorporate qualitative insights to refine retention strategies and improve customer satisfaction.
3.	Strategic Retention Initiatives:
•	Leverage the model's insights to implement targeted retention strategies.  
•	Tailor interventions based on customer segments and usage patterns identified by the model.
# Next Steps
