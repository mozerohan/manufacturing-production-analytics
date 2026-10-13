
# Manufacturing Production Analytics with Python

## Project Overview

This project analyzes simulated manufacturing production data from a control-transformer manufacturing environment. 
The goal is to understand production trends, product performance, quality issues, defects, and rework using Python.

The project demonstrates a complete exploratory data analysis workflow, from data loading and cleaning to visualization
and business recommendations.

## Business Objectives

- Analyze monthly production trends and rejection rates.
- Compare production volume, rejection rates, and manufacturing time across product types.
- Explore relationships between manufacturing measurements and inspection results.
- Identify frequently recorded defects and rework patterns.
- Translate analytical findings into actionable recommendations.

## Dataset

The dataset contains 3,000 simulated manufacturing records covering January–June 2026.

It includes production dates, product types, manufacturing times, material and cost information, 
inspection measurements, defect categories, and rework information.

**Note:** This is a simulated dataset created for portfolio and learning purposes. 
It does not contain actual company production records.

## Technologies Used

- Python 3.13
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook
- Docker

## Analysis Workflow

1. Load and inspect the dataset.
2. Check data quality and handle missing values.
3. Validate records and investigate outliers.
4. Create date-based and manufacturing-time features.
5. Explore monthly production and rejection rates.
6. Analyze quality measurements and product performance.
7. Investigate correlations, defects, and rework.
8. Summarize findings and recommend areas for further investigation.

## Key Findings

- Monthly production and rejection rates vary over the observation period.
- The 500VA product category has a substantially higher rejection rate than the other analyzed product categories.
- Failed inspections are associated with higher winding temperatures and no-load current, 
  and lower insulation resistance, in this dataset.
- Voltage and winding defects account for high rework counts.
- Rework rates differ across defect categories.

These findings describe patterns in the simulated dataset and should not be interpreted as proof of causation 
or as conclusions about real manufacturing operations.

## Project Structure

```text
Project_01_Manufacturing_Analytics/
├── 01_manufacturing_production_analysis.ipynb
├── manufacturing_production_data.csv
├── requirements.txt
├── Dockerfile
├── .dockerignore
├── .gitignore
└── README.md
```

## Run Locally

Clone the repository, then open a terminal in the project directory.

```bash
python -m venv .venv
```

Activate the environment on Windows:

```powershell
.venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
python -m pip install -r requirements.txt
```

Launch Jupyter:

```bash
jupyter notebook
```

Open `01_manufacturing_production_analysis.ipynb` and run the notebook cells.

## Run with Docker

Build the image:

```bash
docker build -t manufacturing-production-analytics .
```

Start the container:

```bash
docker run --rm -p 8888:8888 manufacturing-production-analytics
```

Then open the Jupyter URL in your browser at `http://localhost:8888` and use the configured token:

`portfolio-project`

## Limitations

- The dataset is simulated and may not reflect real-world manufacturing distributions.
- Observed relationships are exploratory and do not establish causation.
- Further investigation with real production records would be needed before implementing operational changes.

## Future Improvements

- Add automated data-quality checks.
- Build a production and quality dashboard.
- Add tests for data validation and analytical calculations.
- Explore a machine-learning approach to identify potential quality risks.

## Author

Created as part of a practical Python and data analytics portfolio.


