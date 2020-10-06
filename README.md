# Telecom Churn 

## Backgroud
In the telecom industry, customers are able to choose from multiple service providers and actively switch from one operator to another. In this highly competitive market, the telecommunications industry experiences an average of 15-25% annual churn rate. Given the fact that it costs 5-10 times more to acquire a new customer than to retain an existing one, customer retention has now become even more important than customer acquisition.
The churn prediction is usually more critical (and non-trivial) for prepaid customers, and the term ‘churn’ should be defined carefully.  Also, prepaid is the most common model in India and southeast Asia, while postpaid is more common in Europe in North America.
This project is based on the Indian and Southeast Asian market.
In this project, you will use the usage-based definition to define churn.
Usage-based churn: Customers who have not done any usage, either incoming or outgoing - in terms of calls, internet etc. over a period of time.

Understanding Customer Behaviour During Churn
Customers usually do not decide to switch to another competitor instantly, but rather over a period of time (this is especially applicable to high-value customers). In churn prediction, we assume that there are three phases of customer lifecycle:
- The ‘good’ phase: In this phase, the customer is happy with the service and behaves as usual.
- The ‘action’ phase: The customer experience starts to sore in this phase, for e.g. he/she gets a compelling offer from a  competitor, faces unjust charges, becomes unhappy with service quality etc. In this phase, the customer usually shows different behaviour than the ‘good’ months. Also, it is crucial to identify high-churn-risk customers in this phase, since some corrective actions can be taken at this point (such as matching the competitor’s offer/improving the service quality etc.)
- The ‘churn’ phase: In this phase, the customer is said to have churned. You define churn based on this phase. Also, it is important to note that at the time of prediction (i.e. the action months), this data is not available to you for prediction. Thus, after tagging churn as 1/0 based on this phase, you discard all data corresponding to this phase.

 

## Goals and Objective
For many incumbent operators, retaining high profitable customers is the number one business goal.In this project, We will analyse customer-level data of a leading telecom firm, build predictive models to identify customers at high risk of churn and identify the main indicators of churn.
The dataset contains customer-level information for a span of four consecutive months - June, July, August and September. The months are encoded as 6, 7, 8 and 9, respectively. 
The business objective is to predict the churn in the last (i.e. the ninth) month using the data (features) from the first three months. To do this task well, understanding the typical customer behaviour during churn will be helpful.


## Dataset
The dataset can be downloaded from this drive link (URL: https://drive.google.com/drive/folders/1BICVJoWI9iC2YyJAX1vIRqWt0AIGwmku?usp=sharing)
The dataset has 99999 entries with each row having 226 features.


## Tech Stack 
- Data preprocessing - Numpy, Pandas and Sklearn(Scaling)
- Data Visualization - Matplotlib and Seaborn
- Modeling - Sklean(Decison tree, Random Forest, Adaboost, Gradient Boosting ,PCA , XGB)
- Sampling methods - Weighted class, SMOTE

## Results
### Model Performances
For prediction, Weighted Random forest model performs well with fl score of .57 in train and .55 in test compared to other logistic, Adaboost, Gardient Boosting, XG boosting models.
For Interpretation, Logistic Regression with l1 penalty (lasso) performs better.

### Important Features
Thesea are the important features based on the Logistic Regression
- loc_ic_t2m_mou_8 - As the local incoming calls from other network for the month of 8 increases the Probability of churning decreases
- last_day_rch_amt_8 - As the last day recharge amount for month 8 increases the Probability of churning decreases
- total_rech_num_8 - As the total recharge amount for data in the month of 8 increases the probability of churning decreases.
