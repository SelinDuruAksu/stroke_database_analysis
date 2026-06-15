# stroke_database_analysis
Contains a Python-based Exploratory Data Analysis (EDA) pipeline analyzing patient data for stroke prediction. The notebook contains data cleaning, missing value handling, and statistical visualization.

---

### Project Overview

The project processes clinical and demographic variables. 

**Operations performed in the notebook:**
* Exploratory Data Analysis (EDA)
* Missing Value Imputation
* Outlier Detection (IQR and Z-Score methods)
* Statistical Visualizations
* Pandas querying and aggregation

---

### Dataset Information

The dataset is sourced from Kaggle. 

* **Source:** [Stroke Prediction Dataset (Kaggle)](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset?hl=en-EN)
* **Target Variable:** `stroke` (Binary: 1 for stroke, 0 for no stroke)
* **File Name:** `healthcare-dataset-stroke-data.csv`

---

### Methodology & Workflow

| Phase | Description | Libraries Used |
| :--- | :--- | :--- |
| **Data Cleaning** | Removal of the `id` column. Filtering of the "Other" gender category due to insufficient data (1 row). | `pandas`, `numpy` |
| **Missing Values** | Imputation of missing `bmi` values using the median. | `pandas` |
| **Outlier Handling** | IQR method tested on `avg_glucose_level`. Z-Score method (boundary of -4 to 4) applied to `bmi`. Analysis notes the impact of outlier removal on the positive stroke class. | `scipy.stats` |
| **Visualization** | Heatmaps, violin plots, KDE distributions, scatterplots, and pairplots showing relationships between age, glucose levels, BMI, and stroke occurrences. | `seaborn`, `matplotlib` |
| **Aggregation** | Use of `groupby`, `query`, and `transform` functions to analyze sub-populations. | `pandas` |

---

### Prerequisites & Installation

To run this Jupyter Notebook, install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scipy
