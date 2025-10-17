# Big Data Analysis in R: Practical Assignments

This repository contains a series of practical assignments focused on analyzing large datasets using the R programming language. The project's goal is to demonstrate a complete data analysis workflow, from loading and cleaning data to building predictive models and interpreting their results.

---

## 🚀 Core Concepts Covered

In these practical assignments, you will find examples of the following techniques and approaches:

* **Data Loading and Processing**: Efficiently handling large files (e.g., `.parquet` format) using the `arrow` library.
* **Data Cleaning and Transformation**: Applying logical filters, handling missing values, and removing outliers with `dplyr`.
* **Feature Engineering**: Creating new, informative features from existing data (e.g., extracting the hour of the day or day of the week from a timestamp).
* **Exploratory Data Analysis (EDA)**: Visualizing distributions, variable relationships, and correlations to better understand the data using `ggplot2` and `corrplot`.
* **Statistical Modeling**: Building and evaluating machine learning models, specifically linear regression (`lm`), to predict a target variable.
* **Model Diagnostics**: Checking model assumptions (linearity, normality of residuals) to assess its reliability.
* **Report Generation**: Formatting the analysis into professional reports using Quarto.

---

## 📂 Repository Structure

* **/Data**: A directory for storing the source datasets.
* **/Reports**: A directory containing practical assignments formatted as Quarto documents.
* **Practice01.qmd**: The first practical assignment focused on predicting NYC taxi fare amounts.
* **Practice02.qmd**: The second practical assignment (to be added).
* `README.md`: This file, which describes the repository.

---

## 🛠️ Technologies Used

* **Programming Language**: R
* **IDE**: VS Code
* **Data Format**: Parquet for efficient storage and retrieval of large datasets.
* **Reporting Format**: Quarto
* **Key R Libraries**:
    * `tidyverse` (including `dplyr`, `ggplot2`, `readr`) for data manipulation and visualization.
    * `arrow` for high-performance reading of Parquet files.
    * `corrplot` for creating correlation matrices.
    * `broom` for tidying model output into data frames.

---

## 📖 Projects

### Practice Assignment 01: Predicting NYC Taxi Fare Amount

* **Description**: This assignment involves analyzing a dataset of NYC Yellow Taxi trips from January 2025. The primary objective is to build a linear regression model to predict the total fare (`total_amount`) of a trip. 
* **Key Findings**: The analysis confirmed that **trip distance** is the most crucial predictor of the fare. The final model, which also accounts for factors like passenger count, payment method, and time of day, successfully explains approximately **90.7%** of the variance in the total trip cost.

### Practice Assignment 02: Model Diagnostics and Improvement

* **Description**: This assignment builds directly on the first. It focuses on the critical process of model validation. The baseline model from Practice 01 is subjected to a rigorous diagnostic analysis, which reveals violations of key linear regression assumptions (e.g., non-linearity and heteroscedasticity). The model is then improved by applying a log-log transformation to the skewed variables. 
* **Key Findings**: The analysis demonstrated that a high R-squared is not enough to guarantee a good model. By applying a **log-log transformation**, a new model was created that better satisfies the assumptions of linear regression, making it more statistically robust and reliable. This improved model explains **85.7%** of the variance in the log-transformed total fare and provides a more accurate understanding of the relationships between the predictors and the taxi fare.