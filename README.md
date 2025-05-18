<!-- # To Do
- Create a conda environment to store the packages
- Unzip the data (use !unzip on terminal or use python package zipfile)
- Load the data into a pandas dataframe
- Clean the data (up to your discretion)
- Work solo or in pairs
- Ensure that your code is well commented
- Create a jupyter notebook to document your work
- Create a README file to explain your project, your process, and your findings
- Create a requirements.txt file to document the packages you used
- Create a .gitignore file to ignore the data files
- Create a branch for your project on this repository

The best project will be merged into the main branch for showcase! Good luck! -->

# Data Cleaning and Visualization Project

## Project Overview
This project focuses on exploring, cleaning, and preprocessing a raw dataset to prepare it for further analysis, modeling, or visualization. The dataset contains demographic and income information, including features like age, workclass, education, occupation, capital gains and losses, and more.

The main objectives are:
- Handle missing values and inconsistencies
- Remove duplicates
- Fix data formatting issues
- Detect and handle outliers
- Convert data to correct types
- Generate insightful visualizations to understand patterns in the data

---

## Data Cleaning Process

1. **Handling Missing Values:**
   - Rows with missing or unknown values (`?`) were removed to ensure clean data.
   - For categorical columns like `workclass` and `occupation`, missing values were replaced with 'Unknown' before dropping remaining nulls.
   
2. **Removing Duplicates:**
   - Duplicate rows were identified and dropped to avoid bias.

3. **Standardizing Text Columns:**
   - All categorical text fields were stripped of whitespace and converted to lowercase for consistency.

4. **Converting Data Types:**
   - Numeric columns such as `age`, `fnlwgt`, `education.num`, `capital.gain`, `capital.loss`, and `hours.per.week` were explicitly converted to numeric types.
   - Rows that became invalid during conversion were dropped.

5. **Feature Engineering:**
   - Created a new column `net.capital` as the difference between `capital.gain` and `capital.loss`.

6. **Exporting Clean Data:**
   - The cleaned dataset was saved as `cleaned_data.csv` for downstream tasks.

---

## Data Visualization

- Various plots were created using Matplotlib and Seaborn to explore relationships and distributions in the data.
- All graphs are saved in the `graphs/` directory.

---

## How to Run

1. Clone the repository.  
2. **Using Conda environment (recommended):**

    ```bash
    conda env create -f environment.yml
    conda activate my_env  # replace my_env with your env name
    python your_script.py  # run your cleaning and visualization scripts

3. Run the cleaning and visualization scripts.  
4. View the output graphs inside the `graphs/` folder.  

---

## Implications and Findings
### Age vs Income
![Age vs Income](graphs/age_vs_income.png)
- The median age is higher for the >50k group compared to the <=50k group.
- The interquartile range (IQR), is also higher for the >50k group, indicating that higher earners tend to be older on average.
- There are more outliers (older individuals) in the <=50k group, suggesting that while most high earners are older, some older individuals still earn less.

### Education vs Income
![Education vs Income](graphs/education_vs_income.png)
- Higher education levels are associated with higher income brackets.
- The median education level is higher for the >50k group compared to the <=50k group.
- Some education levels (e.g., hs-grad, some-college) have a very large number of entries, while others like preschool, 1st-4th, and doctorate have very few.

### Occupation vs Income
![Occupation vs Income](graphs/occupation_vs_income.png)
- For every occupation, the number of people earning <=50k (blue bars) is higher than those earning >50k (orange bars).
- Managerial and professional-specialty occupations have the highest counts of high earners (>50k), but even in these categories, low earners (<=50k) outnumber high earners.
- Certain occupations (e.g., handlers-cleaners, machine-op-inspct, farming-fishing, transport-moving, priv-house-serv) have very few high earners (>50k), indicating these roles are predominantly lower-income.
- Some categories, like armed-forces and priv-house-serv, have very low counts overall, which may suggest limited data or rare occupations in the dataset.
- The "unknown" category has a substantial number of entries, which could indicate missing or unclassified occupation data.

### Marital Status vs Income
![Marital Status vs Income](graphs/marital_status_vs_income.png)
- Across all marital status categories, the number of people earning <=50k (blue bars) is higher than those earning >50k (orange bars).
- The "married-civ-spouse" group stands out: it has a large number of both low and high earners, but the count of high earners (>50k) is much higher here than in any other group.
- "Never-married" individuals are overwhelmingly low earners, with very few earning >50k.
- Marital status is a strong indicator of income. Being a "married-civ-spouse" is associated with a much higher likelihood of earning >50k compared to other groups.
- There is a significant class imbalance in most marital status categories, with the majority earning <=50k. This may affect model performance and should be considered during model development (e.g., using class weighting or resampling).

### Native Country vs Income
![Native Country vs Income](graphs/country_vs_income_top10.png)
- The vast majority of individuals in the dataset are from the United States, with a much smaller representation from other countries.
- High earners from countries other than the United States are extremely rare or nearly absent in the dataset.
- For most countries, the income distribution is almost entirely in the <=50k category. This suggests that "native country" may not be a strong predictor of high income except for distinguishing the United States from other countries.
- Strong imbalance affects the usefulness of "native country" as a predictive feature and should be carefully handled in modeling and interpretation.

### Hours per Week vs Income
![Hours per Week vs Income](graphs/hours_vs_income.png)
- There is a clear positive relationship: those who work more hours per week are more likely to earn >50k.
- This suggests "hours per week" is an important feature for predicting income.
- The presence of many outliers (especially at the extremes) may indicate data entry errors, unusual work patterns, or exceptional cases (e.g., multiple jobs, underreporting/overreporting).

### Sex vs Income
![Sex vs Income](graphs/sex_vs_income.png)
- The income distribution is heavily skewed by sex: a larger proportion of men earn >50k compared to women.
- This suggests that gender may be an important factor in predicting income.

### Race vs Income
![Race vs Income](graphs/race_vs_income.png)
- The majority of individuals in the dataset are classified as "white," with both low earners (<=50k) and high earners (>50k) present in this group. However, low earners far outnumber high earners.
- For all other racial groups ("black," "asian-pac-islander," "other," "amer-indian-eskimo"), the number of individuals is much lower compared to the "white" group.
- "Race" as a feature may have limited predictive power for income in this dataset, except possibly for distinguishing the "white" group due to its size.

### Conclusion
- The dataset contains a wealth of information that can be used to predict income.
- Key features include age, education, occupation, marital status, and hours worked per week.
- The visualizations provide insights into the relationships between these features and income, highlighting potential areas for further analysis or modeling.