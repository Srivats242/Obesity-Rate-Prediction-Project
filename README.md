# Obesity Rate Prediction Using Machine Learning

## Overview

This project uses machine learning to predict obesity rates across countries based on dietary and nutritional factors. It explores relationships between food consumption patterns and obesity prevalence using data preprocessing, exploratory analysis, and regression models.

The dataset contains **15,087 observations across 167 countries**.

## Technologies Used

- **Python** – Data processing and model development
- **Pandas** – Data cleaning and manipulation
- **NumPy** – Numerical operations
- **Scikit-learn** – Machine learning models and evaluation
- **Matplotlib** – Data visualization
- **Jupyter Notebook** – Analysis and experimentation

## Dataset and Features

The project uses global obesity and food supply data from sources including the World Health Organization (WHO) and Food and Agriculture Organization (FAO).

The models use the following features:

- Fat supply
- Daily calorie availability per capita
- Protein supply per capita
- Sugar availability per capita
- Year
- Country (numerically encoded)

The target variable is the **obesity rate**.

## Methodology

1. **Data Preprocessing:** Cleaned and prepared the data, selected relevant features, and encoded country information using LabelEncoder.
2. **Train-Test Split:** Divided the dataset into 80% training data and 20% testing data.
3. **Model Training:** Trained Linear Regression, Decision Tree Regression, and Random Forest Regression models.
4. **Model Evaluation:** Compared model performance using the coefficient of determination (R²).

## Results

The **Random Forest Regression** model achieved the best performance among the evaluated models, with an **R² score of 0.748**.

This indicates that the model explained approximately 74.8% of the variation in obesity rates in the evaluated dataset.

## Key Takeaways

- Gained experience preparing and analyzing real-world datasets.
- Compared multiple regression algorithms to evaluate predictive performance.
- Applied feature encoding, train-test splitting, and model evaluation techniques.
- Explored how dietary and nutritional indicators relate to obesity prevalence.

## Project Purpose

This project demonstrates the application of machine learning and data analysis techniques to a public health problem, with an emphasis on understanding data, building predictive models, and evaluating their results.
