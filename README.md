### 📊 Netflix Stock Price Forecasting using Time Series (ARIMA & SARIMA) 

🔍 Overview
This project focuses on forecasting Netflix stock prices using classical time series models such as ARIMA and SARIMA. The goal is to understand historical patterns, ensure stationarity, and predict future trends with visual accuracy.

📁 Dataset
Source: Historical stock prices of Netflix

File used: NFLX.csv

Columns:

Date

Open, High, Low, Close, Volume

Adjusted Close (used as Final Price)

📌 Objectives
📈 Load and preprocess historical stock data

🧹 Clean and transform the data (log, difference)

📉 Perform statistical tests for stationarity

⚙️ Build ARIMA and SARIMA forecasting models

📊 Forecast and visualize future stock prices

✅ Evaluate models using RMSE

🔧 Tools & Technologies
Python

Pandas, NumPy – data handling

Matplotlib, Seaborn – visualizations

Statsmodels – ARIMA, SARIMA modeling

Sklearn – RMSE evaluation

📈 Project Workflow
1. 📦 Data Cleaning
Dropped unnecessary columns

Renamed 'Adj Close' → 'Final Price'

Converted dates to datetime and resampled monthly

2. 📊 Exploratory Data Analysis (EDA)
Line plot to visualize stock trends

Seasonal decomposition to extract trend, seasonality, residual

3. 🧪 Stationarity Check
Used ADF Test

Log transformation and differencing applied

Re-validated stationarity post-transformation

4. ⚙️ Model Building
Applied ARIMA(2,1,2) initially

Used Grid Search over (p,d,q) to tune model

Introduced SARIMA (0,1,1)(0,1,1,12) for seasonality

5. 🔮 Forecasting
Generated 1-step, 5-step, and 12-step ahead forecasts

Converted forecasts back from log scale using np.exp

Plotted actual vs predicted data for visual validation

6. ✅ Model Evaluation
RMSE calculated for each (p,d,q) combo

Compared models visually and numerically


Here's what a forecast plot might look like:

### ARIMA Forecast Plot

![ARIMA Forecast](<img width="1603" height="1237" alt="forecast_plot1" src="https://github.com/user-attachments/assets/7ff4bb61-7ecb-4c56-ad81-86dc029de651" />
)

### Rolling Mean and Std Visualization

![Rolling Stats](<img width="1638" height="1253" alt="forecast_plot2" src="https://github.com/user-attachments/assets/d9522d5f-d255-4e1e-803f-dd809a62d34a" />
)

## 📈 Forecast Visualizations

Here are some sample outputs from the time series modeling process:

### Original + Rolling Mean & Std

![Rolling Statistics](<img width="1638" height="1253" alt="forecast_plot2" src="https://github.com/user-attachments/assets/f20da83c-c17b-4453-8611-de1d7b88ea1e" />
)

### Differenced Series with Forecast

![ARIMA Forecast](<img width="1603" height="1237" alt="forecast_plot1" src="https://github.com/user-attachments/assets/c1a57870-738b-4ffc-a756-b16ac77bde2a" />
)

### Final Forecasted Prices (Transformed Back)

![Final Prediction](<img width="1656" height="1237" alt="forecast_plot4" src="https://github.com/user-attachments/assets/d054d3c2-bda8-4d14-b04e-8337af0231be" />
)



🧠 Key Learnings
How to transform time series for stationarity

ARIMA vs SARIMA modeling decisions

Forecast evaluation using RMSE and visual plots

Real-world application of statistical time series models

📌 Conclusion
This project highlights how traditional time series models can be used to analyze and forecast real-world financial data. By preprocessing the data correctly and tuning the right model parameters, we can gain powerful insights into future trends. The ARIMA/SARIMA approach proved effective for capturing both short-term movements and seasonality in Netflix's stock prices.



🚀 Future Improvements
- Integrate auto_arima for automatic tuning

- Add confidence intervals to forecast plots

- Deploy a Streamlit dashboard for user interaction

- Compare with LSTM or Prophet models for deep learning analysis

📬 Contact
If you have any suggestions or questions, feel free to reach out or create an issue in the repository.
