# Predicting default on credit card data

Data from [UCI ML Archives](https://archive.ics.uci.edu/ml/machine-learning-databases/00350/default%20of%20credit%20card%20clients.xls)

In this small notebook, I cover:
- Simple data cleaning
- Simple feature engineering
- Data pipelining through scaling, PCA, and a machine learning model

___

## Key insights:

:white_check_mark: Check what is important for the business

From a machine learning perspective, `accuracy` may __NOT__ always be the best measure. In this case, the __true positive rate (or `recall rate`)__ is more important. This is because from a business perspective, predicting that a customer will not default but actually defaulted can have costly :warning: :money_with_wings: :warning: consequences for the business.

:white_check_mark: Increasing `Recall rate` from __18.5%__ :arrow_right: __53.8%__

Another important thing to note is that class imbalances (too much non-default, too little default data) can severely affect recall rate. In this experiment, I ran the original data that has 77% non-default and 23% default rates. The recall rate was only at __18.5%__. Now I reduced the data to have 50-50 split of default and non-default data, and the recall increased to  __53.8%__

