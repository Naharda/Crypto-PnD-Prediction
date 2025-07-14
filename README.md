# 📈 Crypto PnD Prediction

A machine‑learning based framework to **detect and predict cryptocurrency pump‑and‑dump (PnD) schemes** using historical patterns, sentiment analysis, and sequence modeling.

---

## 🚀 Features

- **Event extraction from Telegram**: Parses major pump‑and‑dump Telegram channels by tracking message history and metadata.
- **Sequence modeling**: Utilizes LSTM or Transformer-based neural networks to predict the probability of an upcoming PnD event for a specific coin.
- **Feature engineering**:
  - Price/action time series: volume & price spikes  
  - Trading indicators: moving averages, RSI, MACD, Bollinger Bands  
  - Sentiment analysis: Telegram messages, social media noise  
  - Historical PnD event patterns  
- **Evaluation metrics**: Accuracy, ROC‑AUC, precision/recall, F1-score for model validation.
- **Interactive dashboards**: Visualize channel activity, real-time signals, and performance metrics.

---

## 📁 Repository Structure

```
Crypto-PnD-Prediction/
├── Coins data/
├── notebooks/
├── src/
│   ├── ingestion/
│   ├── features/
│   ├── modeling/
│   ├── evaluation/
│   └── utils/
├── requirements.txt
└── README.md
```

---

## ⚡ Quick Start

1. **Clone the repo**  
   ```bash
   git clone https://github.com/Naharda/Crypto-PnD-Prediction.git
   cd Crypto-PnD-Prediction
   ```

2. **Python + venv setup**  
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```
---

## 🧠 Model & Approach

1. **Data sources**: Collected and labeled ~700 PnD events from Telegram channels over several years.  
2. **Feature types**:
   - Channel‑level spike detection and intra-sequence homogeneity  
   - Price series technical indicators  
   - Natural Language Processing on chat message context  
3. **Model architectures**:
   - **LSTM‑based sequence model**  
   - **Transformer with positional/temporal attention**  
4. **Interpretability**: Attention weights help identify which messages or timepoints triggered an alert.

---

## 📊 Results & Performance

| Metric       | Value       |
|--------------|-------------|
| ROC‑AUC      | 92%         |
---

## 🛠️ Advanced Usage

- **Add new channels**: Drop Telegram export JSON/CSV into `data/raw/`, then run ingestion.
- **Hyperparameter tuning**: Use `src/modeling/hyperparam_search.py`.
- **Deploy as a service**: Integrate model into a Flask/Streamlit API.
- **Extend to other platforms**: Add feature extraction for Twitter, Discord, etc.

---

## 🤝 Contributing

Contributions, bug reports, and enhancements are welcome!

1. Fork the repo  
2. Create a new branch: `git checkout -b feature/*`  
3. Commit changes with a descriptive message  
4. Submit a pull request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for details.

---

## 🙏 Acknowledgments

- Telegram communities documenting PnD events  
- Maintainers of crypto-data APIs (CoinGecko, Binance, ccxt)  
- Hu *et al*. (2022) for PnD detection inspiration

---

**Happy detecting! ⚡**
