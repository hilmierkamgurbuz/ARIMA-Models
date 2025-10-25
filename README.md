# ARIMA Analyses for Crypto Markets

This repo contains a Jupyter Notebook (`arima_price_and_returns.ipynb`) that tests two "Hybrid" ARIMA modeling approaches on a crypto (BTC) time series.

Both models use an **Expanding Window** (for stability) and **Dynamic Parameters** (for adaptation, re-fitting params every 200 steps).

## The Two Models in the Notebook

### 1. The Hybrid Price Model (d=1)
* **What it does:** Tries to forecast the price itself (using `d=1` differencing).
* **Method:** Re-searches for the best (p,d,q) parameters during the test to adapt to market changes.

### 2. The Hybrid Returns Model (d=0)
* **What it does:** Tries to forecast the log-returns (using `d=0`, an ARMA model).
* **Method:** This also re-searches for the best (p,d,q) parameters, adapting to changes in the data's structure.

## Requirements

* pandas
* numpy
* matplotlib
* statsmodels
* scikit-learn

You can install them with: `pip install pandas numpy matplotlib statsmodels scikit-learn`

## How to Use

1.  **Get the Data:**
    * This analysis needs a `.csv` file (like `BTC_LAST1YEAR_4H.csv`).
    * You can download the data by running the script from my other project:
    * **[Binance-Futures-Data-Fetcher](https://github.com/hilmierkamgurbuz/Binance-Futures-Data-Fetcher)
2.  **Clone this Repo:**
    * Clone this project to your local machine.
3.  **Run the Analysis:**
    * Place the `.csv` file in this project's folder.
    * Open and run the `arima_price_and_returns.ipynb` notebook.