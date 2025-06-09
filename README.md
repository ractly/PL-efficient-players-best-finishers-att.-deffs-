# ⚽ Premier League Player Efficiency & Ball Carrying Analysis

This project analyzes football players' **offensive and defensive efficiencies** based on Premier League data, focusing on metrics such as contribution per salary, dribbling efficiency, and progressive carrying.

---

## 📊 Project Goals

- Identify the **most efficient players** based on their goal/assist contributions relative to their salary and minutes played.
- Evaluate **dribbling efficiency** among forwards using attempted vs successful take-ons.
- Detect **modern defenders** who contribute to attack through progressive carries.
- Visualize and interpret all findings through **clean, insightful charts**.

---

## 🧩 Data Sources

The project uses 3 main `.csv` datasets:

- `player_stats.csv`: goals, assists, minutes, expected goals, etc.
- `player_salaries.csv`: annual and weekly wages
- `player_possession_stats.csv`: touches, carries, progressive carries, dribbling stats

> All datasets are fictional or anonymized for educational purposes.

---

## 🧠 Key Metrics

### Offensive Efficiency
- `contribution = goals + assists`
- `efficiency = (contribution / minutes) / salary`

### Dribbling Efficiency
- `dribbling_efficiency = successful_take_ons / attempted_take_ons`
- Filtered for `attempted_take_ons >= 10` and position containing `"FW"`

### Defensive Carry Ratio
- `carry_outside_ratio = progressive_carries / (touches - deffensive_touches)`
- Applied only to players with `"DF"` in position and at least 5 progressive carries

---

## 📈 Visualizations

- **Bar charts** for top efficient players
- **Scatter plots** for dribbling efficiency vs take-ons, with average line
- **Lollipop charts** for progressive defenders

All plots are generated using `matplotlib`.

---

## 🛠 Tech Stack

- Python 3.x
- Pandas
- Matplotlib
- Jupyter Notebook / Kaggle Notebook

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/pl-efficiency-analysis.git
   cd pl-efficiency-analysis
