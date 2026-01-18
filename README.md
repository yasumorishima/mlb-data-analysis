# MLB Data Analysis

Professional-grade MLB data analysis with focus on practical scouting, performance tracking, injury prevention, and image analysis.
(実用的なスカウティング、パフォーマンス追跡、怪我予防、画像分析に焦点を当てたプロフェッショナルレベルのMLBデータ解析)

## 🎯 Project Overview

This project demonstrates practical data analysis skills through real-world baseball analytics. All analyses use Python and MLB Statcast data to extract actionable insights for player evaluation, strategic planning, and performance monitoring. Includes both statistical analysis and computer vision techniques.

(実際の野球分析を通じて実践的なデータ解析スキルを実証するプロジェクトです。Pythonと MLB Statcastデータを使用して、選手評価、戦略立案、パフォーマンスモニタリングのための実用的な洞察を抽出します。統計分析とコンピュータビジョン技術の両方を含みます。)

## 🛠️ Tech Stack

- **Python 3.x**
- **pybaseball**: MLB Statcast data acquisition
- **pandas**: Data processing and analysis
- **matplotlib / seaborn**: Statistical visualization
- **bar_chart_race**: Animated visualizations
- **numpy**: Numerical computing
- **PIL (Pillow)**: Image processing
- **scikit-learn**: Machine learning (KMeans clustering)
- **Jupyter Notebook**: Interactive analysis environment

## 📊 Analysis Portfolio

### 1. [WBC 2023: Pre-Game Scouting Report - Patrick Sandoval](./notebooks/wbc_2023_sandoval_scouting.ipynb) ⭐ FEATURED

![Sandoval Pitch Usage by Batter Side](./docs/image/sandoval_pitch_usage.png)
*Key Finding: Against left-handed batters, Sandoval throws sliders 49.2% of the time - nearly half of all pitches.*
*(重要な発見: 左打者に対して、サンドバルはスライダーを49.2%の割合で投げる - ほぼ半分の投球)*

![Sandoval Hit Distribution](./docs/image/sandoval_hit_distribution.png)
*Key Finding: No left-handed batter hit a home run off Sandoval in the previous season.*
*(重要な発見: 前シーズン、左打者は誰もサンドバルからホームランを打っていない)*

**Real-world application**: Pre-game scouting analysis of Mexico pitcher Patrick Sandoval conducted before the 2023 World Baseball Classic Japan vs. Mexico semifinal game.

(実際の応用例: 2023年ワールド・ベースボール・クラシック準決勝、日本対メキシコ戦前に実施したメキシコ投手パトリック・サンドバルの試合前スカウティング分析)

**Analysis Components:**

**Pitch Repertoire Analysis** (投球レパートリー分析)
- 5 pitch types identified: Changeup (CH), Sinker (SI), 4-Seam Fastball (FF), Slider (SL), Curveball (CU)
- Pitch usage frequency by batter handedness (打者の左右別投球頻度)
- Strike zone location mapping for each pitch type (各球種のストライクゾーン配球マップ)

**Performance Benchmarking** (パフォーマンスベンチマーク)
- Velocity comparison: Sandoval vs. MLB average by pitch type
- Spin rate analysis: Individual vs. league standards
- Statistical significance testing (mean ± standard deviation)

**Strategic Insights** (戦略的洞察)
- Left-handed vs. right-handed batter tendencies
- Hit distribution patterns (singles, doubles, triples, home runs)
- Batting average and home run vulnerability by batter side
- Visual heat maps of pitch locations and outcomes

**Tools:** pybaseball, pandas, matplotlib, seaborn, numpy

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yasumorishima/mlb-data-analysis/blob/main/notebooks/wbc_2023_sandoval_scouting.ipynb)

**Data Period:** 2022 MLB Season (March 30 - December 31, 2022)  
**Analysis Date:** March 2023 (pre-WBC)  
**Practical Value:** Data-driven game preparation and strategic planning
(実用的価値: データに基づく試合準備と戦略立案)

**Key Findings Example:**
- Identified pitch location tendencies vs. left/right batters
- Quantified velocity differentials from league average
- Mapped vulnerable zones for offensive strategy

---

### 2. [Trevor Bauer Set Position Image Analysis (2023)](./notebooks/bauer_set_position_analysis_2023.ipynb) ⭐ - IMAGE PROCESSING

![Bauer Set Position Analysis](./docs/image/bauer_set_position.png)
*Key Finding: K-means clustering detected potential "tells" in glove position across different pitch types.*
*(重要な発見: K-meansクラスタリングにより、球種ごとのグラブ位置に癖がある可能性を検出)*

**Real-world application**: Image-based analysis of pitcher's set position to detect potential "tells" or mechanical inconsistencies that batters might exploit.

(実際の応用例: 打者が利用できる可能性のある「癖」や機械的な不整合を検出するための、投手のセットポジションの画像ベース分析)

**Background:**
In 2023, when Trevor Bauer (Yokohama DeNA BayStars) was hit hard in a game against Hiroshima, this analysis was conducted to investigate whether there were detectable differences in his set position across different pitch types.

(背景: 2023年、トレバー・バウアー(横浜DeNAベイスターズ)が広島戦で打ち込まれた際、球種ごとのセットポジションに検出可能な違いがあるかどうかを調査するために実施した分析)

**Analysis Methodology:**

**Image Processing Pipeline** (画像処理パイプライン)
1. Background removal (green field transparency using RGB thresholds)
   - (背景除去 - RGBしきい値を使用した緑フィールドの透過処理)
2. Frame-by-frame difference detection (フレーム間差分検出)
3. Pixel-level comparison across pitch types (球種間のピクセルレベル比較)
4. Statistical clustering of difference regions (差分領域の統計的クラスタリング)

**Computer Vision Techniques** (コンピュータビジョン技術)
- RGB channel processing and alpha compositing
- Image differencing with threshold-based filtering (threshold = 250)
- K-means clustering (n_clusters=4) to identify regions of maximum variance
- Visualization of difference hotspots with circular markers

**Analysis Workflow**
- Compare each pitch type's frames against the first frame of that pitch type
- Extract pixels with significant differences (>250 RGB delta)
- Cluster difference points to identify key body position variations
- Visualize results with red highlighting and blue cluster centers

**Tools:** Python, PIL (Pillow), NumPy, scikit-learn (KMeans), matplotlib

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yasumorishima/mlb-data-analysis/blob/main/notebooks/bauer_set_position_analysis_2023.ipynb)

**Technical Stack:**
- Image processing: PIL (Pillow), NumPy arrays
- Machine learning: K-means clustering for spatial analysis
- Data visualization: matplotlib with patches overlay

**Manufacturing Applications:** (製造業への応用)
This image processing methodology directly applies to:
- **Automated visual inspection**: Defect detection on production lines
  - (自動外観検査: 生産ラインでの欠陥検出)
- **Quality control**: Comparing products against reference standards
  - (品質管理: 基準との製品比較)
- **Anomaly detection**: Identifying deviations from normal patterns
  - (異常検知: 正常パターンからの逸脱の特定)
- **Process monitoring**: Tracking visual changes over time
  - (プロセス監視: 視覚的変化の経時追跡)

---

### 3. [Shohei Ohtani Batting Analysis (2022)](./notebooks/ohtani_batting_analysis_2022.ipynb)

![Ohtani Batting Heatmap](./docs/image/ohtani_batting_heatmap.png)
*Key Finding: High concentration of hits through second base area - this likely explains why teams deployed the "Ohtani Shift" with defensive positioning in that zone.*
*(重要な発見: セカンド付近を通るヒットが集中している - これがチームが「大谷シフト」でそのゾーンに守備を配置した理由と推測される)*

Comprehensive analysis of Shohei Ohtani's batting performance during his 2022 MVP season.
(大谷翔平の2022年MVP シーズンにおける打撃パフォーマンスの包括的分析)

**Key Features:**
- Batted ball direction analysis by pitch location (投球位置別の打球方向分析)
- Hit distribution across strike zone (ストライクゾーン全体のヒット分布)
- Performance visualization with heat maps
- Contact quality metrics

**Tools:** pybaseball, pandas, matplotlib, seaborn

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yasumorishima/mlb-data-analysis/blob/main/notebooks/ohtani_batting_analysis_2022.ipynb)

---

### 4. [MLB Home Run Race 2024](./notebooks/mlb_home_run_race_2024.ipynb)

https://github.com/yasumorishima/mlb-data-analysis/raw/main/docs/image/mlb_hr_race_2024.mp4

*Dynamic bar chart race showing the 2024 home run leaders throughout the season.*
*(2024年シーズンを通じたホームランリーダーを示す動的バーチャートレース)*

Animated visualization of the 2024 MLB home run race throughout the season.
(2024年MLBシーズンを通じたホームラン競争のアニメーション可視化)

**Key Features:**
- Dynamic bar chart race animation (動的バーチャートレースアニメーション)
- Top 10 home run leaders tracking
- Regular season data (March 20 - October 1, 2024)
- Player name mapping and data cleaning
- Cumulative progression visualization

**Tools:** pybaseball, bar_chart_race, matplotlib, pandas, numpy

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yasumorishima/mlb-data-analysis/blob/main/notebooks/mlb_home_run_race_2024.ipynb)

**Output:** MP4 animation file

---

### 5. [Shohei Ohtani Injury Precursor Analysis (2023)](./notebooks/ohtani_injury_analysis_2023.ipynb)

![Ohtani Injury Precursor Analysis](./docs/image/ohtani_injury_analysis.png)
*Key Finding: Combining multiple parameters (release position × spin rate) may reveal injury precursors - note the increasing outliers (outside ±2σ) as the season progressed.*
*(重要な発見: 複数のパラメーターを組み合わせる（リリース位置×スピンレート）ことで、怪我の予兆が見える可能性がある - シーズン後半に向けて±2σ外の外れ値が増加している点に注目)*

Statistical analysis of pitching metrics to detect potential injury warning signs.
(潜在的な怪我の警告サインを検出するための投球指標の統計分析)

**Key Features:**
- Time-series analysis across 23 game dates (2023 season)
  - (23試合日にわたる時系列分析)
- Multi-parameter tracking (15+ metrics):
  - Release speed, spin rate, extension
  - Release position (X, Y, Z)
  - Spin axis, plate location
  - Pitch movement (pfx_x, pfx_z)
  - Velocity and acceleration components
- Anomaly detection (Average ± 2σ methodology)
  - (異常検知 - 平均±2σ手法)
- Before/after comparison (June 27, 2023 baseline)
- Pitch type analysis (FF, SL, FS, ST, CU, SI, FC)

**Tools:** pybaseball, pandas, matplotlib, seaborn, numpy

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yasumorishima/mlb-data-analysis/blob/main/notebooks/ohtani_injury_analysis_2023.ipynb)

**Analysis Period:** March 30 - August 23, 2023 (23 starts)

**Methodology:**
- Baseline establishment from pre-June 27 data
- Statistical outlier detection (統計的外れ値検出)
- Monthly trend aggregation
- Multi-dimensional correlation analysis

---

## 📁 Project Structure

```
mlb-data-analysis/
├── notebooks/
│   ├── wbc_2023_sandoval_scouting.ipynb      # Pre-game scouting
│   ├── bauer_set_position_analysis_2023.ipynb # Image analysis (NEW)
│   ├── ohtani_batting_analysis_2022.ipynb    # Batting analysis
│   ├── mlb_home_run_race_2024.ipynb          # Animation
│   └── ohtani_injury_analysis_2023.ipynb     # Injury prediction
├── requirements.txt
└── README.md
```

## 🚀 Getting Started

### Installation

```bash
pip install pybaseball pandas matplotlib seaborn bar_chart_race numpy jupyter pillow scikit-learn
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

### Technical Skills (技術スキル)
- **Data Acquisition**: MLB Statcast API integration
- **Statistical Analysis**: Mean, standard deviation, outlier detection
  - (統計分析: 平均、標準偏差、外れ値検出)
- **Image Processing**: Background removal, pixel-level differencing, alpha compositing
  - (画像処理: 背景除去、ピクセルレベル差分、アルファ合成)
- **Machine Learning**: K-means clustering for spatial analysis
  - (機械学習: 空間分析のためのK-meansクラスタリング)
- **Data Visualization**: Multi-plot layouts, heat maps, animations
- **Time-Series Analysis**: Trend detection, baseline comparison
  - (時系列分析: トレンド検出、ベースライン比較)
- **Data Cleaning**: Handling missing values, data validation
- **Comparative Analysis**: Individual vs. population benchmarking

### Domain Knowledge (ドメイン知識)
- **Baseball Analytics**: Pitch tracking, biomechanics, strategic implications
- **Scouting Methodology**: Pre-game preparation, opponent analysis
  - (スカウティング手法: 試合前準備、対戦相手分析)
- **Performance Metrics**: ERA, batting average, spin rates, release points
- **Injury Prevention**: Biomechanical marker interpretation
  - (怪我予防: バイオメカニクス指標の解釈)
- **Computer Vision**: Motion analysis, pattern recognition
  - (コンピュータビジョン: 動作分析、パターン認識)

### Business Applications (ビジネス応用)
- **Pre-Game Scouting**: Actionable intelligence for strategic planning
  - (試合前スカウティング: 戦略立案のための実用的インテリジェンス)
- **Competitive Analysis**: Benchmarking against industry standards
  - (競合分析: 業界標準とのベンチマーク)
- **Trend Detection**: Early warning systems for performance degradation
  - (トレンド検出: パフォーマンス低下の早期警告システム)
- **Data-Driven Decision Making**: Evidence-based recommendations
  - (データ駆動型意思決定: エビデンスに基づく推奨)
- **Visual Inspection**: Automated quality control systems
  - (外観検査: 自動品質管理システム)

## 🔬 Analysis Highlights

### Real-World Impact: WBC 2023 Scouting

The Patrick Sandoval scouting report demonstrates **practical application of data analysis** for high-stakes decision making:
(パトリック・サンドバルのスカウティングレポートは、高リスクの意思決定における**データ分析の実践的応用**を示しています)

**Problem**: Japan faces Mexico in WBC semifinals - need strategic edge  
**Solution**: Comprehensive data analysis of opposing pitcher  
**Outcome**: Actionable insights on pitch tendencies, vulnerable zones, strategic approach

**Transferable to Business:** (ビジネスへの転用)
- Competitive intelligence gathering (競合インテリジェンス収集)
- Market entry strategy (市場参入戦略)
- Risk assessment (リスク評価)
- Strategic planning under time pressure (時間的制約下での戦略立案)

---

### Computer Vision: Bauer Set Position Analysis

The Trevor Bauer image analysis demonstrates **computer vision techniques** applied to sports:
(トレバー・バウアーの画像分析は、スポーツに応用された**コンピュータビジョン技術**を示しています)

**Problem**: Pitcher getting hit hard - investigate mechanical tells  
**Solution**: Image-based difference detection across pitch types  
**Outcome**: Visual identification of body position variations

**Transferable to Manufacturing:** (製造業への転用)
- **Automated Visual Inspection**: Product defect detection
  - (自動外観検査: 製品欠陥検出)
- **Quality Control**: Reference-based comparison systems
  - (品質管理: 基準ベースの比較システム)
- **Anomaly Detection**: Statistical clustering of deviations
  - (異常検知: 逸脱の統計的クラスタリング)
- **Process Monitoring**: Frame-by-frame analysis of production
  - (プロセス監視: 生産のフレーム単位分析)

---

### Injury Prevention Research

The Ohtani 2023 analysis explores **predictive analytics** for injury prevention:
(大谷2023年分析は、怪我予防のための**予測分析**を探求しています)

**Hypothesis**: Can statistical anomalies in pitching metrics predict injury risk?  
**Method**: Multi-parameter tracking with ±2σ threshold detection  
**Application**: Early warning system for biomechanical stress

**Transferable to Manufacturing:** (製造業への転用)
- Predictive maintenance (予知保全)
- Quality control (品質管理)
- Process monitoring (プロセス監視)
- Anomaly detection systems (異常検知システム)

---

## 💼 Professional Value

### Why These Analyses Matter for Business (これらの分析がビジネスにとって重要な理由)

**1. WBC Scouting Analysis**
- Demonstrates ability to deliver actionable insights under deadline
  - (期限内に実用的な洞察を提供する能力を示す)
- Shows comparative analysis skills (individual vs. population)
- Proves data-driven decision-making capability
- **Business Parallel**: Competitive intelligence, market analysis

**2. Bauer Image Analysis**
- Exhibits computer vision and image processing skills
  - (コンピュータビジョンと画像処理スキルを示す)
- Shows ability to apply ML clustering to visual data
- Demonstrates creative problem-solving with unstructured data
- **Business Parallel**: Automated inspection, quality control, visual defect detection
  - (自動検査、品質管理、外観欠陥検出)

**3. Injury Prediction Analysis**
- Exhibits predictive analytics methodology
  - (予測分析手法を示す)
- Shows multi-variable monitoring capability
- Demonstrates statistical rigor (±2σ methodology)
- **Business Parallel**: Predictive maintenance, quality control
  - (予知保全、品質管理)

**4. Animation & Visualization**
- Proves ability to communicate data insights visually
  - (データ洞察を視覚的に伝える能力を証明)
- Shows technical breadth (multiple libraries)
- Demonstrates attention to presentation quality
- **Business Parallel**: Executive dashboards, stakeholder reports
  - (経営ダッシュボード、ステークホルダーレポート)

---

## 🔗 References

- [pybaseball Documentation](https://github.com/jldbc/pybaseball)
- [MLB Statcast Data](https://baseballsavant.mlb.com/)
- [Baseball Savant - Patrick Sandoval](https://baseballsavant.mlb.com/savant-player/patrick-sandoval-663776)
- [2023 World Baseball Classic](https://www.mlb.com/world-baseball-classic)
- [scikit-learn KMeans](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html)
- [Pillow (PIL) Documentation](https://pillow.readthedocs.io/)

---

**Portfolio Purpose**: This project demonstrates practical data analysis capabilities with real-world applications, statistical rigor, computer vision techniques, and business value generation through actionable insights.

(ポートフォリオの目的: このプロジェクトは、実世界への応用、統計的厳密性、コンピュータビジョン技術、そして実用的な洞察によるビジネス価値創出を伴う、実践的なデータ分析能力を示しています。)

*Personal learning project showcasing data analysis, image processing, visualization, and strategic thinking skills.*
*(データ分析、画像処理、可視化、戦略的思考スキルを示す個人学習プロジェクト)*
