# \# ARIMA Analyses for Crypto Markets

# 

# This repo contains a Jupyter Notebook (`arima\_price\_and\_returns.ipynb`) that tests two "Hybrid" ARIMA modeling approaches on a crypto (BTC) time series.

# 

# Both models use an \*\*Expanding Window\*\* (for stability) and \*\*Dynamic Parameters\*\* (for adaptation, re-fitting params every 200 steps).

# 

# \## The Two Models in the Notebook

# 

# \### 1. The Hybrid Price Model (d=1)

# \* \*\*What it does:\*\* Tries to forecast the price itself (using `d=1` differencing).

# \* \*\*Method:\*\* Re-searches for the best (p,d,q) parameters during the test to adapt to market changes.

# 

# \### 2. The Hybrid Returns Model (d=0)

# \* \*\*What it does:\*\* Tries to forecast the log-returns (using `d=0`, which is an ARMA model).

# \* \*\*Method:\*\* This also re-searches for the best (p,d,q) parameters, adapting to changes in the data's structure.

# 

# \## Requirements

# 

# \* pandas

# \* numpy

# \* matplotlib

# \* statsmodels

# \* scikit-learn

# 

# You can install them with: `pip install pandas numpy matplotlib statsmodels scikit-learn`

# 

# \## How to Use

# 

# 1\.  Clone or download this repo.

# 2\.  Make sure your data file (e.g., `BTC\_LAST1YEAR\_4H.csv`) is in the same folder.

# 3\.  Open and run the `arima\_price\_and\_returns.ipynb` notebook.

# 

# Each analysis will print a summary report and generate plots.

