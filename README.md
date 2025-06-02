# Predicting Price Moves with News Sentiment

## Overview

This project was developed for the 8 Academy AIM Week 1 Challenge. It investigates the relationship between news sentiment and stock price movements by performing:

- **Quantitative analysis** using technical indicators (SMA, RSI, MACD)
- **Sentiment analysis** on news headlines using NLTK’s VADER
- **Focused stocks:** AAPL, AMZN, GOOG, META, MSFT, NVDA, TSLA

---

## Repository Structure

```
data/
├── fnspid.csv              # News headlines dataset
├── yfinance_data/          # Raw stock data (AAPL.csv, etc.)
└── processed/              # Stock data with technical indicators

notebooks/
├── quant_analysis.ipynb    # Technical analysis using TA-Lib
├── sentiment_analysis.ipynb# Sentiment analysis and correlation
├── final_report.md         # Summary of findings
└── *.png                   # Visual outputs

README.md                   # Project info
requirements.txt            # Dependencies
```

---

## Setup Instructions

### Prerequisites

- Python 3.8+
- Git
- Virtual environment tool (e.g., venv)

### Steps

1. **Clone the repository:**
    ```bash
    git clone https://github.com/abmoh4219/Predicting-Price-Moves-with-News-Sentiment.git
    cd Predicting-Price-Moves-with-News-Sentiment
    ```

2. **Create and activate a virtual environment:**
    - **Windows**
      ```bash
      python -m venv venv
      venv\Scripts\activate
      ```
    - **macOS/Linux**
      ```bash
      python -m venv venv
      source venv/bin/activate
      ```

3. **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4. **Download VADER lexicon for sentiment analysis:**
    ```bash
    python -c "import nltk; nltk.download('vader_lexicon')"
    ```

5. **Verify data files exist:**
    - `data/fnspid.csv`
    - CSV files in `data/yfinance_data/`

---

## Running the Notebooks

Start Jupyter Notebook:

```bash
python -m notebook
```

Open and run:

- `notebooks/quant_analysis.ipynb`: Computes SMA, RSI, MACD and saves results
- `notebooks/sentiment_analysis.ipynb`: Applies VADER sentiment analysis and calculates correlations

**Outputs:**

- Plots → `notebooks/*.png`
- Processed data → `data/processed/`

---

## Project Tasks

### Task 2: Quantitative Analysis

- Uses TA-Lib to calculate:
  - 20-day SMA
  - 14-day RSI
  - MACD
- Visualizes trends for each stock

### Task 3: Sentiment Analysis

- Analyzes `fnspid.csv` using VADER (NLTK)
- Calculates correlation between sentiment and stock returns

---

## Challenges Tackled

- Performance optimization via sampling
- Reduced plot file sizes
- Fixed path errors while saving data

---

## Dependencies

Core libraries (see `requirements.txt`):

- `pandas`, `numpy` — data processing
- `matplotlib`, `seaborn` — visualization
- `nltk` — sentiment analysis
- `talib` — technical indicators
- `jupyter` — notebook interface
