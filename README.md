# 🏡 ML-real-estate-prediction

```
Can we build a model to better predict transaction prices of real estate prices?
```

## 💡 Business Background

In a bid to modernize their property valuation process, a leading Real Estate Investment Trust (REIT) based in a small county in New York state launched an ambitious initiative. Their goal: to construct a data-driven real estate pricing model that accurately predicts the fair transaction price of properties before their sale, maintaining an updated understanding of the market's ebbs and flows.

The REIT engaged my services as a data science consultant, presenting me with the challenge of developing a model capable of predicting transaction prices with an average error of less than $70,000. To aid in this mission, they offered an unused dataset from 2016 containing the transaction prices of properties in the REIT's area of operation.

## 📈 Machine Learning Background

* The dataset has 1883 observations in the county where the REIT operates.
* Each observation is for the transaction of one property only.
* Each transaction was between $200,000 and $800,000.
* Target Variable: Transaction Price
* Input Features: 22 independent variable including `Public records for the property`, `Property characteristics`, `Location convenience scores`, `Neighborhood demographics`, `Schools`
* Machine Learning Task: Regression
* Win Condition: Mean Absolute Error (MAE) < $70,000

## 🚀 Getting Started

Initiate the process by establishing an appropriate environment for running a Jupyter Notebook file, making certain that you have the right versions of all required libraries. Following this, proceed to download the data and the .ipynb file. Load the necessary libraries and data in the notebook. Finally, execute the entire notebook by selecting "Run All".

## 🎨 Exploratory Data Analysis / Data Cleaning / Feature Engineering

We first cleaned the data, conducted exploratory data analysis and feature engineering using the [Real Estate Prediction - Data Cleaning, Exploratory Analysis, & Feature Engineering.ipynb](https://github.com/yamachang/ML-real-estate-prediction/blob/main/Real%20Estate%20Prediction%20-%20Data%20Cleaning%2C%20Exploratory%20Analysis%2C%20%26%20Feature%20Engineering.ipynb). During data cleaning and exploratory data analysis, we utilized various plots to assess distributions, segmentations, correlations, and outliers. Subsequently, we performed the following tasks: dropping unwanted observations, rectifying structural errors, eliminating outliers, and addressing missing data. In terms of feature engineering, we generated new features, grouped sparse classes, and created dummy variables for categorical features.

### Summary Statistics

We did some preliminary analysis and visualizations in order to better understand our data. Below you can see some of those results:

First, we created **histograms** to get to know about the **distributions** and to eye detect if there's any sparse data.

![Plot 1](plots/histogram.png)

Next, we used **box plot** to check the relationship between categorical features and numeric features. In general, it looks like single family homes are more expensive than apartments.

![Plot 2](plots/boxplot.png)

In order to examine the relationship between numeric features and other numeric features, we visualized the **correlation matrix**!

![Plot 3](plots/heatmap.png)

Next, we aimed to perform data cleaning tasks, which involved **grouping sparse data** to mitigate overfitting and **checking for outliers**. 

* **Grouping sparse data**: For categorical features, we reduced the number of items in `exterior_walls` from 16 to 8, and in `roof` from 16 to 5.

![Plot 4](plots/bar-plot-walls.png) 
![Plot 5](plots/bar-plot-roof.png)

* **Checking for outliers**: It looks like `lot_size` has a potential outlier as it has a long and skinny tail, and we decided to remove observations with `lot_size` greater than 500,000 sqft for outliers.

![Plot 6](plots/violin-plot-lotsize.png) 

## 🧵 Predicting House Prices using Regression Models

![Plot 7](plots/model-metrics.png)

## 📍 Takeaways and Next Steps

