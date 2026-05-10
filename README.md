# synent-task1-datacleaning-beshoynashaat
Titanic Dataset - Data Cleaning Task
This project focuses on the initial data cleaning and preprocessing of the Titanic dataset to ensure it is ready for exploratory data analysis (EDA) or machine learning modeling.

1. Problem Statement
Raw data is rarely clean. In the case of the Titanic dataset, the data contains missing values (nulls), redundant rows (duplicates), and column names that are not immediately intuitive. The goal of this task is to perform essential data cleaning steps to improve data quality and consistency.

2. Dataset Details
The script utilizes the Titanic dataset, loaded directly from the seaborn library.

Source: sns.load_dataset('titanic').

Key Features: Includes passenger information such as age, sex, class, survival status, and embarkation details.

Initial State: The dataset starts with several missing values in the age, deck, and embark_town columns.

3. Approach
The script follows a systematic approach to refine the data:

Handling Missing Values
Imputation: Missing values in the age column are filled using the median to avoid the influence of outliers.

Dropping Features: The deck column is removed entirely because it contains too many missing values to be useful for analysis.

Mode Imputation: For categorical data like embarked and embark_town, missing values are filled with the mode (the most frequent value).

Data Integrity & Refinement
Duplicate Removal: The script identifies and removes duplicate rows to prevent bias in future analysis.

Type Casting: The survived column is explicitly converted to an integer format.

Feature Renaming: Several columns are renamed for better clarity:

pclass → passenger_class

sibsp → siblings_spouses

parch → parents_children

4. Results
Null Count: Successfully reduced missing values to zero across all remaining columns.

Dimensionality: Adjusted the dataframe by dropping the deck column and removing duplicate rows.

Readability: The final dataframe features descriptive column names and consistent data types, making it ready for downstream tasks.

How to Run
Ensure you have pandas and seaborn installed: pip install pandas seaborn.

Execute the script: python synent_task1_datacleaning_beshoynashaat.py.
