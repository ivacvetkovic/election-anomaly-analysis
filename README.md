# Election Anomaly Analysis

## Overview

Election Anomaly Analysis is a data-analysis and visualization project exploring how statistical and introductory cybersecurity methods can be used to identify unusual patterns in election data.

The project contains two components:

- **Python analysis notebook** — performs data cleaning, anomaly detection, statistical testing, risk scoring, visualization, and synthetic tampering simulation.
- **Interactive web interface** — presents selected results through a static HTML/CSS/JavaScript walkthrough with animated charts and explanations.

Two dataset modes are supported:

1. A real New Jersey dataset from the 2020 general election
2. A synthetic precinct-level dataset designed to demonstrate methods that require more complete data

Statistical anomalies are treated as indicators for further investigation, not as evidence of fraud.

## Analysis Methods

The Python notebook includes:

- Data cleaning and standardization with Pandas
- Turnout and vote-pattern analysis
- Local Outlier Factor (LOF) anomaly detection
- Benford's Law analysis where applicable
- Last-digit irregularity testing
- County-level risk scoring using multiple indicators
- Synthetic tampering simulation
- Precision and recall evaluation
- Data visualization with Matplotlib

## Technologies

**Analysis:** Python, Pandas, NumPy, SciPy, scikit-learn, Matplotlib  
**Web:** HTML, CSS, JavaScript  
**Environment:** Jupyter / Google Colab

## Real NJ Dataset Mode

The real-data mode uses precinct-level vote returns together with county-level registered-voter information.

Because the available registration data is county-level, analyses requiring precinct-level registered-voter counts are limited or disabled in this mode.

The web interface presents:

- County turnout
- County vote totals
- Ballot rejection rates
- County-level anomaly patterns

## Synthetic Dataset Mode

The synthetic dataset provides complete precinct-level fields so the full analysis pipeline can be demonstrated.

It supports:

- Precinct-level turnout analysis
- Local Outlier Factor anomaly detection
- Benford's Law analysis
- Last-digit testing
- County-level risk scoring
- Tampering simulation and precision/recall evaluation

## Important Methodological Note

The project is an introductory demonstration of statistical anomaly detection and cybersecurity-oriented risk analysis.

A statistical anomaly does **not** establish that manipulation or fraud occurred. Results are intended to identify unusual patterns that could warrant additional investigation.

## Running the Analysis

Open `Election_Anomaly_Analysis.ipynb` in Jupyter Notebook or Google Colab.

1. Upload the required real-data CSV files if using Real NJ mode.
2. Run the installation/import cell.
3. Select either the real or synthetic dataset.
4. Run the remaining cells in order.

## Web Demo

The browser-based visualization is contained in:

- `index.html`
- `style.css`
- `app.js`

Open `index.html` locally in a browser to view the interactive walkthrough.

## Data Sources

- MIT Election Data and Science Lab (2022).  
  *U.S. President Precinct-Level Returns 2020* (Harvard Dataverse, V4).  
  https://doi.org/10.7910/DVN/JXPREB

- New Jersey Division of Elections (2020).  
  *Official General Election Voter Turnout (County-level).*  
  https://www.nj.gov/state/elections/assets/pdf/election-results/2020/2020-official-general-voter-turnout.pdf
This project is intentionally scoped as an introductory analytical walkthrough rather than a full election auditing system.

To ensure accessibility and ease of use, the application relies on precomputed summary values instead of accepting user-uploaded datasets. Future improvements could include dynamic CSV uploads, live recomputation of metrics, and additional statistical checks.
