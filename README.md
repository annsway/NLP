# Summary

This was my individual final project for a Text Mining course (INFO 6350) at Cornell University in the Spring 2022 semester. The intuition of this project was to utilize machine learning methodologies to classify NASDAQ-100 stock performance based on the Risk Factors from hundreds of 10-K Reports.

# Restult

**Q1: What are the tones or sentiments used to describe the risks of companies? Are they related to the stock prices?**

Based on the sentiment analysis and the results of t-test, there was a significant difference in both the **positive** and **trust** emotions between below-average and above-average stock prices. That is, when companies performed better than the average stock prices, they tended to be more optimistic about their risks and would be more likely to assure their investors about their competence in the market.

**Q2. Can we build a classifier to categorize the IT sector and non-IT sector by their Risk Factors? If so, what features are most important?**

All the classifiers were able to surpass the baseline accuracy benchmark of 0.5559 even without optimization of parameters. The **random forest** classifier (max*feature=2) based on the top 20 features from the risk corpus was successfully reached to a high accuracy score of 0.9. The top 20 important features showed us the most identifiable for the IT sectors, such as \_computing, engineering, oci (Oracle Cloud Infrastructure), semiconductor, software, technology, and so on*. The random forest classfier successfully classify the IT vs. Non-IT sectors in the risk corpus.

**Q3: Can we build a classifier to categorize the below-average-stock-price and above-average-stock-price by their Risk Factors from 10-K reports? What are the most important features to distinguish them? Can we improve the accuracy of our classifiers?**

All the classifiers were able to surpass the baseline accuracy benchmark of 0.3947. In particular, it seems random forest with the default parameter max_features=None and max_features=100 has the highest accuracy scores, and the one with max_features=None had the best F1 score, which was still lower than the baseline F1 0.566.

Code and detailed explaination can be found in [NLP-Project.ipynb](https://github.com/annsway/NLP/blob/master/NLP-Project.ipynb).

# Get started with the project

### 0. Clone this repository to your local computer `git clone https://github.com/annsway/NLP.git`

### 1. Run `jupyter notebook`

### 2. Run web-scraping-and-data-prep.ipynb

This step will scrap the 10-K reports from SEC website and the stock price data from Yahoo Finance site.

### 3. Run NLP-Project.ipynb
