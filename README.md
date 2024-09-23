# Shopping Trends Analysis

## Project Overview
The Customer Shopping Preferences Dataset provides insights into consumer behavior and purchasing patterns, including age, gender, payment methods, and purchase frequency. Analyzing this data helps businesses optimize product offerings and tailor marketing strategies. It serves as a valuable resource for enhancing customer satisfaction and aligning business strategies with consumer needs.

(I used this dataset to learn data visualization in Power BI. Please note that this is a synthetic dataset created specifically for beginners, and as such, the insights it provides are limited. Its primary purpose is for learning and practice.)

### Data Source
Customer Shopping Trends data: The dataset used for this analysis is the "shopping_trends.csv" file, containing detailed information about consumer behavior and purchasing patterns. The dataset can be found on [Kaggle](https://www.kaggle.com/datasets/iamsouravbanerjee/customer-shopping-trends-dataset).

### Tools
Microsoft Power BI Desktop

### Data Cleaning/Preparation
In the initial data preparation phase, I performed the following tasks:
1. Data loading and inspection.
2. Removed Duplicates from Customer ID (if any)
3. Check the format for each column
4. Made the following changes to the Frequency of Purchases column using the Replace Values tool in Power Query Editor
    - Replaced Fortnightly to Bi-weekly
    - Replaced Every 3 Month to Quarterly

### Exploratory Data Analysis
EDA involved exploring the data to answer questions such as:
 - What category of items are contributing to frequent sales
 - What is the overall customer satisfaction with the items purchased
 - Who are our customers (Customer Demographics: Age, Size used & Gender)

### Interesting Code I came across
 For the Stars visualization, I created a new measure and included the following code I found while watching a [YouTube Video](https://www.youtube.com/watch?v=rOjEFWDoooQ)

``` Rating = 
VAR _star = ROUND(AVERAGE('shopping_trends'[Review Rating]), 0)
VAR _unstar = 5 - _star
RETURN 
REPT(UNICHAR(11088), _star) & REPT(UNICHAR(9734), _unstar)
```

### Findings
 - Clothing (followed by Accessories,Footwear and Outwear) was the category contributing to most sales irrespective of frequency.
 - Customer satisfaction for all products were 4 out of 5 stars.
 - Most customers were over 45 years of age and are predominatly male.

### Recommendations
1. Marketing can target more female customers in order to increase sale
2. Items sold could include products that might attract younger generations (under 45)

### Limitations
1. The data does not contain any information on the purchase date which could have helped further in analysing this data. 
2. The data is not really consistent or realistic. For example if I select a female clothing item from the ratings table, the % for Male is greater than that for Female.

   
