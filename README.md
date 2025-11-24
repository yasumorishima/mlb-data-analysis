# MLB Data Analysis

MLB data analysis using pybaseball library

## 🎯 Project Overview

This project analyzes MLB (Major League Baseball) data using Python. The goal is to extract insights from player statistics, team performance, and game trends, with a focus on Shohei Ohtani's performance analysis.

## 🛠️ Tech Stack

- **Python 3.x**
- **pybaseball**: MLB data acquisition
- **pandas**: Data processing and analysis
- **matplotlib / seaborn**: Data visualization
- **bar_chart_race**: Animated bar chart race visualization
- **numpy**: Numerical computing
- **Jupyter Notebook**: Interactive analysis

## 📊 Analysis Contents

### [Shohei Ohtani Batting Analysis (2022)](./notebooks/ohtani_batting_analysis_2022.ipynb)

Analysis of Shohei Ohtani's batting performance in the 2022 season using pybaseball.

**Key Features:**
- Batted ball direction by pitch location
- Hit distribution across different zones
- Performance visualization with heatmaps

**Tools:** pybaseball, pandas, matplotlib, seaborn

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yasumorishima/mlb-data-analysis/blob/main/notebooks/ohtani_batting_analysis_2022.ipynb)

---

### [MLB Home Run Race 2024](./notebooks/mlb_home_run_race_2024.ipynb) ⭐ NEW

Animated bar chart race visualization of cumulative home runs during the 2024 MLB season.

**Key Features:**
- Real-time home run race animation (bar chart race)
- Top 10 home run leaders throughout the season
- Regular season data only (March 20 - October 1, 2024)
- Player name mapping from MLB IDs
- Cumulative home run tracking by date

**Tools:** pybaseball, bar_chart_race, matplotlib, pandas, numpy

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yasumorishima/mlb-data-analysis/blob/main/notebooks/mlb_home_run_race_2024.ipynb)

**Output:** MP4 animation file showing cumulative home run progression throughout the 2024 season

---

### [Shohei Ohtani Injury Precursor Analysis (2023)](./notebooks/ohtani_injury_analysis_2023.ipynb) ⭐ NEW

Comprehensive analysis of Shohei Ohtani's pitching data during the 2023 season to detect potential injury precursors through statistical analysis.

**Key Features:**
- Time-series analysis of pitching metrics (23 game dates in 2023 season)
- Multiple parameter tracking:
  - Release speed, spin rate, release extension
  - Release position (X, Y, Z coordinates)
  - Spin axis, plate location (X, Z)
  - Pitch movement (pfx_x, pfx_z)
  - Velocity components (vx0, vy0, vz0)
  - Acceleration components (ax, ay, az)
- Statistical analysis (Average ± 2σ)
- Comparison before and after June 27, 2023
- Pitch type distribution analysis (FF, SL, FS, ST, CU, SI, FC)
- Boxplots and scatter plots for trend detection

**Tools:** pybaseball, pandas, matplotlib, seaborn, numpy

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yasumorishima/mlb-data-analysis/blob/main/notebooks/ohtani_injury_analysis_2023.ipynb)

**Analysis Period:** March 30 - August 23, 2023 (23 pitching appearances)

**Methodology:**
- Baseline statistics calculated from data until June 27, 2023
- Anomaly detection using 2σ threshold
- Monthly aggregation for trend analysis
- Correlation analysis between release point and spin metrics

---

## 📁 Project Structure

```
mlb-data-analysis/
├── notebooks/
│   ├── ohtani_batting_analysis_2022.ipynb
│   ├── mlb_home_run_race_2024.ipynb
│   └── ohtani_injury_analysis_2023.ipynb
├── images/
│   └── visualization_examples.png
├── requirements.txt
└── README.md
```

## 🚀 Getting Started

### Installation

```bash
pip install pybaseball pandas matplotlib seaborn bar_chart_race numpy jupyter
```

### For Ubuntu/Debian users (required for bar_chart_race):
```bash
sudo apt-get update && sudo apt-get install -y ffmpeg
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
- Animated visualization techniques (bar chart race)
- Time-series analysis for injury detection
- Anomaly detection using statistical methods (±2σ)
- Multi-parameter correlation analysis
- Handling large datasets efficiently
- Pitch tracking data interpretation

## 🔬 Analysis Highlights

### Injury Precursor Detection
The 2023 analysis explores whether changes in pitching metrics can indicate potential injury risks. By tracking multiple parameters over time and comparing them to baseline statistics, we can identify statistically significant deviations that may warrant attention.

**Key Insights:**
- Systematic tracking of 15+ pitching parameters
- Statistical baseline establishment (pre-June 27, 2023)
- Anomaly detection through 2σ threshold
- Multi-dimensional correlation analysis

## 🔗 References

- [pybaseball documentation](https://github.com/jldbc/pybaseball)
- [MLB Statcast data](https://baseballsavant.mlb.com/)
- [bar_chart_race documentation](https://github.com/dexplo/bar_chart_race)
- [Baseball Savant - Shohei Ohtani](https://baseballsavant.mlb.com/savant-player/shohei-ohtani-660271)

---

*This is a personal learning project for data analysis practice.*
