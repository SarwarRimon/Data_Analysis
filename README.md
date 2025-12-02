# Stack Overflow Developer Survey — Data Analysis

A reproducible exploratory data analysis of the Stack Overflow Developer Survey. This repository analyzes developer careers, compensation, skills, learning methods, and work preferences using the public survey dataset.

- Author: Sarwar Rimon — https://github.com/SarwarRimon

Badges
- (Add CI / Binder / license badges here if you enable them)

Table of contents
1. Project overview
2. Repository structure
3. Dataset
4. Quick start
5. Reproducibility (environment)
6. Notebooks & scripts
7. Results & visualizations
8. Suggested next steps
9. Contributing
10. License & data usage
11. Contact

1. Project overview
This repository contains a documented exploratory analysis of the Stack Overflow Developer Survey. The analysis covers:
- Job satisfaction and remote work patterns
- Popular programming languages
- Median salary by organization size and years of experience
- Learning methods and multi-select analysis
- Data cleaning and preprocessing steps with rationale

2. Repository structure
(Adjust these paths to match the actual repo layout if needed.)
```
DataAnalysis/
├── Notebook/
│   └── AnalysisNotebook.ipynb        # Main analysis and visualizations
├── Data/
│   └── survey_results_public.csv     # Survey data CSV (included or linked)
├── results/                          # (optional) exported figures and tables
├── .gitignore
├── README.md
└── requirements.txt or environment.yml
```

3. Dataset
- Location (in repo): DataAnalysis/Data/survey_results_public.csv
- Source: Stack Overflow Insights — https://insights.stackoverflow.com/survey
- Usage: This dataset is subject to Stack Overflow's data usage terms. Ensure you comply with those terms when redistributing or publishing derived data.

4. Quick start
Clone the repository:
```
git clone https://github.com/SarwarRimon/Data_Analysis.git
cd DataAnalysis/Notebook
```

Create and activate a virtual environment (recommended):
- macOS / Linux:
```
python -m venv .venv
source .venv/bin/activate
```
- Windows (PowerShell):
```
python -m venv .venv
.venv\Scripts\Activate.ps1
```

Install dependencies:
```
pip install -r ../requirements.txt
```
If you don't have a requirements file, install the basics:
```
pip install pandas numpy matplotlib seaborn jupyter
```

Run the notebook:
```
jupyter notebook AnalysisNotebook.ipynb
```
Run cells in order (the notebook documents the pipeline).

5. Reproducibility (environment)
- Add a pinned requirements.txt or an environment.yml for exact package versions (recommended).
- Optionally add a Binder badge or Dockerfile to make the notebook runnable online.
- Consider adding a GitHub Actions workflow to run linting or notebook checks on push.

6. Notebooks & scripts
- Notebook/AnalysisNotebook.ipynb: main analysis, data cleaning steps, and visualizations.
- Consider extracting core preprocessing steps into scripts (scripts/clean_data.py) so they can be unit-tested.

Data cleaning summary (as implemented in the notebook)
- Standardized column names
- Converted multi-select responses into binary indicator columns
- Cleaned and normalized salary into numeric form
- Standardized experience columns (e.g., YearsCodePro → YearsCodeProClean)
- Converted special string values (e.g., "More than 50 years") to numeric
- Documented handling of missing values

7. Results & visualizations
The notebook includes:
- Job satisfaction vs. remote work (boxplots / distributions)
- Most popular programming languages (bar charts)
- Median salary by organization size (grouped comparisons)
- Salary vs. years of professional experience (scatter + trend)
- Correlation heatmap for numeric variables
- Aggregation of learning methods (multi-select analysis)

Tip: Export final figures and summary CSVs into results/ for quick browsing and to include in the README.

8. Suggested next steps
- Add a requirements.txt or environment.yml with pinned versions
- Export sample figures into results/ and show them in README
- Add a LICENSE file for your code and a clear note on dataset license
- Refactor critical cleaning to scripts and add simple unit tests
- Add a Binder link / Dockerfile to allow reproducible execution

9. Contributing
Contributions welcome. Suggested workflow:
- Fork repo
- Create a feature branch named feature/<short-description>
- Open a PR with a clear description of changes and any associated notebooks or outputs

10. License & data usage
- Add a LICENSE file for this repository (e.g., MIT, Apache 2.0) — choose one that fits your intentions.
- Data from Stack Overflow Insights is subject to their terms. Include a short data license/citation line, and link to the original survey page.

11. Contact
Author: Sarwar Rimon — https://github.com/SarwarRimon

Acknowledgements
- Stack Overflow for providing the public survey dataset.
