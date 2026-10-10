# FIFA World Cup Data Analysis (1930–2026)

**Historical Scoring Trends, Match Competitiveness & SQL Exploration**

## Project Overview

This project explores FIFA World Cup scoring patterns across tournament history and compares match competitiveness in the 2022 and 2026 tournaments. It combines **Python/pandas exploratory analysis** with a companion **DuckDB SQL notebook** to demonstrate reproducible data analysis, querying, interpretation, and communication of findings.

The analysis examines statistical associations and trends; it does not claim that World Cup expansion caused observed changes in match competitiveness.

## Tools & Skills

**Python · pandas · SQL · DuckDB · Matplotlib · Google Colab · GitHub**

- **Python/pandas:** data loading, validation, grouping, calculating metrics, and visualization
- **SQL:** filtering, aggregation, `GROUP BY`, `HAVING`, `INNER JOIN`, common table expressions (CTEs), and `LAG()` window functions
- **Analytical reasoning:** normalized comparisons, identifying limitations, and interpreting results without overclaiming causation

## Project Notebooks

| Notebook | Description |
|---|---|
| [01 — World Cup Exploration (Python)](01_world_cup_exploration.ipynb) | Data quality checks, historical scoring averages, 2022 vs. 2026 competitiveness comparisons, and visualizations |
| [02 — SQL Practice & Analysis (DuckDB)](02_sql_practice.ipynb) | World Cup aggregations, `HAVING` filters, tournament-to-tournament scoring comparisons with `LAG()`, and an introductory player-performance `JOIN` exercise |

**Note:** The player-scouting example in the SQL notebook uses **fictional players** only to demonstrate joining tables and calculating key passes per 90 minutes. It is not a real player evaluation or transfer recommendation.

## Questions Investigated

1. How have World Cup scoring averages changed across tournaments?
2. How did the proportion of one-sided matches compare between 2022 and 2026?
3. Which tournament years met selected scoring thresholds?
4. How can SQL be used to reproduce summaries, combine tables, and compare periods?

## Selected Findings

| Metric | 2022 | 2026 |
|---|---:|---:|
| Matches | 64 | 104 |
| Goals per match | 2.69 | 2.96 |
| Average absolute goal margin | 1.41 | 1.56 |
| Matches decided by 3+ goals | 14.06% | 21.15% |

- **1954** had the highest historical goals-per-match average in the dataset (**5.38**), while **1990** had the lowest (**2.21**).
- The share of matches decided by three or more goals was **7.09 percentage points higher** in 2026 than in 2022.
- Since the tournaments contained different numbers of matches, **percentages and per-match averages** provide more meaningful comparisons than raw counts alone.
- The SQL exploration identifies six tournaments (1930–1958) that averaged **more than three goals per match**.

These findings are descriptive. They do not, on their own, establish *why* scoring or competitiveness changed.

## Data Quality & Reproducibility

The Python analysis checked for missing values, duplicate records, and invalid negative scores. The analyzed dataset contains **1,068 World Cup matches** and **3,028 goals** across the included tournament years.

**Source:** [International Football Results — martj42/international_results](https://github.com/martj42/international_results)

Both notebooks use the following fixed CSV version rather than an automatically changing latest release:

[View the pinned results.csv snapshot](https://raw.githubusercontent.com/martj42/international_results/b7a3a8ee5d37780c6a03101c188658fd439e241d/results.csv)

### Running the notebooks

1. Open a notebook using its link above and select **Open in Colab** (or upload it to [Google Colab](https://colab.research.google.com/)).
2. Select **Runtime → Run all** to execute the code in order.
3. An internet connection is needed for dependencies and the pinned CSV download. The SQL notebook creates DuckDB tables within the Colab session; rerun its setup cell if the session restarts.

The notebooks contain saved outputs for inspection, but outputs are tied to the dataset snapshot and notebook execution state.

## Limitations & Next Steps

Historical results do not directly measure team tactics, player quality, formations, or tournament-adjusted competitive balance. Comparing two tournament years cannot isolate the effect of expansion from other changes. More detailed team-level data and explicit analytical assumptions would be needed to test causal explanations.

This repository demonstrates exploratory and SQL fundamentals. Subsequent portfolio projects will focus on **decision-support analyses** in sports performance, sports business, and other industries.

## Author

**Juan Vasquez**  
M.S. Information Systems — Data Analytics  
B.S. Recreation & Sports Management

Interested in sports analytics, business intelligence, and data-driven decision-making.
