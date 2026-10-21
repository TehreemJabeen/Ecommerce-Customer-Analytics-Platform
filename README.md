# E-Commerce Customer Analytics Platform

An exploratory analytics project built around the Online Retail transaction dataset. The notebooks prepare and explore transaction data, derive customer-level features, and evaluate customer segmentation approaches. The analysis also includes sales, product, geographic, and time-based visualizations.

## Analysis workflow

Run the notebooks in this general order:

1. `notebooks/data_preparation.ipynb` — data preparation experiments.
2. `notebooks/01_eda.ipynb` — exploratory data analysis.
3. `notebooks/02_feature_engineering.ipynb` — customer features, including RFM-related analysis.
4. `notebooks/optimal_k.ipynb` — explore candidate cluster counts.
5. `notebooks/clustering_models.ipynb` — compare clustering methods and examine customer segments.

`Untitled.ipynb` and `Untitled1.ipynb` are additional notebooks whose purpose may need review.

## Repository layout

| Folder | Purpose |
| --- | --- |
| `data/` | Transaction dataset used for analysis. |
| `notebooks/` | Jupyter notebooks and some generated analysis files. |
| `outputs/` | Exported charts and analysis results. |
| `models/` | Model-related artifacts and comparison results. |
| `docs/` | Supporting analysis data currently stored in CSV files. |
| `app/`, `src/`, `scripts/`, `processed/`, `visualizations/`, `tests/` | Project folders reserved for application code, reusable modules, processing, and validation. |

Some generated files and data are currently present in more than one folder. Refer to the notebook's input and output paths when running it, and avoid treating duplicate copies as separate sources of truth.

## Getting started

Use Python and install the packages listed in `requirements.txt`:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

Launch Jupyter:

```powershell
jupyter notebook
```

Open a notebook from `notebooks/` and run its cells in order. The source workbook is `data/online_retail.xlsx`; some notebooks may expect a copy in the notebook's working directory, so check their data-loading cell if the file is not found.

## Data and generated files

The project uses the Online Retail spreadsheet (`.xlsx`). Notebooks may create intermediate CSV files, clustering results, model files, and chart images. Their exact names and output paths can vary by notebook; inspect the relevant notebook before rerunning cells that write files.

## Dependencies

See `requirements.txt` for pinned data analysis, machine learning, visualization, and Jupyter dependencies.
