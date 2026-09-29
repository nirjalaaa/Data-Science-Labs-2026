# Predicting Online Shopper Purchase Intention

## Business Problem

How can an e-commerce business predict whether a website visitor is likely to make a purchase?

## Business Objective

The objective of this project is to analyze online shopping session data and build machine learning models that can predict whether a website visitor will make a purchase.

This can help an e-commerce business understand customer behavior and identify patterns associated with purchasing activity.

## Dataset

This project uses the **Online Shoppers Purchasing Intention Dataset** from the UCI Machine Learning Repository.

* Original records: **12,330**
* Original features: **18 columns**
* Duplicate records removed: **125**
* Records used for analysis: **12,205**
* Target variable: **Revenue**

  * `False` = No Purchase
  * `True` = Purchase

## Technologies Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

## Project Steps

### 1. Data Cleaning

* Loaded the dataset using Pandas
* Checked the dataset structure
* Checked for missing values
* Checked for duplicate records
* Removed duplicate records

### 2. Exploratory Data Analysis

The project analyzed:

* Purchase vs. no-purchase sessions
* Visitor types
* Product-related page views
* Time spent on product-related pages
* PageValues
* Weekend vs. weekday purchasing
* Monthly purchase rates

### 3. Data Preparation

* Separated features and target variable
* Converted categorical variables into numerical variables
* Converted the `Revenue` target into 0 and 1
* Split the dataset into training and testing sets
* Used stratified sampling to preserve the target distribution

### 4. Machine Learning Models

Three classification models were tested:

1. Logistic Regression
2. Decision Tree
3. Random Forest

## Model Results

| Model               | Accuracy | Purchase Precision | Purchase Recall | Purchase F1 |
| ------------------- | -------: | -----------------: | --------------: | ----------: |
| Logistic Regression |   87.01% |               0.56 |            0.75 |        0.65 |
| Decision Tree       |   86.24% |               0.56 |            0.55 |        0.56 |
| Random Forest       |   90.05% |               0.74 |            0.55 |        0.64 |

The models show different performance characteristics. Random Forest achieved the highest overall accuracy in this experiment, while Logistic Regression identified a larger proportion of actual purchasing sessions through its higher purchase recall.

## Business Insights

* **15.63%** of shopping sessions resulted in a purchase.
* **New visitors** had a purchase rate of **24.93%**, compared with **14.09%** for returning visitors.
* Purchasing visitors viewed an average of **48.21 product-related pages**, compared with **29.05** for non-purchasing visitors.
* Purchasing visitors spent an average of **1876.21** on product-related page duration, compared with **1082.98** for non-purchasing visitors.
* The average **PageValues** was **27.26** for purchasing sessions and **2.00** for non-purchasing sessions.
* The purchase rate was **17.45% on weekends** and **15.08% on weekdays**.
* Among the months available in the dataset, **November** had the highest purchase rate at **25.49%**.
* **PageValues** was the most important feature in the Random Forest model, followed by **ExitRates**, **ProductRelated_Duration**, and **ProductRelated**.

These findings describe patterns in the dataset and should not be interpreted as proof that one factor directly causes a purchase.

## Conclusion

This project demonstrates how data analysis and machine learning can be used to understand online shopping behavior and predict purchase outcomes.

The analysis found differences between purchasing and non-purchasing sessions in areas such as product-page activity, time spent on product pages, and PageValues.

Three machine learning models were evaluated using accuracy, precision, recall, and F1-score. The results show why multiple evaluation metrics are useful when assessing a classification problem.

## Project Files

```text
Assignment_1/
├── Assignment_1.ipynb
├── online_shoppers_intention.csv
└── README.md
```

## How to Run

1. Download or clone this repository.
2. Open `Assignment_1.ipynb` using Jupyter Notebook or JupyterLab.
3. Make sure `online_shoppers_intention.csv` is in the same folder as the notebook.
4. Run the notebook cells from top to bottom.

## Dataset Source

UCI Machine Learning Repository — Online Shoppers Purchasing Intention Dataset.
