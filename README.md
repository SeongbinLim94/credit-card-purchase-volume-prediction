# credit-card-purchase-volume-prediction  
The result of this project is deployed as a blog post. The link is written below.  
https://medium.com/@lim.andrew1/trying-to-open-business-in-korea-here-is-the-market-research-ee03d616970b

## Project Description  
Most of countries are moving toward cashless society. With the development of paying technology, consumers can easily pay for the products without holding cash.  
By analyzing credit card usage data, provided by BC Card which is a credit card company in Korea, purchase volume across each regions, and industry sectors in Korea can be predicted.  
To predict the information, demographic and behavioral information in dataset is also analyzed, being the basis of Random Forest Regression model.  
  
  
## Contained Files  
1. **data**  
In `data` folder, `201901-202003.zip` file is stored. If you decompress the file and look into the dataset, the following columns are contained:  
  - REG_YYMM: Year and month of a credit card usage  
  - CARD_SIDO_NM: The region of a credit card usage (The address of the store)  
  - CARD_CCG_NM: The specific region of a credit card usage  
  - STD_CLSS_NM: The industry domin of stores during the usage of a credit card  
  - HOM_SIDO_NM: The residence of a credit card issuer during the usage of a credit card  
  - HOM_CCG_NM: The specific residence of credit card issuer during the usage of a credit card  
  - AGE: The age of a credit card issuer  
  - SEX_CTGO_CD: The gender of a credit card issuer  
  - FLC: Family Life Cycle of a credit card issuer  
  - CSTMR_CNT: The number of customers of credit card usages  
  - CNT: The number of credit card usages  
  - AMT: Purchase volume of a credit card usage (Korean currency Won is used for each unit)  
2. **bc-credit-card.ipynb**  
`bc-credit-card.ipynb` file contains code that analyze the above features and predict the purchase volume across each regions, and industry domains in Korean domestic market.
    
  
## Libraries Used & Version Control  
  - python 3.8.5  
  - pandas  
  - numpy  
  - matplotlib  
  - sklearn  
  - joblib  
  
  
## Result Summary  
In this research, the Random Forest Regression estimator is tested to predict the purchase volume across industry domains, and paid location. It estimated purchase volume quite well, with the rounded mean squared error of 0.18 (with logarithm base 10). In the created model, CUSTMR_CNT feature is selected to be the most important feature.  
With the analysis of 3 features, FLC, industry domain, and paid month, to the purchase volume, FLC, and industry domian showed notable distribution. The purchase volume was highest in credit card users in FLC 4 (households with children above the age of 18). In industry domains, Korean food sector recorded highest purchase volume. However, surprisingly, the median of purchase volume across each month doesn't show relative difference to each other.  
  
  
## Acknowledgements  
The data set for this project was provided by BC card for the Jeju Credit Card Big Data Contest held by dacon. If you understand Korean language, you can get further information in the following link. https://dacon.io/competitions/official/235615/overview/  
Both Korean langauge and English is used in dataset. The blog post explain enough to understand this research, but further question can be answered through my e-mail. `lim.andrew1@gmail.com`  


## Source
https://dacon.io/competitions/official/235615/codeshare/1228?page=1&dtype=recent&ptype=pub  
https://pinkwink.kr/1296?fbclid=IwAR3nY6uD95Cm3RjDM3YTS9sby47lNWGocIy9w4l_VN9xwchoNNap6MgzjFA  
