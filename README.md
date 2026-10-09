# FIFA World Cup Data Analysis (1930–2026)

### Historical Scoring Trends and Match Competitiveness

## Project Overview

This project explores historical FIFA World Cup scoring patterns and examines whether the expansion from 32 to 48 participating teams in 2026 coincided with changes in match competitiveness.

Using Python and pandas, I analyzed international football match results, calculated tournament-level statistics, performed data quality checks, and created visualizations to communicate key findings.

## Tools Used

**Python | pandas | Matplotlib | Google Colab | GitHub**

## Research Questions

1. How have World Cup scoring averages changed throughout history?
2. Did one-sided matches become more frequent in the expanded 2026 World Cup?
3. What can match results tell us about tournament competitiveness?

## Key Findings

| Metric | 2022 | 2026 |
|---|---:|---:|
| Matches | 64 | 104 |
| Goals per match | 2.69 | 2.96 |
| Average absolute goal margin | 1.41 | 1.56 |
| Matches decided by 3+ goals | 14.06% | 21.15% |

Historically, 1954 recorded the highest scoring average at 5.38 goals per match, while 1990 recorded the lowest at 2.21.

Between 2022 and 2026, the proportion of matches decided by three or more goals increased by 7.09 percentage points. However, this comparison alone cannot establish whether tournament expansion caused the change.

## Data Validation

The analysis included checks for missing values, duplicate match records, and invalid negative scores.

Aggregate totals of 1,068 matches and 3,028 goals were also reconciled with published FIFA statistics.

## Dataset

[International Football Results — Mart Jürisoo](https://github.com/martj42/international_results)

The analysis uses match records classified as FIFA World Cup fixtures.

## View the Analysis

[View the complete Jupyter notebook](01_world_cup_exploration.ipynb)

The notebook includes Python code, calculations, visualizations, analytical interpretations, and conclusions.

## Limitations

The findings describe observed statistical patterns rather than proving their underlying causes. Additional research into national team strength, tournament formats, and individual match results would help evaluate the relationship between expansion and competitiveness.

The dataset is currently loaded from an externally maintained CSV, so future updates may affect reproducibility until the source version is fixed.

## Author

**Juan Vasquez**

M.S. Information Systems — Data Analytics

B.S. Recreation & Sports Management

Interested in sports analytics, business intelligence, and data-driven decision-making.
