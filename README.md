Obesity Rate Prediction Using Machine Learning
Overview
This project explores the relationship between dietary indicators and adult obesity prevalence across countries. Using publicly available global health and food supply data, we cleaned and combined multiple datasets, performed exploratory data analysis, and compared regression models for predicting obesity rates.

The research focuses on fat supply, calorie availability, protein supply, and sugar availability, alongside country and year. These are observational data, so the models identify predictive relationships rather than proving that dietary changes cause changes in obesity.
Technologies
- Python, Jupyter Notebook
- Pandas and NumPy for data preparation
- Matplotlib and Seaborn for visualization
- SciPy for statistical analysis
- Scikit-learn for preprocessing, regression models, and evaluation
Data Sources
- World Health Organization (WHO), Global Health Observatory: adult obesity prevalence by country and year
- Food and Agriculture Organization (FAO), Food Balance Sheets: calorie, protein, and sugar supply indicators
- FAO via Our World in Data: daily per-capita fat supply
The final modeling dataset used in the notebook contains 1,936 country-year observations from 154 countries (2010–2022).
Features
Feature	Description
Fat_Supply	Daily fat supply per capita
Calories_kcal_per_capita	Daily calorie availability per capita
Protein_g_per_capita	Daily protein supply per capita
Sugar_kcal_per_capita	Daily calories supplied from sugar
Year	Observation year
Country_Encoded	Country encoded numerically using LabelEncoder


Prediction target: Obesity_Rate, the adult obesity prevalence percentage.
Approach
1. Data exploration: Inspected the WHO, FAO, and fat-supply datasets, including missing values, distributions, and relationships between variables.
2. Data cleaning: Selected relevant fields, removed unusable or incomplete records, and standardized country/year information for merging.
3. Feature preparation: Used a cleaned merged dataset and encoded countries numerically.
4. Training and testing: Split the modeling data into 80% training and 20% testing (random_state=42).
5. Model comparison: Trained Random Forest, Decision Tree, and Linear Regression models, evaluating each with R², RMSE, and MAE.
Model Results
Results shown in the uploaded notebook:
Model	R²	RMSE (percentage points)	MAE (percentage points)
Random Forest Regression	0.8295	4.4603	3.0033
Decision Tree Regression	0.5592	7.1724	5.2005
Linear Regression	0.3530	8.6900	6.2420


Random Forest performed best on the notebook's test split. The implementation uses 100 trees, a maximum depth of 10, and random_state=42.

The Random Forest feature-importance analysis assigned the largest importances to fat supply (0.4198) and sugar availability (0.2114). Feature importance reflects the fitted model's predictive behavior, not a causal effect.
Running the Notebook
1. Clone this repository and open the project in Jupyter Notebook or JupyterLab.
2. Install the Python packages used in the notebook:
   pip install pandas numpy matplotlib seaborn scipy scikit-learn jupyter
3. Ensure the input CSV files are available at the paths referenced by the notebook:
   Datasets/
   ├── Prevalence_of_obesity_among_adults_WHO.csv
   ├── daily-per-capita-fat-supply.csv
   └── FoodBalanceSheets_E_All_Data.csv
4. The modeling section also loads merged_data_cleaned.csv. Ensure this prepared file is available in the notebook's working directory, or adjust the notebook to generate it from the source data before running that section.
5. Run the notebook cells in order, adjusting file paths if necessary.
Note: The source CSVs and prepared merged CSV are referenced by the notebook. Their availability in the GitHub repository has not been verified here.
Key Learnings
- Combining and cleaning data from multiple public sources
- Exploratory data analysis and visualization
- Feature encoding and regression modeling with Scikit-learn
- Comparing models using R², RMSE, and MAE
- Interpreting model feature importance while distinguishing correlation from causation
Contributors
This project was developed as a team project by Nischal Kharel, Fernando Seanez, and Srivats Pulumati.
