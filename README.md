# Project Overview

In this project, we'll be predicting the future price movement of **Bitcoin**. We'll leverage historical Bitcoin price data and combine it with Wikipedia edit history for the Bitcoin page. After merging the datasets, we'll train a **Random Forest** model to predict whether the Bitcoin price will rise or fall the following day. Later, we’ll enhance the model by switching to **XGBoost** and incorporating more sophisticated predictors for improved performance.

To evaluate our model accurately, we’ll develop a custom **backtesting framework** and apply a reliable error metric to assess performance.

> This methodology can also be adapted to forecast other cryptocurrencies.

---

## Project Workflow

1. Load and explore data  
2. Clean, process, and merge datasets  
3. Build an initial machine learning model and assess accuracy  
4. Upgrade to a more advanced model and fine-tune features  

---

## Code Repository

You can find the full implementation in the following Jupyter notebooks:

- **`prediction.ipynb`** – Contains the core model code to forecast Bitcoin prices  
- **`sentiment.ipynb`** – Generates the dataset using Wikipedia edit history  

---

## Local Setup

### Installation

To run this project locally, make sure you have:

- **JupyterLab**
- **Python 3.8 or newer**
- The following Python packages:
  - `pandas`
  - `yfinance`
  - `scikit-learn`
  - `xgboost`
  - `mwclient`
  - `transformers`

---

## Data

- Generating the Wikipedia edits dataset can take a while. For convenience, a pre-generated version (**`wikipedia_edits.csv`**) is available in this repository. You can download and use it directly.
- Bitcoin price data will be fetched using the **`yfinance`** package during the execution of the notebook.

---

## Running the Project

1. Start by executing **`sentiment.ipynb`** to generate or update the Wikipedia edits dataset. The existing file in the repo may be outdated, and this step will bring the data up to date.
2. Then run **`prediction.ipynb`**, which by default loads data from `btc.csv`. If you'd prefer to fetch the most recent data, simply remove or modify the code that loads from the local file.
