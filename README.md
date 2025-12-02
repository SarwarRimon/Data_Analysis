StackOverflow Developer Survey — Data Analysis
A reproducible exploratory data analysis of the StackOverflow Developer Survey. The analysis explores developer careers, compensation, skills, learning methods, and work preferences.

Project overview
This repository contains a clean, well-documented exploratory analysis of the StackOverflow Developer Survey (public dataset). The main analysis and visualizations are contained in the Jupyter notebook.

Dataset (included)
The survey dataset is included in this repository at: DataAnalysis/Data/survey_results_public.csv

Note: The dataset originates from Stack Overflow Insights (https://insights.stackoverflow.com/survey) and is subject to Stack Overflow's data usage terms.

Project structure
DataAnalysis/

Notebook/
AnalysisNotebook.ipynb # Main analysis and visualizations
Data/
survey_results_public.csv # Included survey data CSV
.gitignore
README.md
Objectives / Research questions
The analysis addresses the following questions (examples):

How does remote work relate to job satisfaction?
Which programming languages are most commonly used?
Which organization sizes tend to offer the highest median salaries?
Are developers with Master’s degrees more likely to be employed?
How does years of professional experience relate to salary?
What are the most common methods developers use to learn to code?
Data cleaning & preprocessing (summary)
Key preprocessing steps performed in the notebook:

Standardized and cleaned column names.
Converted multi-select responses into binary indicator columns for aggregation.
Normalized and cleaned salary values into a numeric form.
Standardized experience columns (e.g., YearsCodePro → YearsCodeProClean).
Converted special values (e.g., "More than 50 years") into numeric where appropriate.
Handled missing values (documented removals and imputations).
All transformations and rationale are documented inline in Notebook/AnalysisNotebook.ipynb.

Visualizations & analysis included
The notebook contains figures and brief interpretations:

Job satisfaction vs. remote work (boxplots / distributions)
Most popular programming languages (bar charts)
Median salary by organization size (grouped comparisons)
Salary vs. years of professional experience (scatter + trend)
Correlation heatmap for numeric variables
Aggregation of learning methods (multi-select analysis)
Additional charts and summary tables are included in the notebook.

How to run (reproducibility)
Clone the repository: git clone https://github.com/SarwarRimon/Data_Analysis.git

Ensure the dataset is present: DataAnalysis/Data/survey_results_public.csv

(Recommended) Create and activate a virtual environment:

macOS / Linux: python -m venv .venv source .venv/bin/activate
Windows (PowerShell): python -m venv .venv ..venv\Scripts\Activate.ps1
Install dependencies: pip install pandas numpy matplotlib seaborn jupyter

Note: Add a requirements.txt or environment.yml if you want pinned versions.

Launch Jupyter and run the notebook: cd DataAnalysis/Notebook jupyter notebook Open AnalysisNotebook.ipynb and run the cells in order.

Reproducibility & outputs
The notebook contains the full preprocessing pipeline for end-to-end reproduction.
Optionally: export final figures and summary CSVs to a results/ directory. I can add notebook cells to save outputs automatically.
Suggested next steps
Add requirements.txt with pinned versions for reproducibility (I can create it).
Export final figures and summary tables to results/ for quick browsing.
Optionally refactor critical data cleaning into scripts and add unit tests.
Notes about repository contents
The repository previously included a data model file for planning; it is not required by the analysis pipeline. Let me know if you want it removed or integrated.
Author & contact
Author: Sarwar Rimon
GitHub: https://github.com/SarwarRimon
