
# India: Corruption, Education & Environmental Degradation

### A Spatial Data Science Analysis of Governance, Literacy and Vegetation Change

[View Project Portfolio](https://lorenzobettin.github.io/projects/india-environment/)

## Overview

This project explores relationships between political candidate
criminal-charge records, literacy rates and environmental change
across Indian states.

Using Python, GeoPandas and statistical analysis, the study
combines political, demographic and vegetation datasets to
investigate whether governance-related indicators and education
are associated with changes in vegetation.

The project demonstrates the application of spatial data science
to environmental and governance-related research questions.

## Research Question

Are political candidate criminal-charge records and education
levels associated with vegetation change across Indian states?

The analysis investigates two main hypotheses:

1. Higher levels of criminal charges among political candidates
   may be associated with greater environmental degradation.
2. Higher literacy rates may be associated with differences
   in environmental outcomes.

**Important:** Criminal charges do not establish proven corruption,
and vegetation change does not necessarily represent deforestation.
These variables are exploratory proxies.

## Dataset

The analysis combines several datasets covering the period
2003–2017, including:

- Vegetation-cover measurements
- Political candidate affidavit records
- State-level literacy and demographic indicators
- Indian administrative boundary geometries

### Original input files

| Dataset | Filename | Purpose |
|---|---|---|
| Vegetation data | `vcf_pc11subdist.csv` | Environmental measurements |
| Political affidavits | `affidavits_clean.csv` | Candidate criminal-charge records |
| Census indicators | `pc11_pca_clean_pc11dist.csv` | Population and literacy |
| State boundaries | `state.shp` | Geospatial visualization |

Input data are not necessarily included in this repository.
Their availability and redistribution permissions must be
checked separately.

## Methodology

### 1. Data Collection and Preparation

The original datasets were imported into Python using pandas
and GeoPandas.

The workflow included:

- Inspecting and cleaning variables
- Filtering relevant observations
- Aggregating political candidate characteristics
- Preparing vegetation-change measures
- Integrating literacy and geographical information

### 2. Spatial Data Analysis

GeoPandas was used to connect environmental and
socio-economic data to geographical boundaries.

The resulting spatial analysis enabled:

- Mapping literacy rates across Indian states
- Examining geographical variation
- Comparing observations across different regions

### 3. Exploratory Data Analysis

Exploratory visualizations and correlation analysis were
used to investigate:

- Criminal-charge records versus vegetation change
- Literacy rates versus vegetation change
- Geographic differences in explanatory variables
- Outliers and distributions

### 4. Statistical Modelling

A multiple linear regression model was used to investigate
relationships between the vegetation-change proxy and
selected explanatory variables.

The model considered:

- A rolling measure of criminal cases
- Mean vegetation
- Literacy rates

Model performance was evaluated using R-squared and
mean squared error.

## Technologies

- Python
- pandas
- NumPy
- GeoPandas
- Matplotlib
- Seaborn
- scikit-learn
- Jupyter Notebook

## Results

### Regression Performance

The original notebook reported:

| Metric | Result |
|---|---|
| Test R-squared | 0.082 |
| Test Mean Squared Error | 61.70 |

The test R-squared indicates that the model explained
approximately 8.2% of variation in the held-out observations.

This suggests limited explanatory power.

### Political Candidate Criminal Charges

The analysis found little evidence of a strong linear
relationship between the criminal-case measure and the
vegetation-change proxy.

This does not establish that governance or corruption
has no effect on environmental outcomes.

### Literacy and Environmental Change

Literacy showed a negative fitted regression coefficient.

However, the limited performance of the model prevents
strong conclusions about the relationship between
education and vegetation change.

### Geographical Variation

Spatial analysis highlighted variation in literacy
and environmental measurements across Indian regions.

The integration of datasets with different geographical
and temporal resolutions also revealed methodological
challenges.

## Limitations

The study is exploratory and has several limitations:

1. **Proxy measurements:** Criminal charges do not directly
   measure corruption, and vegetation change does not
   necessarily measure forest loss.

2. **Model performance:** The regression has limited
   explanatory power.

3. **Temporal alignment:** Some calculations use shifts
   across observations rather than fixed calendar intervals.

4. **Spatial aggregation:** Datasets contain observations
   at different geographical scales, requiring careful
   interpretation.

5. **Causality:** Statistical associations cannot establish
   causal relationships.

A more comprehensive analysis would benefit from direct
forest-loss measurements, additional governance variables,
spatially aware validation and stronger temporal alignment.

## Project Structure

```text
india-environmental-degradation/
├── README.md
├── lorenzo_bettin_india_corruption_vegetation.ipynb
└── data/
    ├── vcf_pc11subdist.csv
    ├── affidavits_clean.csv
    ├── pc11_pca_clean_pc11dist.csv
    └── state.shp
```

The `data/` directory represents the expected input structure.
The files may need to be obtained separately.

For shapefile data, companion files such as `.shx`, `.dbf`
and `.prj` may also be required.

## How to Run the Analysis

### 1. Clone the repository

```bash
git clone https://github.com/LorenzoBettin/india-environmental-degradation.git
cd india-environmental-degradation
```

### 2. Install the required Python packages

For example:

```bash
python -m pip install pandas numpy geopandas matplotlib seaborn scikit-learn jupyter openpyxl
```

Additional dependencies may be necessary depending on
the original notebook and Python environment.

### 3. Prepare the datasets

Create a folder named `data` in the repository root.

Place the required input files inside this directory,
preserving their original filenames.

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

`lorenzo_bettin_india_corruption_vegetation.ipynb`

Run the cells in order after ensuring that all input
datasets and dependencies are available.

## Reproducibility

The source notebook preserves the original analytical
workflow and visualizations.

The project may not be fully reproducible without its
original input datasets and compatible Python dependencies.

The repository is primarily intended to document the
research approach and demonstrate the analytical methods.

## Portfolio

For the full project description, figures, methodology
and interpretation, visit:

[India: Corruption & Environmental Degradation — Portfolio](https://lorenzobettin.github.io/projects/india-environment/)
