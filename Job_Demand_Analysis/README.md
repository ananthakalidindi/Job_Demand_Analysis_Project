# 💼 Job Demand & Skills Analysis

## 📌 Project Overview

This project analyzes job-market data to identify patterns in job demand, requested skills, salaries, industries, locations, experience levels, and posting trends. The project follows an eight-stage Data Analysis Essentials (DAE) workflow from raw data loading through final results and visualization.

The project is organized so that each stage has its own Jupyter Notebook (`.ipynb`). These notebooks can be opened in **Visual Studio Code with the Jupyter extension** or uploaded to **Google Colab**.

## 🎯 Project Objectives

- Analyze job-demand records and demand scores.
- Identify frequently requested technical skills.
- Study demand across job roles, industries, and locations.
- Analyze annual salary and experience-level patterns.
- Validate and clean missing data.
- Produce summary tables and visualizations.
- Interpret the major findings from the cleaned dataset.
- Provide a reproducible eight-stage analysis workflow.

## 🔄 Project Workflow

### 1. Data Loading & Reading
The original CSV is loaded and examined for structure, data types, and missing values.

### 2. Data Acquisition & Filtering
Records with `Demand_Score >= 70` are selected. Missing values are not removed during this filtering stage.

### 3. Data Extraction
Individual skills are extracted from job postings and counted.

### 4. Data Validation & Cleaning
Rows containing at least one missing value are removed using `dropna()`. The raw dataset contains 1,200 rows and 16 null cells; the cleaned dataset contains 1,184 rows and 0 null cells.

### 5. Data Aggregation & Representation
The cleaned records are summarized by job title, location, and industry.

### 6. Data Analysis
Descriptive statistics, salary-by-job analysis, experience-level demand, and correlation analysis are produced.

### 7. Data Visualization
Eight charts are generated from the cleaned dataset.

### 8. Results & Interpretation
The final findings and metrics are stored in `08_Results_Interpretation/08_results.csv` and reviewed in the Stage 8 notebook.

## 📂 Repository Structure

```text
Job_Demand_Analysis/
│
├── data/
│   └── job_demand_analysis.csv
│
├── 01_Data_Loading_Reading/
│   ├── 01_data_loading.ipynb
│   └── 01_load_data.csv
│
├── 02_Data_Acquisition_Filtering/
│   ├── 02_data_acquisition_filtering.ipynb
│   └── 02_filter_data.csv
│
├── 03_Data_Extraction/
│   ├── 03_data_extraction.ipynb
│   └── 03_extract_skills.csv
│
├── 04_Data_Validation_Cleaning/
│   ├── 04_data_validation_cleaning.ipynb
│   └── 04_clean_data.csv
│
├── 05_Data_Aggregation_Representation/
│   ├── 05_data_aggregation.ipynb
│   └── 05_aggregate_data.csv
│
├── 06_Data_Analysis/
│   ├── 06_data_analysis.ipynb
│   ├── 06_analyze_data.csv
│   ├── descriptive_statistics.csv
│   ├── experience_demand.csv
│   ├── salary_by_job.csv
│   └── correlation_analysis.csv
│
├── 07_Data_Visualization/
│   ├── 07_data_visualization.ipynb
│   └── 8 visualization JPG files
│
├── 08_Results_Interpretation/
│   ├── 08_results.ipynb
│   └── 08_results.csv
│
├── requirements.txt
├── README.md
└── .gitignore
```

## 🛠️ Technologies Used

- **Python 3**
- **Pandas** — data loading, cleaning, transformation, and analysis
- **NumPy** — numerical operations
- **Matplotlib** — visualization
- **Jupyter Notebook / JupyterLab** — notebook execution
- **IPykernel** — Python kernel support for notebooks
- **Visual Studio Code** — notebook editing and execution
- **Google Colab** — cloud notebook execution
- **GitHub** — project version control and sharing

## 📊 Dataset

The project uses `data/job_demand_analysis.csv`.

- **Rows:** 1,200
- **Columns:** 11
- **Initial null cells:** 16

Main columns:

`Job_ID`, `Job_Title`, `Industry`, `Location`, `Experience_Level`, `Education`, `Employment_Type`, `Posting_Year`, `Salary_INR_Annual`, `Demand_Score`, and `Skills`.

The raw file intentionally contains missing values so that the validation and cleaning stage can be demonstrated.

## 🧹 Cleaning Summary

| Stage | Records | Null cells |
|---|---:|---:|
| Raw | 1,200 | 16 |
| Demand-filtered | 84 | 1 |
| Cleaned | 1,184 | 0 |

Stage 4 removes any row containing at least one missing value. No missing values are artificially filled.

## 📈 Visualizations

The Stage 7 notebook produces eight JPG visualizations:

1. Market Demand Radar
2. Top Skills Polar Chart
3. Yearly Job Posting Trend
4. Job Demand by Industry
5. Jobs by Location
6. Salary-Demand Market Map
7. Correlation Matrix
8. Average Salary by Experience

## 🖥️ How to Open and Run in Visual Studio Code

1. Install **Visual Studio Code**.
2. Install the **Python** and **Jupyter** extensions in VS Code.
3. Extract the project ZIP.
4. Open the `Job_Demand_Analysis` folder in VS Code.
5. Open any stage `.ipynb` file.
6. Select a Python kernel when VS Code asks for one.
7. Run the notebook cells from Stage 1 through Stage 8 in numerical order.

Install the project dependencies from the VS Code terminal:

```bash
pip install -r requirements.txt
```

The eight notebooks are located directly inside their corresponding numbered stage folders.

## 🚀 How to Run in Google Colab

1. Upload the project to Google Drive/GitHub or upload the required notebook and data files to Colab.
2. Open the Stage 1 notebook first:
   `01_Data_Loading_Reading/01_data_loading.ipynb`
3. Run the stages in order:
   `01 → 02 → 03 → 04 → 05 → 06 → 07 → 08`
4. Check the generated CSV files and Stage 7 visualizations after execution.
5. Review the final results in Stage 8.

## ▶️ Recommended Execution Order

```text
01_Data_Loading_Reading
        ↓
02_Data_Acquisition_Filtering
        ↓
03_Data_Extraction
        ↓
04_Data_Validation_Cleaning
        ↓
05_Data_Aggregation_Representation
        ↓
06_Data_Analysis
        ↓
07_Data_Visualization
        ↓
08_Results_Interpretation
```

## 📦 Requirements

The `requirements.txt` file contains the packages required to run the notebooks:

```text
pandas
numpy
matplotlib
jupyter
ipykernel
nbformat
nbclient
```

Install them with:

```bash
pip install -r requirements.txt
```

## 📝 Conclusion

This project demonstrates a complete job-demand data-analysis pipeline covering data loading, filtering, extraction, validation, cleaning, aggregation, analysis, visualization, and interpretation. The eight notebooks provide a clear stage-by-stage workflow that can be opened in Visual Studio Code or executed in Google Colab.
