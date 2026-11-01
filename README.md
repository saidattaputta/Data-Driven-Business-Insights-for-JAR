# Data-Driven Business Insights for JAR

A retail business analytics project examining sales, profit, category performance, regional performance, customer segments, and short-horizon sales forecasts. The work combines spreadsheet data preparation, exploratory analysis, time-series analysis, RFM segmentation, clustering, and reporting outputs.

## Business Objective

Turn order-level sales and target data into practical answers to questions such as:

- Which product categories contribute most to sales and profit?
- Where do actual sales differ from targets?
- How do sales evolve over time?
- Which customer groups appear more valuable or need attention?
- What does a short-term sales forecast suggest for planning?

## Data Sources

The repository includes three Excel source workbooks in `data/Raw_Data/`:

- List of orders
- Order details
- Sales targets

The notebooks join and enrich these inputs to create analytical tables and charts.

## Analysis Workflow

| Notebook | Scope |
|---|---|
| `data_prep.ipynb` | Load, clean, join, and prepare order and target data |
| `exploratory_data_analysis.ipynb` | Sales, profit, category, and descriptive analysis |
| `forcasting_and_targets.ipynb` | Time-series decomposition, moving averages, and a three-month forecast / target comparison |
| `regional_and_segment_analysis.ipynb` | Regional summaries, RFM features, customer segmentation, and clustering |

## Deliverables

- Charts in the repository root and `outcome/charts/`
- Analytical tables and model outputs in `outcome/tables/`
- Original input workbooks in `data/Raw_Data/`

The repository currently contains both `outcome/` and `outcomes/` directories. They are documented as present and have intentionally not been renamed or merged.

## Technology

- Python
- pandas and NumPy
- Matplotlib and Seaborn
- scikit-learn (scaling and K-Means)
- statsmodels (time-series decomposition)
- Prophet when available, with a simple growth-based fallback in the forecast notebook
- Jupyter Notebook

## Reproduce the Analysis

```bash
git clone https://github.com/saidattaputta/Data-Driven-Business-Insights-for-JAR.git
cd Data-Driven-Business-Insights-for-JAR
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\\Scripts\\activate
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels openpyxl jupyter
```

Open the notebooks from the repository root and run them in the order shown above. If using the Prophet forecasting path, install Prophet separately. The forecast notebook includes a simpler fallback when Prophet is unavailable.

## Interpretation and Limitations

- Forecasts are exploratory, short-horizon estimates and should be compared with a proper time-based holdout before operational use.
- RFM labels and K-Means clusters depend on the chosen snapshot date, features, and thresholds.
- Profit and margin interpretation depends on the source workbook definitions.
- Some notebook paths refer to generated `data/processed/` and `outputs/` directories, while committed exports use `outcome/`; follow the paths established by the data-preparation notebook when reproducing the full workflow.


---

**Sai Datta Putta**

[LinkedIn](https://www.linkedin.com/in/sai-datta-putta/)
