# MLB Data Analysis

Professional-grade MLB data analysis with focus on practical scouting, performance tracking, and injury prevention.

## 🎯 Project Overview

This project demonstrates practical data analysis skills through real-world baseball analytics. All analyses use Python and MLB Statcast data to extract actionable insights for player evaluation, strategic planning, and performance monitoring.

## 🛠️ Tech Stack

- **Python 3.x**
- **pybaseball**: MLB Statcast data acquisition
- **pandas**: Data processing and analysis
- **matplotlib / seaborn**: Statistical visualization
- **bar_chart_race**: Animated visualizations
- **numpy**: Numerical computing
- **Jupyter Notebook**: Interactive analysis environment

## 📊 Analysis Portfolio

### 1. [WBC 2023: Pre-Game Scouting Report - Patrick Sandoval](./notebooks/wbc_2023_sandoval_scouting.ipynb) ⭐ FEATURED

**Real-world application**: Pre-game scouting analysis of Mexico pitcher Patrick Sandoval conducted before the 2023 World Baseball Classic Japan vs. Mexico semifinal game.

**Analysis Components:**

**Pitch Repertoire Analysis**
- 5 pitch types identified: Changeup (CH), Sinker (SI), 4-Seam Fastball (FF), Slider (SL), Curveball (CU)
- Pitch usage frequency by batter handedness
- Strike zone location mapping for each pitch type

**Performance Benchmarking**
- Velocity comparison: Sandoval vs. MLB average by pitch type
- Spin rate analysis: Individual vs. league standards
- Statistical significance testing (mean ± standard deviation)

**Strategic Insights**
- Left-handed vs. right-handed batter tendencies
- Hit distribution patterns (singles, doubles, triples, home runs)
- Batting average and home run vulnerability by batter side
- Visual heat maps of pitch locations and outcomes

**Tools:** pybaseball, pandas, matplotlib, seaborn, numpy

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yasumorishima/mlb-data-analysis/blob/main/notebooks/wbc_2023_sandoval_scouting.ipynb)

**Data Period:** 2022 MLB Season (March 30 - December 31, 2022)  
**Analysis Date:** March 2023 (pre-WBC)  
**Practical Value:** Data-driven game preparation and strategic planning

**Key Findings Example:**
- Identified pitch location tendencies vs. left/right batters
- Quantified velocity differentials from league average
- Mapped vulnerable zones for offensive strategy

---

### 2. [Shohei Ohtani Batting Analysis (2022)](./notebooks/ohtani_batting_analysis_2022.ipynb)

Comprehensive analysis of Shohei Ohtani's batting performance during his 2022 MVP season.

**Key Features:**
- Batted ball direction analysis by pitch location
- Hit distribution across strike zone
- Performance visualization with heat maps
- Contact quality metrics

**Tools:** pybaseball, pandas, matplotlib, seaborn

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yasumorishima/mlb-data-analysis/blob/main/notebooks/ohtani_batting_analysis_2022.ipynb)

---

### 3. [MLB Home Run Race 2024](./notebooks/mlb_home_run_race_2024.ipynb)

Animated visualization of the 2024 MLB home run race throughout the season.

**Key Features:**
- Dynamic bar chart race animation
- Top 10 home run leaders tracking
- Regular season data (March 20 - October 1, 2024)
- Player name mapping and data cleaning
- Cumulative progression visualization

**Tools:** pybaseball, bar_chart_race, matplotlib, pandas, numpy

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yasumorishima/mlb-data-analysis/blob/main/notebooks/mlb_home_run_race_2024.ipynb)

**Output:** MP4 animation file

---

### 4. [Shohei Ohtani Injury Precursor Analysis (2023)](./notebooks/ohtani_injury_analysis_2023.ipynb)

Statistical analysis of pitching metrics to detect potential injury warning signs.

**Key Features:**
- Time-series analysis across 23 game dates (2023 season)
- Multi-parameter tracking (15+ metrics):
  - Release speed, spin rate, extension
  - Release position (X, Y, Z)
  - Spin axis, plate location
  - Pitch movement (pfx_x, pfx_z)
  - Velocity and acceleration components
- Anomaly detection (Average ± 2σ methodology)
- Before/after comparison (June 27, 2023 baseline)
- Pitch type analysis (FF, SL, FS, ST, CU, SI, FC)

**Tools:** pybaseball, pandas, matplotlib, seaborn, numpy

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yasumorishima/mlb-data-analysis/blob/main/notebooks/ohtani_injury_analysis_2023.ipynb)

**Analysis Period:** March 30 - August 23, 2023 (23 starts)

**Methodology:**
- Baseline establishment from pre-June 27 data
- Statistical outlier detection
- Monthly trend aggregation
- Multi-dimensional correlation analysis

---

## 📁 Project Structure

```
mlb-data-analysis/
├── notebooks/
│   ├── wbc_2023_sandoval_scouting.ipynb      # Featured analysis
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

### For bar_chart_race (Ubuntu/Debian):
```bash
sudo apt-get update && sudo apt-get install -y ffmpeg
```

### Quick Start

```python
from pybaseball import statcast
import pandas as pd

# Get Statcast data for date range
data = statcast(start_dt='2024-04-01', end_dt='2024-04-30')

# Filter by player ID
player_data = data[data['pitcher'] == 663776]  # Patrick Sandoval

# Basic analysis
print(player_data['pitch_type'].value_counts())
```

## 🎓 Skills Demonstrated

### Technical Skills
- **Data Acquisition**: MLB Statcast API integration
- **Statistical Analysis**: Mean, standard deviation, outlier detection
- **Data Visualization**: Multi-plot layouts, heat maps, animations
- **Time-Series Analysis**: Trend detection, baseline comparison
- **Data Cleaning**: Handling missing values, data validation
- **Comparative Analysis**: Individual vs. population benchmarking

### Domain Knowledge
- **Baseball Analytics**: Pitch tracking, biomechanics, strategic implications
- **Scouting Methodology**: Pre-game preparation, opponent analysis
- **Performance Metrics**: ERA, batting average, spin rates, release points
- **Injury Prevention**: Biomechanical marker interpretation

### Business Applications
- **Pre-Game Scouting**: Actionable intelligence for strategic planning
- **Competitive Analysis**: Benchmarking against industry standards
- **Trend Detection**: Early warning systems for performance degradation
- **Data-Driven Decision Making**: Evidence-based recommendations

## 🔬 Analysis Highlights

### Real-World Impact: WBC 2023 Scouting

The Patrick Sandoval scouting report demonstrates **practical application of data analysis** for high-stakes decision making:

**Problem**: Japan faces Mexico in WBC semifinals - need strategic edge
**Solution**: Comprehensive data analysis of opposing pitcher
**Outcome**: Actionable insights on pitch tendencies, vulnerable zones, strategic approach

**Transferable to Business:**
- Competitive intelligence gathering
- Market entry strategy
- Risk assessment
- Strategic planning under time pressure

### Injury Prevention Research

The Ohtani 2023 analysis explores **predictive analytics** for injury prevention:

**Hypothesis**: Can statistical anomalies in pitching metrics predict injury risk?
**Method**: Multi-parameter tracking with ±2σ threshold detection
**Application**: Early warning system for biomechanical stress

**Transferable to Manufacturing:**
- Predictive maintenance
- Quality control
- Process monitoring
- Anomaly detection systems

## 💼 Professional Value

### Why These Analyses Matter for Business

**1. WBC Scouting Analysis**
- Demonstrates ability to deliver actionable insights under deadline
- Shows comparative analysis skills (individual vs. population)
- Proves data-driven decision-making capability
- **Business Parallel**: Competitive intelligence, market analysis

**2. Injury Prediction Analysis**
- Exhibits predictive analytics methodology
- Shows multi-variable monitoring capability
- Demonstrates statistical rigor (±2σ methodology)
- **Business Parallel**: Predictive maintenance, quality control

**3. Animation & Visualization**
- Proves ability to communicate data insights visually
- Shows technical breadth (multiple libraries)
- Demonstrates attention to presentation quality
- **Business Parallel**: Executive dashboards, stakeholder reports

## 🔗 References

- [pybaseball Documentation](https://github.com/jldbc/pybaseball)
- [MLB Statcast Data](https://baseballsavant.mlb.com/)
- [Baseball Savant - Patrick Sandoval](https://baseballsavant.mlb.com/savant-player/patrick-sandoval-663776)
- [2023 World Baseball Classic](https://www.mlb.com/world-baseball-classic)

---

**Portfolio Purpose**: This project demonstrates practical data analysis capabilities with real-world applications, statistical rigor, and business value generation through actionable insights.

*Personal learning project showcasing data analysis, visualization, and strategic thinking skills.*
