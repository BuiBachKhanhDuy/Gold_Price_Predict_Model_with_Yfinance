# GOLD PRICE PREDICT MODEL WITH YFINANCE
A project to predict gold price trends using data from Yahoo Finance, with data visualization, preprocessing, modeling, and evaluation.


## Project Overview
Project include two main parts:
1. Data Visualization (Data_Visualization.ipynb): Data collected by import yfinance library with ticket GC=F (Gold price). In the file you can find charts that use for visualization and notes of my insight about gold price analysis.
2. Predict Model (Predict_Model.ipynb): This part include preprocessing, train model (Random Forest, XGBoost, MLP), evaluation and backtest function.

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
    Train-test split (Time Series Split).
  Models Used:
    Random Forest
    XGBoost
    MLP
  Evaluation:
    Regression: MSE, R² Score
    Classification: Accuracy, Confusion Matrix, Precision, Recall, F1-score
  Backtesting:
    Evaluate how the model performs on unseen data by simulating predictions over time.


## Results
### Classification
<img width="567" height="435" alt="image" src="https://github.com/user-attachments/assets/1af9c15c-2a4e-4204-a46a-ec92d3b2e925" />

<img width="1698" height="547" alt="image" src="https://github.com/user-attachments/assets/944d3728-972f-4194-86a3-2a5586f440bf" />



### Regression
<img width="789" height="490" alt="image" src="https://github.com/user-attachments/assets/cd7bf07b-324a-4f88-9505-f442bfaeef08" />

<<img width="2090" height="590" alt="image" src="https://github.com/user-attachments/assets/17854d14-7627-48ab-a3b1-a2831c36df84" />



From the charts above, Random Forest seems to have higher accuracy compare to XGBoost and MLP in classification task. In regressor task, MLP significantly higher in MSE and  lower R^2. But comparasion predict values and actual values shows that MLP have better visualization about price trend, RF and XGBoost only show small predict from the begin.


