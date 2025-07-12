"# nse-1min-return-predictor" 

---

## 🔍 Problem Statement

> Predict the **next-minute stock return** (ratio of time T+1 price to time T price) using market microstructure features such as volume, trade imbalance, spreads, and order book statistics.

---

## 🧠 Features Engineered

Aggregated per minute per stock:
- `num_trades`, `o`, `h`, `l`, `c`, `total_volume`
- `total_buy_cap`, `total_sell_cap`, `weighted_price`
- `trade_imbalance_ratio`, `volume_imbalance_ratio`
- `avg_spread`, `max_spread`, `min_spread`
- `weighted_avg_bid_price`, `weighted_avg_ask_price`

Target variable:
- **Return** = (Next minute's close price) / (Current minute's close price)

---

## ✅ Tasks Completed

- ✅ Aggregated trade and quote data to 1-minute intervals
- ✅ Engineered predictive features
- ✅ Modeled using Linear Regression (`sklearn`)
- ✅ Evaluated with:
  - 📈 **Minute-wise correlation plot** (actual vs predicted returns)
  - 📊 **Confusion matrix** for up/down classification
  - 🔥 **Correlation matrix heatmap** across all companies

---

## 📊 Example Outputs

### 1. Correlation over time  
Measures how well predictions match real returns over each minute.

### 2. Confusion Matrix  
We binarized returns as:
- `1` → Stock went **up**
- `0` → Stock went **down/flat**

### 3. Correlation Matrix  
Stock-wise return correlations across companies on the selected date.

---

## 📦 Requirements

```bash
pip install -r requirements.txt
