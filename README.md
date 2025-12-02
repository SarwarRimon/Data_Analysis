StackOverflow Developer Survey — Data Analysis
A reproducible exploratory data analysis of the StackOverflow Developer Survey that explores developer careers, compensation, skills, learning methods, and work preferences.

Project overview
This repository contains a clean, well-documented exploratory analysis of the StackOverflow Developer Survey (public dataset). The analysis focuses on trends in salaries, experience, remote work and job satisfaction, popular languages and tools, learning methods, and employment patterns by education level and organization size. The work is implemented in a Jupyter Notebook and includes data cleaning, transformation, and visualizations.

Dataset (included)
The survey dataset is included in this repository. Place (or verify) the CSV at this path:

DataAnalysis/Data/survey_results_public.csv
Note: The dataset originates from Stack Overflow Insights (https://insights.stackoverflow.com/survey) and is subject to the data usage terms provided by Stack Overflow. If you prefer the dataset not be stored in the repo, I can remove it and instead provide instructions to download it locally.

Project structure
DataAnalysis/
Notebook/
AnalysisNotebook.ipynb # Main analysis and visualizations
Data/
survey_results_public.csv # Included survey data CSV
.gitignore
README.md
Objectives
The analysis addresses the following research questions:

How does remote work relate to job satisfaction?
Which programming languages are most commonly used by respondents?
Which organization sizes tend to offer the highest median salaries?
Are developers with Master’s degrees more likely to be employed than those without?
How does years of professional experience relate to salary?
Which tools, platforms, and databases do developers admire most?
What are the most common methods developers use to learn to code?
Data cleaning & preprocessing
Key preprocessing operations performed in the notebook:

Standardized and cleaned column names for readability.
Converted multi-select responses into binary indicator columns for aggregation.
Normalized and cleaned salary values (converted to a common numeric form).
Standardized experience columns (e.g., YearsCodePro → YearsCodeProClean).
Converted special string values (e.g., "More than 50 years") to numeric where appropriate.
Handled missing values (documented removals and imputations).
Ensured correct dtypes for columns used in analysis.
All transformations and the rationale for decisions are documented inline in AnalysisNotebook.ipynb.

Visualizations and analyses included
The notebook contains the following figures and analyses (each with brief interpretation text):

Job satisfaction vs. remote work (boxplots / distribution comparisons)
Most popular programming languages (bar charts)
Median salary by organization size (grouped comparisons)
Salary vs. years of professional experience (scatter plot + trendline / binned medians)
Correlation heatmap for numeric variables (experience, salary, job satisfaction)
Aggregation of learning methods used by respondents (multi-select analysis)
Additional exploratory charts and summary tables
If you want the notebook to export figures to a results/ folder automatically, I can add that.

How to run
Clone the repository: git clone https://github.com/SarwarRimon/Data_Analysis.git

Ensure the dataset is present: DataAnalysis/Data/survey_results_public.csv

(Recommended) Create and activate a virtual environment: python -m venv .venv source .venv/bin/activate # macOS / Linux ..venv\Scripts\activate # Windows PowerShell

Install dependencies: pip install pandas numpy matplotlib seaborn jupyter

If you prefer, I can add a requirements.txt with pinned versions.

Launch Jupyter and run the notebook: cd DataAnalysis/Notebook jupyter notebook Open AnalysisNotebook.ipynb and run the cells in order.

Reproducibility & outputs
The notebook contains the full preprocessing pipeline, so others can reproduce the analysis end-to-end given the CSV.
Consider adding a requirements.txt or environment.yml to fully fix package versions. I can generate one based on the environment you used.
If you’d like, I can add notebook cells to save final figures and summary CSVs into a results/ directory.
Notes about repository contents
The repository previously included a data model file for planning; it is not required by the analysis pipeline. Let me know if you want it removed or integrated into preprocessing.
Dataset is included in DataAnalysis/Data/ as requested. If you used Git LFS for a large file, confirm that collaborators will have LFS enabled when cloning.
Suggested next steps
Add requirements.txt with pinned versions for reproducibility.
Add a concise "Key findings" section to this README summarizing the most important takeaways from the notebook (I can draft this if you provide the top 4–6 findings you want highlighted).
Optionally export figures and summary tables to a results/ directory for quick browsing without opening the notebook.
If desired, add unit tests for critical data cleaning functions (if they are refactored into scripts).
Author & contact
Author: Sarwar Rimon
GitHub: https://github.com/SarwarRimon
