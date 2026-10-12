# Call of Duty Player Performance Analytics Dashboard

## Overview

This project presents an exploratory player-performance analytics dashboard built with Python. The analysis examines Call of Duty player statistics to identify performance patterns across individual players, countries, and weapon selections.

The dataset contains **1,000 player records and 8 original variables**, including player identity, country, kills, deaths, wins, matches, accuracy, and weapon selection.

The project extends the original dataset with calculated performance metrics, including:

- **K/D Ratio** — Kills divided by Deaths
- **Win Rate** — Wins divided by Matches



---

## Project Objectives

The primary objectives of this analysis are to:

- Explore player performance distributions.
- Identify high-performing and low-performing players.
- Compare player performance across countries.
- Analyze weapon-level performance.
- Calculate and evaluate K/D ratios.
- Calculate player win rates.
- Rank players according to performance metrics.
- Transform analytical results into visual insights through a dashboard.

---

## Key Metrics

The analysis evaluates the following performance indicators:

| Metric | Description |
|---|---|
| Kills | Number of kills recorded by each player |
| Deaths | Number of deaths recorded by each player |
| Wins | Number of matches won |
| Matches | Total matches played |
| Accuracy | Player accuracy percentage |
| K/D Ratio | Kills divided by deaths |
| Win Rate | Wins divided by matches |
| Weapon | Weapon associated with the player's record |

The dataset contains no null values across the eight original columns.

---

## Analysis Performed

### Player Performance

Players are ranked according to their kill totals, with additional evaluation using K/D ratio, accuracy, wins, and win rate.

The analysis identifies the top five players by kills as well as the bottom five players by kills.

### K/D Ratio Analysis

A K/D ratio was calculated using:

```python
df["KD"] = df["Kills"] / df["Deaths"]
```

Players with a K/D ratio greater than 3 were also isolated for further performance analysis.

### Win Rate Analysis

Win rate was calculated using:

```python
df["WinRate"] = df["Wins"] / df["Matches"]
```

This provides a normalized measure of winning performance across players with different numbers of matches.

### Country-Level Analysis

The project aggregates player performance by country, including:

- Average kills
- Average K/D ratio

For example, the notebook calculates average K/D by country using Pandas `groupby()`.

### Weapon Analysis

Weapon-level analysis includes calculating average win rate by weapon.

---

## Dashboard

The project combines multiple visualizations into a single **Call of Duty Player Analytics Dashboard**.

The notebook also generates a high-resolution dashboard image:

```text
cod_analytics_dashboard.png
```

The dashboard is exported at 300 DPI for presentation and portfolio use.

---

## Technology Stack

- **Python**
- **Pandas** — Data manipulation and analysis
- **Matplotlib** — Data visualization
- **Jupyter Notebook**
- **CSV** — Dataset source

Matplotlib is explicitly used in the notebook for visualization.

---

## Project Structure

```text
call-of-duty-player-performance-analytics/
│
├── Call of Duty Player Analytics Dashboard(2).ipynb
├── cod_players.csv
├── cod_analytics_dashboard.png
└── README.md
```

---

## Dataset

The analysis uses a CSV dataset loaded into a Pandas DataFrame:

```python
df = pd.read_csv("cod_players.csv")
```

The dataset contains 1,000 observations and the following original fields:

```text
Player
Country
Kills
Deaths
Wins
Matches
Accuracy
Weapon
```



---

## Example Performance Statistics

Across the 1,000 player records, the notebook calculates the following descriptive statistics:

- Average kills: **140.178**
- Average deaths: **65.824**
- Average wins: **38.628**
- Average matches: **65.199**
- Average accuracy: **58.2563**
- Maximum kills: **250**
- Maximum wins: **80**
- Maximum accuracy: **95.0**



---

## Key Analytical Finding

The highest recorded kill total in the dataset is **250 kills**. Three players in the displayed top-three result achieved this total, with different K/D ratios and win rates, demonstrating why evaluating player performance using a single metric can be misleading.

---

## Purpose

This project demonstrates practical data-analysis skills including:

- Data ingestion
- Data inspection
- Descriptive statistics
- Feature engineering
- Performance metric calculation
- Filtering and ranking
- Grouped aggregation
- Comparative analysis
- Data visualization
- Dashboard development

It is designed as a portfolio project demonstrating the application of Python-based analytics to a gaming performance dataset.

---

## Author

**Jehosaphat Brobbey Impiani**

Aspiring Data Scientist | Machine Learning Engineer

---

## License

This project is intended for educational and portfolio purposes.
