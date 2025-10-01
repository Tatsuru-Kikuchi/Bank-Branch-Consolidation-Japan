# Bank Branch Consolidation in Japan: Spatial-Temporal Boundary Analysis

This project analyzes the spatial and temporal boundaries of customer adjustment following bank branch consolidations in Japan, applying the diffusion-based boundary detection framework from [Regime-Switch-Dynamics](https://github.com/Tatsuru-Kikuchi/Regime-Swithch-Dynamics).

## Research Questions

1. **Spatial Boundary**: How far do customers travel to alternative branches after their local branch closes?
2. **Temporal Boundary**: How long does customer adjustment take after branch closure?
3. **Demographic Heterogeneity**: Do older customers (55+) exhibit different boundary patterns than younger customers?
4. **Network Effects**: How do branch networks and firm relationships moderate consolidation impacts?

## Context

- Japanese banks are consolidating branches for digital transformation (DX)
- Older people (55+) hold most financial assets but have lower digital adoption
- Regional demographic variation creates spatial heterogeneity in consolidation impacts
- Branch-enterprise relationships create network dependencies

## Data Sources

- Bank branch location data (2015-2024)
- Branch closure announcements from major banks
- Regional demographics from Statistics Bureau of Japan
- Financial Services Agency surveys on banking access

## Methodology

Applies three-stage boundary detection:
1. Difference-in-differences for direct effects of branch closure
2. Spatial decay estimation for geographic spillovers
3. Temporal decay estimation for adjustment dynamics

## Installation
### Clone this repository
```bash
git clone https://github.com/Tatsuru-Kikuchi/Bank-Branch-Consolidation-Japan.git
cd Bank-Branch-Consolidation-Japan
```

### Create virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### Install dependencies
```bash
pip install -r requirements.txt
```

### Install theoretical framework
```bash
pip install git+https://github.com/Tatsuru-Kikuchi/Regime-Swithch-Dynamics.git
```

## Project Structure
```
Bank-Branch-Consolidation-Japan/
├── data/
│   ├── raw/              # Raw data (not in git)
│   ├── processed/        # Cleaned data (not in git)
│   └── README.md         # Data documentation
├── code/
│   ├── data_collection/  # Scraping and compilation
│   ├── data_processing/  # Cleaning and panel construction
│   ├── analysis/         # Boundary estimation
│   └── visualization/    # Figures and tables
├── results/
│   ├── tables/
│   └── figures/
├── paper/
│   └── consolidation.tex
└── notebooks/            # Exploratory analysis
```
