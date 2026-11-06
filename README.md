# Call of Duty Player Performance Analytics Dashboard

A Python data analysis project exploring player performance through descriptive statistics, engineered metrics, and visualisation.

The analysis uses a dataset of 1,000 player records and produces charts summarising performance across players, countries, and weapon categories.

## Questions Explored

- Which players have the highest kill totals?
- How do kill/death ratios vary?
- How do win rates compare across players?
- Are there differences in the observed metrics across countries and weapons?

## Dataset

The repository includes `cod_players.csv` with eight original fields:

`Player`, `Country`, `Kills`, `Deaths`, `Wins`, `Matches`, `Accuracy`, and `Weapon`.

## Derived Metrics

- **K/D ratio:** kills divided by deaths.
- **Win rate:** wins divided by matches.

These ratios should be calculated only for records with valid nonzero denominators.

## Analysis Workflow

1. Load and inspect the dataset using Pandas.
2. Summarise distributions and check data quality.
3. Calculate performance indicators.
4. Rank and group players.
5. Compare metrics by country and weapon.
6. Present results using Matplotlib.

## Predictive modelling status

The notebook's earlier `PerformanceTier` classifier has been removed. The tier was derived from `PerformanceScore`, which was itself calculated from the same record's K/D ratio and win rate. Predicting that derived label from overlapping match statistics creates a circular target and does not demonstrate genuine future-performance prediction. This repository is therefore presented as descriptive player analytics, not a validated predictive model.

A future prediction version should use time-indexed match records, define a next-match outcome, and restrict predictors to information available before that match.

## Tools

Python, Pandas, Matplotlib, and Jupyter Notebook.

## Repository Contents

```text
.
├── Call of Duty Player Analytics Dashboard.ipynb
├── cod_players.csv
├── cod_analytics_dashboard.png
├── Distribution of player kills.png
├── Top 10 kills vs Death.png
├── top10_kills.png
└── README.md
```

## Dashboard Preview

![Call of Duty analytics dashboard](cod_analytics_dashboard.png)

## Run the Analysis

Install Python, Pandas, Matplotlib, and Jupyter Notebook. Open the notebook and execute its cells in order:

```bash
jupyter notebook
```

## Interpretation and Limitations

The analysis is descriptive. Comparisons across players and countries depend on the quality, representativeness, and provenance of the underlying dataset. The data source and collection methodology should be documented before drawing wider conclusions.

## Author

Jehosaphat Brobbey Impiani  
[GitHub](https://github.com/Slimjoey56)