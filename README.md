# MLB Data Analysis

MLB data analysis using pybaseball library

## 🎯 Project Overview

This project analyzes MLB (Major League Baseball) data using Python. The goal is to extract insights from player statistics, team performance, and game trends.

## 🛠️ Tech Stack

- **Python 3.x**
- **pybaseball**: MLB data acquisition
- **pandas**: Data processing and analysis
- **matplotlib / seaborn**: Data visualization
- **Jupyter Notebook**: Interactive analysis

## 📊 Analysis Contents

### [Shohei Ohtani Batting Analysis (2022)](./notebooks/ohtani_batting_analysis_2022.ipynb)

Analysis of Shohei Ohtani's batting performance in the 2022 season using pybaseball.

**Key Features:**
- Batted ball direction by pitch location
- Hit distribution across different zones
- Performance visualization

**Tools:** pybaseball, pandas, matplotlib

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yasumorishima/mlb-data-analysis/blob/main/notebooks/ohtani_batting_analysis_2022.ipynb)

---

### [MLB Home Run Race 2024](./notebooks/mlb_home_run_race_2024.ipynb) ⭐ NEW

Animated bar chart race visualization of cumulative home runs during the 2024 MLB season.

**Key Features:**
- Real-time home run race animation (bar chart race)
- Top 10 home run leaders throughout the season
- Regular season data only (March 20 - October 1, 2024)
- Player name mapping from MLB IDs

**Tools:** pybaseball, bar_chart_race, matplotlib, pandas

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yasumorishima/mlb-data-analysis/blob/main/notebooks/mlb_home_run_race_2024.ipynb)

**Output:** MP4 animation file showing cumulative home run progression

## 📁 Project Structure
```
mlb-data-analysis/
├── notebooks/
│   ├── ohtani_batting_analysis_2022.ipynb
│   ├── mlb_home_run_race_2024.ipynb
│   └── 
├── requirements.txt
└── README.md
```

## 🚀 Getting Started

### Installation
```bash
pip install pybaseball pandas matplotlib seaborn jupyter
```

### Usage
```python
from pybaseball import statcast
import pandas as pd

# Get data
data = statcast(start_dt='2024-04-01', end_dt='2024-04-30')

# Analyze
print(data.head())
```

## 📈 Sample Results

*(Add visualization images here)*

## 🎓 What I Learned

- MLB data structure and API usage
- Statistical analysis of sports data
- Data visualization best practices
- Handling large datasets efficiently

## 🔗 References

- [pybaseball documentation](https://github.com/jldbc/pybaseball)
- [MLB Statcast data](https://baseballsavant.mlb.com/)

---

*This is a personal learning project for data analysis practice.*
