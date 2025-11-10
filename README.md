# Trader Behavior Analysis Using Fear–Greed Sentiment Index

##  Overview
This project explores how **market sentiment**—as measured by the **Fear & Greed Index**—influences trader behavior and performance.  
By combining **historical trading data** with **sentiment classification**, the analysis identifies behavioral trends such as risk-taking during greed phases and caution during fear phases.

---

## Datasets

### 1. `historical_data.csv`
Contains detailed trade-level information such as:
- Timestamp (IST)
- Trade Side (Buy/Sell)
- Size (Tokens)
- Closed PnL
- Price, Volume, etc.

### 2. `fear_greed_index.csv`
Contains daily sentiment data:
- Date
- Fear–Greed score
- Classification (Fear, Greed, Extreme Fear, Extreme Greed, Neutral)

---

## Objectives
- Correlate **market sentiment** with **trader performance** metrics.
- Understand how **trading volume**, **PnL**, and **position size** vary across sentiment phases.
- Visualize psychological trading patterns during extreme market emotions.

---

## Process Workflow

### 1. Data Cleaning & Preparation
- Loaded both datasets using Pandas.  
- Checked for **missing and duplicate values**.  
- Converted `Timestamp IST` and `date` columns into proper datetime format.  
- Merged datasets on the date field for combined analysis.

### 2. Exploratory Data Analysis (EDA)
- **Buy vs Sell Distribution:**  
  Count plot showing relative trade volume on buy/sell sides.  
- **Market Sentiment Distribution:**  
  Visualized counts of `Fear`, `Greed`, `Extreme Fear`, `Extreme Greed`, and `Neutral`.  
- Generated **correlation heatmaps** to analyze relationships among:
  - Profit/Loss (`Closed PnL`)
  - Trade Volume
  - Market Sentiment

### 3. Sentiment-Based Analysis
Grouped data by the `classification` column and calculated:
- Mean, median, and standard deviation for:
  - `Closed PnL` (profit/loss performance)
  - `Size Tokens` (trade size/volume)

---

## Key Insights
| Sentiment Phase | Behavior | PnL & Volume Pattern |
|-----------------|------------|----------------------|
| **Extreme Greed** | Aggressive trading | High trade sizes, volatile PnL |
| **Greed** | Risk-seeking behavior | Above-average PnL, larger volume |
| **Neutral** | Balanced decisions | Stable volume & PnL |
| **Fear** | Defensive strategy | Smaller positions, steady but lower PnL |
| **Extreme Fear** | Risk-averse trading | Minimal trades, low volatility |

---

## Correlation Highlights
- **PnL** positively correlated with **trade volume** during greedy phases.  
- **Sentiment normalization** revealed cyclical emotional patterns tied to performance metrics.  
- Visual correlation heatmaps illustrated interdependence among sentiment, PnL, and trading risk.

---


## Repo Structure
```
CLUB-HUB/
│
├── csv_files/
│   ├── merged_data          
│
├── outputs/       
|   ├── Avg_Trader.png
|   ├── Buy_vs_Sell.png
|   ├── Correlation.png
|   ├── Market_distribution.png
|
├── data/       
|   ├── fear_greed_index.csv
|   ├── historical_data.csv
│
├── notebook1.ipnyb
├── README.md
├── summary_ds.pdf
```

## Technologies Used
- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**

---


## Author
**Surendra Pattikonda**  
B.Tech in Computer Science (Data Science), RGM College of Engineering and Technology  
[LinkedIn](https://www.linkedin.com/in/pattikondasurendra/) • [GitHub](https://github.com/surendrapattikonda)

---

