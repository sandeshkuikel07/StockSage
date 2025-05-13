
---

#  StockSage: Stock Prediction & Portfolio Management

**StockSage** is a smart, AI-driven web app that predicts stock prices using a time-series **LSTM model** and helps users manage and visualize their stock portfolios. It features a **Flask backend**, a **React frontend**, and a custom-built **Gemini engine** that interprets model predictions for insightful recommendations.

---

##  Features

* 🔮 **LSTM-Based Stock Price Prediction**
* 📊 **Visualization** of historical and predicted trends
* 💡 **Gemini Insight Engine** for forecast interpretation
* 🗞️ **Sentiment Analysis** of financial news using FinBERT
* 💼 **Portfolio Management Interface**
* ⚙️ **Model saved as `.pkl`** for fast deployment
* 🌐 **React + Flask** full-stack architecture
* 📥 **Historical data** provided by `Mero Lagani`

---

##  How It Works

1. **Fetch Data**: Historical stock prices and news articles
2. **Clean News Text**: Preprocess headlines and content (tokenization, stopword removal, etc.)
3. **Sentiment Analysis**: Use **FinBERT** to classify each article as **positive**, **neutral**, or **negative**
4. **Feature Fusion**: Combine sentiment scores with technical indicators (e.g., price, volume, moving average)
5. **Train Model**: LSTM trained on enriched data using PyTorch
6. **Save Model**: Trained model is serialized as `.pkl` using `joblib` or `pickle`
7. **Flask Backend**: Loads `.pkl` and serves predictions via API
8. **Frontend**: Displays forecast charts and manages virtual portfolio

---

## 🧪 Model Training

Train or retrain the model by running:

```
notebooks/stock_prediction.ipynb
```

The final model is exported as:

```
model/(...).pkl
```

---

##  Setup Instructions

### Backend (Flask)

```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python app.py
```

### Frontend (React)

```bash
cd frontend
npm install
npm start
```

---

## 💡 Gemini Engine

The Gemini module interprets predictions with:

* 📈 Trend direction (Buy/Sell/Hold)
* 📊 Confidence scores
* ⚠️ Volatility alerts

---

## 🙌 Built With

* [Flask](https://flask.palletsprojects.com/)
* [React](https://reactjs.org/)
* [PyTorch](https://pytorch.org/)
* [joblib](https://joblib.readthedocs.io/) / `pickle`
* [FinBERT](https://github.com/ProsusAI/finBERT) for sentiment analysis

---
