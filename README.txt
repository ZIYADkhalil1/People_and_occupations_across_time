People and Occupations Across Time
==================================
End-to-end analysis that explores two people/occupation datasets, resolves quality issues, merges them into a unified view, and publishes an interactive Power BI dashboard.

Repository layout
- `dataset/Old datasets/`: the two provided sources (`dataset1.csv`, `dataset2.csv`).
- `dataset/Resulted datasets/mergedData.csv`: cleaned and merged dataset produced by the ETL notebook.
- `Explratory Data Analysis/EDA.ipynb`: exploratory analysis of the raw data (data types, distributions, and quality checks).
  - `Automated_EDA_report_for_data1.html` and `Automated_EDA_report_for_data2.html`: auto-generated EDA reports you can open in a browser.
- `ETL pipeline/ETL_pipeline.ipynb`: main modular pipeline that loads, cleans, matches, and merges the two datasets using pandas/matplotlib.
  - `ETL pipeline/testing_lab.ipynb`: scratchpad used to experiment with data-quality fixes (not the main pipeline).
- `Dashboards/People_and_occupations_across_time_report.pbix`: final Power BI dashboard built on `mergedData.csv`.
  - `Dashboards/User Guide for People_and_occupations_across_time_report.pdf`: short guide for navigating the dashboard.

Working locally
1) Set up Python (tested with 3.10):
   - `python -m venv .venv` then `.\.venv\Scripts\activate`
   - `pip install pandas matplotlib seaborn sweetviz`
2) Explore the raw data:
   - Open `Explratory Data Analysis/EDA.ipynb` in Jupyter and run the cells.
   - Optional: open the two HTML reports in a browser for a quick automated overview.
3) Build the cleaned dataset:
   - Run `ETL pipeline/ETL_pipeline.ipynb` top-to-bottom. It reads from `dataset/Old datasets/` and writes `dataset/Resulted datasets/mergedData.csv`.
   - Use `ETL pipeline/testing_lab.ipynb` only if you want to review the intermediate testing of cleaning/matching logic.
4) Review the dashboard:
   - Open `Dashboards/People_and_occupations_across_time_report.pbix` in Power BI Desktop and point it at `mergedData.csv` if prompted.
   - See the accompanying PDF for interaction tips and key visuals.

Deliverables and references
- Cleaned and merged data: `dataset/Resulted datasets/mergedData.csv`
- EDA and matching notes: `Explratory Data Analysis/EDA.ipynb` (+ automated HTML reports)
- Analysis and ETL logic: `ETL pipeline/ETL_pipeline.ipynb`
- Final dashboard and guide: `Dashboards/People_and_occupations_across_time_report.pbix` + `Dashboards/User Guide for People_and_occupations_across_time_report.pdf`
