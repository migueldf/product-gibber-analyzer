Product Gibber Analyzer
==========================

**Miguel Diaz**

**Data Analytics PT Abr2021**

##Overview
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Include the following points in your overview:

-   What data/business/research/personal question you would like to answer?
    -   On 1995, Amazon.com, Inc. started letting customer post both negative and positive reviews to the products they bought. This move was considered nuts by other retailers, but Amazon vision went far beyond sales: they understood the valuer of earning people's trust by enabling to make smart and informed purchases.

This project aims to build towards this purpuse by enabling customers to get a brief overview of customer's feelings related to products.


##Data Preparation
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Overview:

-   What is your dataset about?
    -   Customer reviews obtained from the reviews site of each product in Amazon. In order to see reviews from an specific product, use the link below replacing ASIN with the specific product ASIN you want to analyze: https://www.amazon.com/product-reviews/ASIN/ref=cm_cr_getr_d_paging_btm_prev_1?pageNumber=1 

-   Where/how did you obtain your dataset?
    -   The data was obtained using web scraping, getting reviews from previoulsy mentioned link. The fixes data set covers the top selling items in the videogame department from Aamazon as of Sep2021.

### Data Ingestion

-   The script used to web scrap the data is contained within the dataset_scraper.ipynb notebook in this repository.


### Data Storage

-   Used dataset is contained in the data folder of this repository under the name "dataset.csv".

##Data Analysis
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Overview

The workflow on this project was:

- Build a web scraper to obtain data from reviews from the Amazon site. The scraped data includes:
    - Overall Star Score
    - Product Title
    - Review Content
- After scraping the data, the next step was to process sentiments from the reviews to assign two different scores to each review:
    - Polarity: shows the overall sentiment of the review on a scale from -1 to 1, where -1 is the most negative sentiment and 1 the most positive.
    - Subjectivity: shows the subjectiveness of the comments made by the customers on a scale of -1 to 1, where -1 is the most objective review and 1 is the most sobjective review.
- After analyzing sentments, the next stap was to identify the most common topics of discussion for both positive and negative reviews. This was made eliminating possible noise made from shared common words between reviews.

### Data Exploration and Visualization

-   Once the previous data was processed, the next step was to visualize the results. The output of the analysis was made through 4 graphs:
    - Overall star score: Pie chart showing the star score distribution from the analyzed reviews.
    - Positivity and subjectivity score: Bar chart showing the median polarity and subjectivity of the analyzed reviews.
    - 2 Wordclouds: wordclouds showing the most common words and phrases of both positive and negative reviews.

##Conclusion
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Customer Reviews help customers to learn more about the product and decide whether it is the right product for them. They should give customers genuine product feedback from fellow shoppers.

Following this idea, the product gibber analyzer helps customers to understand the overall sentiment of customers behind a product and the most common topics liked and disliked regarding the product.

Currently, an online version of this app is available at https://share.streamlit.io/migueldf/product-gibber-analyzer/main/main.py

Further work is being done to improve the quality of the insights provided in the data as well as the ability to introduce any product ASIN without depending on a data set.


## Relevant Links:

- Streamlit app: https://share.streamlit.io/migueldf/product-gibber-analyzer/main/main.py
- Presentation deck: https://docs.google.com/presentation/d/17N2Exj0LsXmmoUB87o3EWiTFWlw30hGvIuAHFyR__SI/edit?usp=sharing

