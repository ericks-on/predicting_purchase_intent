# Overview
The business needs to understand and predict customer purchase intent to better prioritize high-value prospects, optimize marketing strategies, and improve conversion rates. By leveraging machine learning models, the aim is to identify key behaviors and signals of purchase intent in real time and make data-driven predictions that can enhance sales and customer engagement.

## Success Criteria
* Accuracy - atleast 85%
* Precision, recall and f1_score - atleast 85%

# Data Understanding
The data is from [Kaggle](https://www.kaggle.com/competitions/22122shop/data)

There are 18 variables with 10 quantitative and 7 categorical input features, 500K observations (one row or web session per online user) in a tabular format with the first 50K rows missing the Rev revenue flag (1 for purchase intent and 0 otherwise). The data was collected for the period of 1 year.

Features description (from the dataset authors):

1. `Administrative (Adm)`, `Informational (Inf)`,` Product Related (Prd)`: 
    - counts of different page types viewed by the user in that session. Values are derived from the URL information of the pages visited by the user and updated in real time when a user takes an action, e.g. moving from one page to another.
2. `Administrative Duration (AdmDur)`, `Informational Duration (InfDur)`, and `Product Related Duration (PrdDur)`: 
    - total time spent on the page of the specified type.
3. `Bounce Rate (BncRt):` 
    - %visitors who enter the site from that page and then leave ("bounce") without triggering any other requests to the analytics server during that session. Measured by Google Analytics
4. `Exit Rate (ExtRt)`: 
    - %visitors that were the last in the session. Calculated as for all pageviews to the page. Measured by Google Analytics.
5. `Page Value (PgVal)`: 
    - average value for a web page that the user visited before completing an e-commerce transaction.
6. `Special Day (SpclDay)`: 
    - closeness of the site visiting time to a specific special day (e.g. Mother’s Day, Valentine's Day) in which the sessions are more likely to be finalized with transaction. The value of this attribute is determined by considering the dynamics of e-commerce such as the duration between the order date and delivery date. For example, for Valentine's day, this value takes a nonzero value between Feb 2 and Feb 12, zero before and after this date unless it is close to another special day, and its maximum value of 1 on Feb 8.
7. `Operating system (OS)` of the user's PC
8. `Browser (Bsr)`: web user's web browser
9. `Region (Rgn) `of the web user
10. `Traffic type (TfcTp)`: TBD
11. `Visitor type (VstTp)`: Type of visitor
12. `Weekend (Wknd)`: whether the page view event took place on weekend
13. `Month of the year (Mo)`: the month of the page view event

# Results
From the results, our model performs really well.
- `Accuracy = 99%`: this implies that the model correctly identifies if a customer has purchase intent or not 99% of the times.
- `Precision = 99%`: Out of all the Predictions that a customer has purchase intent, 99% are correct.
- `Recall = 96%`: This means that our model correctly identifies 96% of all the customers who actually have purchase intent.

# Conclusion
Final mode chosen is the` RandomForestClassifier` with `max_depth=30 and n_estimators=200`

Our model meets all the success criteria marking a success to the modelling process.
