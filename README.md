# Toronto Bikeshare Mobility Patterns (2018) — Python

Analysis of 1.9 million bikeshare trips in Toronto using pandas and NetworkX, including temporal patterns, station-level analytics, and network analysis with PageRank.

> A [PySpark version](https://github.com/laurabenkel/toronto-bikeshare-spark) of this analysis is also available, demonstrating the same logic using distributed computing.

## The problem

Understanding bikeshare usage patterns helps city planners optimize station placement, anticipate maintenance needs, and promote sustainable transport. This project analyzes a full year of Toronto's bikeshare ridership using standard Python data tools.

## Data

Download the four quarterly CSV files from [Kaggle](https://www.kaggle.com/jackywang529/toronto-bikeshare-data) and place them in the `data/` folder:

```
data/
├── Bike Share Toronto Ridership_Q1 2018.csv
├── Bike Share Toronto Ridership_Q2 2018.csv
├── Bike Share Toronto Ridership_Q3 2018.csv
└── Bike Share Toronto Ridership_Q4 2018.csv
```

The dataset contains ~1.9 million individual trips with origin/destination stations, timestamps, duration, and user type.

## Analysis

| Section | Technique | Purpose |
|---|---|---|
| Temporal analysis | Pivot tables, heatmap, seasonal profiles | Trip volume by hour × month |
| Station analytics | groupby + transform | Mean/min/max duration per station-hour-month, % deviation |
| Network analysis | NetworkX + PageRank | Identify structurally important stations |

## Key findings

- **Commuting peaks** at 8 AM and 5-6 PM are consistent across all months
- **Seasonal variation** of 5-10x between summer and winter
- **PageRank** identifies hub stations that are structurally central to the network

## Repository structure

```
├── README.md
├── .gitignore
├── data/                  ← download from Kaggle (not tracked)
└── notebooks/
    └── toronto_bikeshare_python.ipynb
```

## How to run

```bash
git clone https://github.com/laurabenkel/toronto-bikeshare-python.git
cd toronto-bikeshare-python
pip install pandas numpy matplotlib seaborn networkx
jupyter notebook notebooks/toronto_bikeshare_python.ipynb
```

Or upload the notebook and CSV files to [Google Colab](https://colab.research.google.com/) — no additional installs needed.

## Tools

Python · pandas · NetworkX · matplotlib · seaborn

## Author

**Laura Benkel Brander** — Sociologist & Data Scientist  
[LinkedIn](https://www.linkedin.com/in/laurabenkel)
