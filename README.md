# Market Segmentation for Bank Customers

## Project Overview

Marketing plays a crucial role in business growth and sustainability. Effective marketing strategies can help build a brand, engage customers, and increase revenue. One key challenge for marketers is understanding their customers and identifying their needs to launch targeted campaigns. This case study addresses this challenge by using data science to perform market segmentation.

You have been hired as a consultant by a bank in New York City. The bank has extensive data on their customers for the past 6 months. The goal is to segment these customers into at least 3 distinct groups to launch a targeted marketing campaign.

## Dataset Description

The dataset contains the following features:

- **CUSTID**: Identification of Credit Card holder
- **BALANCE**: Balance amount left in the customer’s account
- **BALANCE_FREQUENCY**: Frequency of balance updates (0 to 1 scale)
- **PURCHASES**: Amount of purchases made from the account
- **ONEOFFPURCHASES**: Maximum purchase amount done in one transaction
- **INSTALLMENTS_PURCHASES**: Amount of purchases done in installments
- **CASH_ADVANCE**: Cash advance given by the user
- **PURCHASES_FREQUENCY**: Frequency of purchases (0 to 1 scale)
- **ONEOFF_PURCHASES_FREQUENCY**: Frequency of one-off purchases (0 to 1 scale)
- **PURCHASES_INSTALLMENTS_FREQUENCY**: Frequency of installment purchases (0 to 1 scale)
- **CASH_ADVANCE_FREQUENCY**: Frequency of cash advances (0 to 1 scale)
- **CASH_ADVANCE_TRX**: Number of transactions with cash advance
- **PURCHASES_TRX**: Number of purchase transactions
- **CREDIT_LIMIT**: Credit card limit for the user
- **PAYMENTS**: Amount of payments made by the user
- **MINIMUM_PAYMENTS**: Minimum amount of payments made by the user
- **PRC_FULL_PAYMENT**: Percent of full payment made by the user
- **TENURE**: Tenure of credit card service for the user

## Project Description

Marketing is crucial for the growth and sustainability of any business. Marketers play a pivotal role in building the company’s brand, engaging customers, growing revenue, and increasing sales. One of the key pain points for marketers is to understand their customers and identify their needs effectively.

By analyzing available data about customers, marketers can create targeted marketing campaigns tailored to specific customer needs. In this case study, data science techniques are applied to perform market segmentation based on customer data provided by a bank.

The dataset includes various features related to customer transactions and credit card usage, which will be used to segment customers into distinct groups. This segmentation will help the marketing team at the bank to launch targeted ad campaigns that address the unique characteristics and needs of each customer group.

## Methodology

### Data Analysis

#### Initial Exploration
- Use `info()` and `describe()` methods to understand the dataset.
- Identify outliers and anomalies, such as customers making a one-off purchase of approximately $40,761 or cash advances of $47,000 and $48,000.

#### Data Cleaning
- **Check for Null Values:**
  - Fill missing values with the mean of 'MINIMUM_PAYMENTS' and 'CREDIT_LIMIT'.
  - Recheck for null values.
  
- **Handle Duplicates:**
  - Check for and drop duplicated entries.
  
- **Drop Unnecessary Columns:**
  - Drop `CUSTID` as it is not useful for clustering.

### Data Visualization
- **Visualize Data Distribution:**
  - Create a KDE plot for all columns to visualize the distribution of data.

### Data Preprocessing
- **Normalization and Scaling:**
  - Normalize and scale the data using `StandardScaler` and `normalize` functions.
  
- **Dimensionality Reduction:**
  - Apply PCA for dimensionality reduction if necessary.

### Market Segmentation
- **Clustering:**
  - Use KMeans clustering to segment customers into distinct groups.
  - Determine the optimal number of clusters based on the dataset.
  
- **Evaluation:**
  - Evaluate the clustering results and interpret the characteristics of each segment.

## Results
- Segmented customers into at least 3 distinct groups based on their transaction behavior and credit card usage.
- Provided insights to the marketing team for targeted ad campaigns.

## Future Work
- Refine the segmentation by exploring additional features or alternative clustering methods.
- Perform a deeper analysis of each segment to develop more personalized marketing strategies.

## Contributions
- This project demonstrates the use of data science for market segmentation, including data cleaning, visualization, and clustering.
- The results will help the bank's marketing team to launch more effective and targeted advertising campaigns.

Feel free to contribute further insights or improvements to this project.
