# Data Cleaning Project
## Objective

The primary goal of this project is to explore, clean, and preprocess raw data by handling issues such as:
- Missing values
- Duplicates
- Inconsistent formatting
- Outliers
- Data type mismatches

By the end of this project, the data is cleaned and ready for downstream tasks like visualization, modeling, or statistical analysis.

---

## Dataset

The dataset used for this project is located inside `dataset.zip` and was extracted before processing. The data was loaded using `pandas` and cleaned as per the quality issues observed during exploration.

---

## Notebook: `data_cleaning.ipynb`

The Jupyter notebook contains:
- Dataset loading and initial inspection
- Summary statistics and data types
- Visualizations for missing values, outliers, and distributions
- Cleaning steps with proper explanations and reasoning
- Final dataset shape and confirmation of clean data

### Visualizations Used:
- Histograms for distribution analysis
- Box plots for outlier detection
- Bar plots for categorical feature exploration
- Heatmaps for correlation analysis
- Missing value heatmap


#### Inferences drawn from graphs
![Box Plot of Capital Gain by Income Group](graphs/income_vs_capital_gain.png)
![Box Plot of Capital Loss by Income Group](graphs/income_vs_capital_loss.png)
![Income Distribution by Age Group](graphs/income_distribution_by_age_group.png)
![Income Distribution by Education Level](graphs/income_distribution_by_education.png)
![Income Distribution by Workclass](graphs/income_distribution_by_workclass.png)
![Income Distribution by Occupation](graphs/income_distribution_by_occupation.png)
![Box Plot of Hours Per Week vs Income](graphs/hours_per_week_vs_income.png)
![Income Distribution by Gender](graphs/income_distribution.png)
![Income Distribution by Race](graphs/income_distribution.png)
![Income Distribution by Country](graphs/income_distribution_by_country.png)
![Income Distribution by Marital Status](graphs/income_distribution_by_marital_status.png)
![Marital Status vs Education](graphs/marital_status_vs_education.png)
![Violin Plot of Age by Marital Status and Gender](graphs/violin_plot_marital_status.png)
![Violin Plot of Age by Education and Gender](graphs/violin_plot_education.png)
![Stacked Bar Plot of Gender by Hours-per-week](graphs/gender_hours_per_week.png)
![Stacked Bar Plot of Race by Hours-per-week](graphs/race_hours_per_week.png)
![Workclass vs Education](graphs/workclass_vs_education.png)
![Occupation vs Education](graphs/occupation_vs_education.png)
![Stacked Bar Plot of Relationship by Marital Status](graphs/marital_status_relationship.png)