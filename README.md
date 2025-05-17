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

"Age-wise, income peaks during middle age—typically between 30 to 55 years. Younger workers are often in early-career, lower-paying roles, while older workers may reduce hours or shift to retirement."


![Income Distribution by Education Level](graphs/income_distribution_by_education.png)

"There’s a clear correlation between higher education and higher income. Those with Bachelor’s degrees or above are far more likely to earn over $50K, emphasizing the long-term financial returns of investing in education."


![Income Distribution by Workclass](graphs/income_distribution_by_workclass.png)

"Income distribution varies across employment types. Self-employed and federal employees show a stronger presence in the higher-income bracket, while private sector workers mostly earn under $50K. This could point to greater job stability or benefits in public and entrepreneurial roles."


![Income Distribution by Occupation](graphs/income_distribution_by_occupation.png)

"Occupation matters. Executive and managerial roles dominate the over-$50K category, whereas manual labor and service roles are more concentrated under $50K. This reflects the value placed on leadership, decision-making, and specialized skills in the labor market."


![Box Plot of Hours Per Week vs Income](graphs/hours_per_week_vs_income.png)

"Not surprisingly, those who work longer hours tend to earn more. However, this also raises questions about work-life balance, labor intensity, and the diminishing returns of excessive work."


![Income Distribution by Gender](graphs/income_distribution.png)

"Let’s now examine the income distribution across genders. From the data, it’s evident that men are more likely to earn over $50K compared to women. A large proportion of women remain in the under $50K category, despite similar participation in the workforce.While some of the gap is explained by job type or time commitment, the persistent nature of this divide points to the need for deeper equity reforms—like equal pay policies, better parental support systems, and leadership development programs for women."


![Income Distribution by Race](graphs/income_distribution.png)

"Analyzing income distribution by race reveals notable disparities in earnings. White and Asian individuals show a higher proportion of incomes above $50K, while Black, Hispanic, and Native populations are more concentrated in the under $50K category.Addressing these disparities requires both policy-level changes and inclusive corporate practices to ensure fair opportunities and economic mobility for all racial groups."


![Income Distribution by Country](graphs/income_distribution_by_country.png)

"When comparing by native country, U.S.-born individuals lead in higher income representation. Many other countries show a skew toward lower income, possibly due to differences in access, qualifications, or employment types for immigrants."


![Income Distribution by Marital Status](graphs/income_distribution_by_marital_status.png)

"Interestingly, marital status also plays a role. Married individuals, especially those with spouses present, are significantly more represented in the higher income group. This may indicate economic advantages through dual incomes or financial stability."


![Marital Status vs Education](graphs/marital_status_vs_education.png)
![Violin Plot of Age by Marital Status and Gender](graphs/violin_plot_marital_status.png)
![Violin Plot of Age by Education and Gender](graphs/violin_plot_education.png)
![Stacked Bar Plot of Gender by Hours-per-week](graphs/gender_hours_per_week.png)

"There’s a notable gender gap in hours worked. On average, men work longer hours than women, which partially explains income disparities. However, this also ties into deeper systemic factors like childcare, societal roles, and occupational choices."


![Stacked Bar Plot of Race by Hours-per-week](graphs/race_hours_per_week.png)
![Workclass vs Education](graphs/workclass_vs_education.png)
![Occupation vs Education](graphs/occupation_vs_education.png)
![Stacked Bar Plot of Relationship by Marital Status](graphs/marital_status_relationship.png)
![Correlation Heatmap (Numerical Features)](graphs/correlation_heatmap.png)

"Finally, our correlation heatmap confirms that education, hours per week, and age have the strongest positive correlations with income. Meanwhile, factors like gender and marital status also show moderate influence."


![Missing Value Heatmap](graphs/missing_value_heatmap.png)