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
