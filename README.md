People and Occupations Across Time
==================================
An end-to-end data project that profiles two people/occupation datasets, resolves quality issues, merges them into a unified dataset, and delivers an interactive Power BI dashboard with a short user guide.

Highlights
- Modular pandas-based ETL notebook to clean, match, and merge the sources.
- Exploratory analysis in Jupyter plus automated HTML EDA reports.
- Final Power BI report and companion PDF guide for stakeholders.

Repository map
- `dataset/Old datasets/`: raw sources (`dataset1.csv`, `dataset2.csv`).
- `dataset/Resulted datasets/mergedData.csv`: cleaned and merged output from the ETL notebook.
- `Explratory Data Analysis/EDA.ipynb`: exploratory analysis of the raw data.
  - `Automated_EDA_report_for_data1.html` and `Automated_EDA_report_for_data2.html`: auto-generated EDA reports.
- `ETL pipeline/ETL_pipeline.ipynb`: main pipeline (load -> clean -> match -> merge) using pandas/matplotlib.
  - `ETL pipeline/testing_lab.ipynb`: scratchpad for testing data-quality fixes (not the primary pipeline).
- `Dashboards/People_and_occupations_across_time_report.pbix`: Power BI dashboard built on `mergedData.csv`.
  - `Dashboards/User Guide for People_and_occupations_across_time_report.pdf`: quick navigation tips for the dashboard.

Quickstart
1) Environment (Python 3.10+):
   ```bash
   python -m venv .venv
   .\.venv\Scripts\activate
   pip install pandas matplotlib seaborn sweetviz
   ```
2) Explore the data:
   - Run `Explratory Data Analysis/EDA.ipynb` in Jupyter.
   - Optionally open the two HTML EDA reports in a browser for a fast overview.
3) Build the cleaned dataset:
   - Execute `ETL pipeline/ETL_pipeline.ipynb` top-to-bottom. It reads from `dataset/Old datasets/` and writes `dataset/Resulted datasets/mergedData.csv`.
   - Use `ETL pipeline/testing_lab.ipynb` only for reviewing experiments.
4) Review the dashboard:
   - Open `Dashboards/People_and_occupations_across_time_report.pbix` in Power BI Desktop; if prompted, point it to `dataset/Resulted datasets/mergedData.csv`.
   - Refer to the PDF guide for interaction tips.

Deliverables
- Cleaned dataset: `dataset/Resulted datasets/mergedData.csv`
- EDA and matching notes: `Explratory Data Analysis/EDA.ipynb` (+ automated HTML reports)
- ETL and analysis logic: `ETL pipeline/ETL_pipeline.ipynb`
- Final dashboard: `Dashboards/People_and_occupations_across_time_report.pbix`
- Dashboard guide: `Dashboards/User Guide for People_and_occupations_across_time_report.pdf`
