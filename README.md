# GOLD PRICE PREDICT MODEL WITH YFINANCE
A project to predict gold price trends using data from Yahoo Finance, with data visualization, preprocessing, modeling, and evaluation.


## Project Overview
Project include two main parts:
1. Data Visualization (Data_Visualization.ipynb): Data collected by import yfinance library with ticket GC=F (Gold price). In the file you can find charts that use for visualization and notes of my insight about gold price analysis.
2. Predict Model (Predict_Model.ipynb): This part include preprocessing, train model (Random Forest and XGBoost), evaluation and backtest function.

## Installation
Clone the repository and install the required dependencies:

```bash
git clone https://github.com/BuiBachKhanhDuy/Gold_Price_Predict_Model_with_Yfinance.git
cd Gold_Price_Predict_Model_with_Yfinance
pip install -r requirements.txt
```
The main dependencies include:

- yfinance
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- xgboost
(See requirements.txt for the full list.)

## How It Works
1. Data Collection
  Gold price data is fetched directly from Yahoo Finance using the yfinance library with ticker GC=F.
  Daily historical data is downloaded including Open, High, Low, Close, and Volume.
2. Data Visualization (Data_Visualization.ipynb)
  Explore price trends and volume over time.
  Generate correlation heatmaps, moving averages, and distribution charts.
  Provide insights into gold’s volatility and seasonal patterns.
3. Predictive Modeling (Predict_Model.ipynb)
  Preprocessing:
    Create target variables for both regression (next-day close price) and classification (price direction up/down).
    Feature engineering (daily returns, price changes, etc.).
    Train-test split.
  Models Used:
    Random Forest
    XGBoost
  Evaluation:
    Regression: MSE, R² Score
    Classification: Accuracy, Confusion Matrix, Precision, Recall, F1-score
  Backtesting:
    Evaluate how the model performs on unseen data by simulating predictions over time.


## Results
### Classification
<img src="https://github.com/user-attachments/assets/884b617b-9a01-43e4-989b-af6435746721" width="567" height="435" />

<img src="https://github.com/user-attachments/assets/df9ea8e8-312d-4517-aead-fa288aeb24e0" width="1156" height="547" />

### Regression
<img src="https://github.com/user-attachments/assets/434d75af-2054-4488-bca2-61aead095e8d" width="630" height="470" />

<img src="https://github.com/user-attachments/assets/574bab99-9424-4fee-a13e-7ddd3fe22ba8" width="1154" height="547" />


From the charts above, XGBoost seems to have higher performance compare to Random Forest. Howeve, both models did not work well with gold price dataset from past 10 years.



