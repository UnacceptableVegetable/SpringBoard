# Predicting Timely Response To Consumer Complaints

The Consumer Financial Protection Bureau is an independent agency of the United States government responsible for consumer protection in the financial sector. Complaints that the CFPB sends to companies for response are published in the Consumer Complaint Database after the company responds, confirming a commercial relationship with the consumer, or after 15 days, whichever comes first.

The goal of this project is the predict whether or not consumer complaints receive timely responses based on features of the data and specifically on the narrative provided by the consumer. 


# Data

The Consumer Complaint Database is a collection of complaints about consumer financial products and services that were sent to companies for response. The database generally updates daily. We will be looking at complaints filed in 2022. 

https://www.consumerfinance.gov/data-research/consumer-complaints/


# Notebooks

1. [Data Wrangling and EDA](https://github.com/UnacceptableVegetable/SpringBoard/blob/main/Capstone%20Three/EDA.ipynb)

Many columns are irrelevant to timely response, and so are dropped. A Chi-square test was performed on the many categories to see which most affected the rate of timely response. In addition to consumer narrative, the top 3 categorical features are the companies, the product and sub-product. 

2. [Preprocessing and Modeling](https://github.com/UnacceptableVegetable/SpringBoard/blob/main/Capstone%20Three/modeling.ipynb)

Redacted text must be handled for the consumer narrative. Afterwards, TF-IDF Vectorization is implemented to allow models to process the text. Ordinal encoding was used for the remaining categorical variables as the features often had over a hundred different categories. 

3 Models were initially compared: Decision Tree, Random Forest, and Logistic Regression. 

## Model Metrics
Final model features, parameters, hyperparameters, and performance metrics.

[model_metrics.txt](https://github.com/UnacceptableVegetable/SpringBoard/blob/main/Capstone%20Three/model_metrics.txt)

## Report 
[capstone_three_final_report.pdf](https://github.com/UnacceptableVegetable/SpringBoard/blob/main/Capstone%20Three/capstone_three_final_report.pdf)
