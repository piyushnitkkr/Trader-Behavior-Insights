# 📊 Trader Performance vs. Market Sentiment Analysis

This project explores the relationship between **trader behavior/performance** and the **Bitcoin market sentiment** (Fear vs. Greed). It merges real trade data with market sentiment indices to uncover patterns that can drive smarter trading strategies.

---

## 📌 Objective

- Investigate how **market sentiment** (Fear or Greed) influences **trading decisions**, such as:
  - Trade size
  - Trade direction (Buy/Sell)
  - Aggression (crossed orders)
  - Profitability (Closed PnL)

- Identify **behavioral patterns** and **hidden risks** under different sentiment conditions.
- Provide **visual insights** and actionable takeaways for smarter decision-making.

---

## 📁 Dataset Overview

### 1. `fear_greed_index.csv`
- Historical Bitcoin market sentiment.
- **Columns**:
  - `timestamp` (Unix time)
  - `value` (0–100 score)
  - `classification` (Fear, Greed, Extreme Fear, etc.)
  - `date` (formatted date)

### 2. `trader_data.csv`
- Trade-level data from Hyperliquid or similar DEX.
- **Columns** (partial):
  - `Account`, `Coin`, `Execution Price`, `Size USD`, `Side`, `Start Position`
  - `Direction`, `Closed PnL`, `Fee`, `Crossed`, `Timestamp IST`, `Trade ID`, etc.

---

## 🧪 Analysis Workflow

### ✅ 1. Data Cleaning & Preprocessing
- Parse and format timestamps
- Normalize sentiment labels
- Handle missing and inconsistent values

### 🔗 2. Merging
- Trades are joined with sentiment data using the trade date

### 📊 3. Exploratory Data Analysis
- Trade volume and distribution by sentiment
- Avg. PnL, Fee, and Size USD under each sentiment
- Buy vs Sell breakdown

### 📈 4. Visualization
- Boxplot of PnL by sentiment
- Barplot of average trade size
- Count plot of trade types
- Correlation matrix of trading features

### 🔍 5. Pattern Discovery
- Aggressive trading behavior (Crossed = TRUE)
- Impact of sentiment on performance and trade type

---

## 💡 Key Insights

- Larger trades are observed during **Greed**, but **profitability is often lower** due to overconfidence.
- **Aggressive orders** are more frequent in **Greed** conditions.
- **Fear periods** may offer better win rates for contrarian strategies.
- Trade direction and size vary meaningfully with sentiment.

---

## 📁 Output

- `merged_trader_sentiment.csv`: Final dataset with sentiment mapped to each trade
- Visual insights generated via Matplotlib and Seaborn

---
Dataset Links : Historical Data 

https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing

Fear Greed Index link:

https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing


## ▶️ Getting Started

### 1. Install dependencies
```bash
pip install pandas matplotlib seaborn
