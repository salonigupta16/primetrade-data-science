# primetrade-data-science
Analysis of trader behavior vs. market sentiment on Hyperliquid.
# Primetrade.ai - Data Science Intern Assignment

This repository contains my analysis of how market sentiment (Fear/Greed) impacts trader behavior and performance on the Hyperliquid platform.

## ⚙️ Setup & How to Run
1. Clone this repository to your local machine.
2. Ensure you have Python installed along with the following libraries: `pandas`, `numpy`, `matplotlib`, and `seaborn`.
3. Download the two required datasets (Sentiment and Trader Data) from the provided Google Drive links.
4. Place the datasets in the same directory as the notebook (or update the file paths in the first cell).
5. Run the `Primetrade_Trader_Sentiment_Analysis.ipynb` notebook from top to bottom.

## 🔬 Methodology
* **Data Preparation:** Aligned tick-level trader data with daily sentiment classifications by converting Unix timestamps to standard date formats. 
* **Aggregation:** Grouped the data to create daily metrics per trader, including Daily PnL, Win Rate, Trade Frequency, and Average Trade Size.
* **Segmentation:** Categorized traders into "Frequent" vs "Infrequent" cohorts based on the 75th percentile of total lifetime trades to observe behavioral divergences.

## 📊 Key Insights
*(Replace these examples with your actual findings from Part B!)*
1. **Performance Discrepancy:** Traders experienced a [X]% higher median drawdown on 'Fear' days compared to 'Greed' days, indicating poor risk management during market panic.
2. **Behavioral Shifts:** Average trade sizes actually *increased* during Fear days for the bottom 50% of traders, suggesting "revenge trading" behavior.
3. **Cohort Differences:** Frequent traders maintained a steady win rate regardless of sentiment, whereas infrequent traders saw their win rate drop significantly during High Greed.

## 💡 Strategy Recommendations (Actionable Output)
*(Replace these with your ideas from Part C!)*
1. **Dynamic Margin Tightening:** Implement a rule where margin requirements automatically increase by 15% when the market shifts to 'Fear' to protect traders from outsized liquidations.
2. **Momentum Alerts for Scalpers:** Provide an opt-in alert system for our 'Frequent Trader' segment when the market enters 'Greed' territory, as historical data shows this is their most profitable environment.
