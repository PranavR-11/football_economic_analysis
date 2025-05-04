# ⚽ The Price of Performance  
## How Output, Opportunity, and Origin Shape Player Value in Elite Football  
**Pranav Rao Rebala**  
---

## 📌 Abstract  
This study investigates the determinants of football player valuation using a novel panel dataset of 8,490 player-season observations across the top five European leagues (2020–2025). A custom-built performance index and a proxy for lagged market value are used to evaluate how performance, salary, age, transfer history, and player origin influence market value. Results from a log-linear regression show that on-field performance significantly drives valuation, especially for high-wage players. However, homegrown and low-fee players remain systematically undervalued, and mid-season transfers correlate with reduced valuation. The findings confirm existing economic theory while revealing inefficiencies shaped by signaling, timing, and wage structures.

---

## 📂 Dataset & Methodology

### Data Overview
- **Player-Seasons:** 8,490  
- **Leagues Covered:** Premier League, La Liga, Bundesliga, Serie A, Ligue 1  
- **Seasons:** 2020–2025  
- **Source Format:** Player-level panel dataset created from raw CSVs, transfermarkt info, and WhoScored-style statistics

### Key Features
- `performance_index`: Composite score from goals, assists, minutes, and progressive actions. Normalized across positions and seasons.
- `proxy_market_value`: Constructed from gross wage, age, and performance. Log-transformed for regression.
- `market_value_lag`: Previous season’s proxy value (created due to missing real-world lagged data).
- `transfer_status`: Coded as 0 (no transfer), 1 (mid-season), 2 (off-season).
- `homegrown_or_lowpaid`: Binary indicator based on age < 20, playing time > 1000 mins, or below-median wage.

### Model Specification
A single **log-linear OLS regression** was used:
