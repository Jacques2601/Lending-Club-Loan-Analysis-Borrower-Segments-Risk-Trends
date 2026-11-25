# Lending Club | Borrower Segmentation & Loan Analytics

## Business objective

A CareerFoundry Data Analytics portfolio project exploring historical Lending Club loan records to understand borrower characteristics, lending terms and regional patterns. The analysis demonstrates data preparation at scale, exploratory modelling, customer segmentation and business intelligence. It is not a validated credit scoring or default prediction system.

[View the interactive Tableau storyboard](https://public.tableau.com/app/profile/jacques.van.rensburg/viz/LendingClubLoanAnalysisBorrowerSegmentsRiskTrends/Storyboard?publish=yes)

## Data and analytical scope

The saved data-cleaning notebook reports 2,260,669 records and 112 variables after cleaning. The clustering experiment retains 1,001,574 records and 83 numeric features after missing-data filtering. These counts describe the original notebook runs, not the smaller CSV included in this repository.

## Key findings

### Borrower segmentation

The KMeans experiment standardises numeric features and uses the elbow method to select three clusters. Saved calculated medians are shown below (USD).

| Cluster | Records | Median loan amount | Median annual income | Median interest rate |
| --- | ---: | ---: | ---: | ---: |
| 0 | 555,479 | $10,000 | $56,400 | 12.62% |
| 1 | 212,309 | $13,400 | $77,000 | 12.62% |
| 2 | 233,786 | $27,000 | $100,000 | 12.62% |

The clusters differ in median loan size and income, but these summaries do not establish default probabilities or creditworthiness. The original notebook's narrative contains conflicting median values; this table uses its calculated output instead.

### Interest-rate regression

A univariate linear regression tests whether loan amount alone explains interest rates, using a 70/30 random train/test split. Saved test results: R² = 0.0093; MSE = 23.04 (squared percentage points). Loan amount alone explains less than 1% of the observed test-set variation. This negative result motivates evaluating additional appropriate features rather than deploying the model.

### Geographic and time-series analysis

The geographic notebook aggregates mean interest rates by US state and creates a Folium choropleth. The Tableau storyboard provides additional exploratory lending visualisations. The separate time-series notebook demonstrates seasonal decomposition, differencing and Augmented Dickey-Fuller testing on US unemployment data (1980–2008); it does not establish a relationship between unemployment and Lending Club outcomes.

## Notebook guide

| Notebook | Purpose |
| --- | --- |
| [1. Sourcing open data](1.%20Sourcing%20Open%20Data.ipynb) | Data loading and cleaning |
| [2. Exploring relationships](2.%20Exploring%20Relationships.ipynb) | Exploratory analysis and correlations |
| [3. Geographical visualisations](3.%20Geographical%20Visualizations%20with%20Python.ipynb) | State-level interest-rate mapping |
| [4. Supervised regression](4.%20Supervised%20Machine%20Learning%20Regression.ipynb) | Interest-rate regression and evaluation |
| [5. Unsupervised clustering](5.%20Unsupervised%20Machine%20Learning%20Clustering.ipynb) | Standardisation, KMeans and cluster profiling |
| [6. Time-series analysis](6.%20Sourcing%20and%20Analyzing%20Time%20Series%20Data.ipynb) | Separate unemployment-series exercise |

## Repository files

- `lending_club_loans_sample.csv` — loan data sample.
- `lending_club_clustered.xlsx` — prepared clustering visualisation data.
- `lending_club_time_geo_ready.xlsx` — prepared temporal and geographic visualisation data.
- `Storyboard.twb` — Tableau workbook.

## Reproducibility and limitations

The original notebooks and saved outputs are preserved. Results have not been independently reproduced. The notebooks reference local Windows paths and full source/cleaned CSV files that are not included under those filenames. The included sample is not a verified drop-in replacement for the full dataset. Exact source version, redistribution permissions and dependency versions require verification.

Core tools: Python, pandas, NumPy, scikit-learn, Matplotlib, seaborn, Folium, statsmodels, Jupyter, Excel and Tableau.

Before extending the analysis:

- Reconcile notebook narrative, exported cluster data and dashboard labels.
- Audit feature availability at origination; exclude post-origination information for any prospective risk model.
- Assess missing-data selection bias, redundant features, outliers and cluster stability.
- Compare loan outcomes using appropriate denominators and comparable loan vintages or observation windows. Recent loans may not have matured.
- Validate regional summaries against sample sizes and source data; geographic association is not causation.
- Document dataset provenance and portable paths, then rerun with a reproducible environment.

## Business relevance

The project illustrates how exploratory analytics can identify questions for lending portfolio monitoring, segmentation and reporting. Any lending decision or default-risk application would require separate outcome validation, temporal testing, fairness assessment and domain review.

**Author:** Jacques van Rensburg
