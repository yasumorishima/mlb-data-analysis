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

1. **Pitcher Performance Analysis**
   - Pitch type statistics
   - ERA and K/9 analysis
   - Season trends

2. **Batter Performance Analysis**
   - Batting average by situation
   - Home run trends
   - On-base percentage analysis

3. **Team Performance Visualization**
   - Win/loss records
   - Run differential
   - League standings

## 📁 Project Structure
```
mlb-data-analysis/
├── notebooks/
│   ├── 01_data_collection.ipynb
│   ├── 02_data_analysis.ipynb
│   └── 03_visualization.ipynb
├── data/
│   └── sample_data.csv
├── images/
│   └── visualization_examples.png
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
