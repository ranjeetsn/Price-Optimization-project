# Coffee chain Retail price optimization project

## Introduction

Pricing a product is a crucial aspect of any business. This project focuses on identifying the optimal prices for items in a cafe based on their past sales and price elasticity. The data is stored in a PostgreSQL database hosted on Amazon RDS and analyzed using various machine learning algorithms in Python.

## Project Overview

This project involves:

Calculating Price Elasticity: Determine the price elasticity for each item using historical sales data.
Optimizing Prices: Use the calculated price elasticity to figure out the optimal price for each item.
Exploratory Data Analysis (EDA): Process and analyze the dataset to prepare it for modeling.
Machine Learning Algorithms: Apply regression trees and ordinary least squares methods to estimate price elasticity and optimize prices.

## Dataset
The data for this project is contained in three CSV files:

Cafe - Sell MetaData.csv: Details about sales made by the cafe.

Columns: Sell ID, Sell Category, Item ID, Item Name
Cafe - Transaction - Store.csv: Information about transactions and sale receipts of the cafe.

Columns: Calendar Date, Price, Quantity, Sell ID, Sell Category
Cafe - DateInfo.csv: Date information corresponding to the transactions performed.

Columns: Date, Year, Holiday, Weekend, School Break, Temperature, Outdoor

## Tools and Techniques

### Techniques
Price Optimization Algorithms:
- Cost-less Pricing
- Competition-based Pricing
- Perceived Value Pricing
- Demand-based Pricing

### Tools
- Exploratory Data Analysis
- Data Cleaning: Remove redundancy and ensure consistency.
- Data Visualization: Use matplotlib and seaborn for visualization.
- Data Merging: Merge datasets using Pandas dataframes.

### Machine Learning Algorithms

- Regression Trees
- Ordinary Least Squares Method

### Model Evaluation

Using statistical parameters like R-squared value to evaluate models.

## Prerequisites

- Python >=3.10.4
- PostgreSQL
- psycopg2 library

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/Price-Optimization-Project.git
```

2. Install the required libraries:
```bash
pip install -r requirements.txt
```

Set up the PostgreSQL database:
- Setup your AWS RDS Data Base as shown below, this step is pretty straight forward:
 <img width="1453" alt="Create AWS RDS Database" src="https://github.com/ranjeetsn/Price-Optimization-project/assets/16061374/52b723e0-87db-4dcc-94ae-4a350cb8b797">

- In the connectivity and Security option, you can get the Endpoint address that you need to connect to your host locally with this address:
<img width="989" alt="Get Endpoint address" src="https://github.com/ranjeetsn/Price-Optimization-project/assets/16061374/bad20597-e8d5-4935-8320-3a6f75cfd91e">

- In MySQL post the address as shown in the image below:
  <img width="670" alt="Server Host address" src="https://github.com/ranjeetsn/Price-Optimization-project/assets/16061374/7fa0a6b6-18d1-472b-b178-1a02058f3c3b">

- Now comes the hard part, To establish connectivity between your local host and the database, it is necessary to configure Inbound rules within the security group, allowing the appropriate traffic to pass through.
  <img width="999" alt="Inbound rules" src="https://github.com/ranjeetsn/Price-Optimization-project/assets/16061374/5315ffc2-5fc9-44d1-9b1e-c91dc6476b61">

- Test the connection to make sure you are connected

3. Running the Project
If you set up a SQL database(recommended)
Fetch data from PostgreSQL database:
import psycopg2

Your code to fetch data
Run the Jupyter Notebook:

jupyter notebook "Price Optimization based on price elasticity.ipynb"

## Application
The solution of this pricing optimization project can be easily extended to various industries like medical, hospitality, insurance, etc.

## FAQs
- How do you do Price Optimization?
Apply different price optimization techniques like reducing cannibalization and cost reduction.

- What is Price Optimization Machine Learning?
Use regression machine learning algorithms like linear regression to estimate price elasticity and optimize prices.

## Conclusion
This project helps in understanding customer behavior through sales data, which is crucial for determining the right price for different products. It utilizes machine learning algorithms to optimize prices and maximize profits based on price elasticity.


