# Milestone-3
🧠 AI Market Sentiment Forecast (Prophet + Slack Alerts)

This project analyzes AI market sentiment trends using historical sentiment scores stored in a local CSV file.
It uses Facebook Prophet for time series forecasting and sends Slack alerts for detected sentiment changes.

📁 Project Overview

This module (milestone_3_prophet_fixed.py) is part of the Infosys Springboard Internship – Week 5-6 tasks.

It performs the following:

Loads pre-analyzed AI sentiment data (analyzed_ai_market_data.csv)

Aggregates and cleans recent 90 days of scores

Forecasts sentiment for the next 14 days using Prophet

Generates and displays a forecast plot

Sends Slack alerts for both strong and small sentiment changes

⚙️ Features

✅ Load and preprocess local sentiment data
✅ Forecast next 14 days of sentiment using Prophet
✅ Visualize forecasts with Matplotlib (auto-shown and saved)
✅ Send automated Slack alerts:

📈 Mild sentiment improvement

📉 Slight or strong decline

⚠️ Negative sentiment prediction

🚀 Sudden positive surge

🧭 Final average sentiment summary

🧰 Requirements

Install dependencies with:
pip install pandas matplotlib prophet python-dotenv requests

📦 Project Structure
📂 Week 5-6
 ┣ 📂 data
 ┃ ┗ analyzed_ai_market_data.csv
 ┣ 📂 plots
 ┃ ┗ prophet_sentiment_forecast.png
 ┣ 📂 scripts
 ┃ ┗ milestone_3_prophet_fixed.py
 ┣ .env
 ┗ README.md

🔑 Environment Variables

Create a .env file in your project root with the following:

SLACK_WEBHOOK_URL=https://hooks.slack.com/services/your/slack/webhook/url
💡 You can generate a webhook from your Slack workspace under
Apps → Incoming Webhooks → Add to Slack

🚀 How to Run

From your terminal:

cd scripts
python milestone_3_prophet_fixed.py

📊 Output

The Prophet model will automatically:

Show a forecast graph

Save it as ../plots/prophet_sentiment_forecast.png

Send alerts to your Slack channel

pip install -r config/requirements.txt

🧠 Notes

Ensure your CSV file has at least the following columns:

timestamp, score
The code automatically filters data to the last 90 days.
If fewer than two unique days are available, Prophet may need duplicated rows to train.

🏁 Author

Rajat — Infosys Springboard Internship (Week 5–6)
AI Market Sentiment Analysis using Prophet Forecast & Slack Integration
