# Dynamic ELO-Based Ranking System for Badminton Players

A data-driven ranking system that models player strength dynamically using historical badminton match data and ELO-based rating updates.

## Overview

Traditional ranking systems often rely on accumulated points or fixed evaluation windows, which may not fully capture changes in a player's competitive strength over time. This project implements a Dynamic ELO-based ranking framework that updates player ratings sequentially as new match results become available.

The system processes historical badminton match data across multiple disciplines and constructs evolving player ratings based on competitive outcomes. The resulting framework can be used to analyze changes in player strength, compare competitors, and support downstream match prediction and performance analysis.

## Key Features

* Dynamic ELO rating updates based on historical match outcomes
* Sequential, time-aware processing of match data
* Player ranking across historical badminton competitions
* Support for multiple badminton disciplines
* Feature engineering for player-performance analysis
* Machine learning-based modeling using XGBoost
* Time-aware evaluation to reduce information leakage

## Dataset

The project uses historical badminton match data organized by discipline:

| File     | Discipline      |
| -------- | --------------- |
| `ms.csv` | Men's Singles   |
| `ws.csv` | Women's Singles |
| `md.csv` | Men's Doubles   |
| `wd.csv` | Women's Doubles |

Each dataset contains historical match information, including tournament details, match dates, players, match outcomes, scores, and additional match-level statistics.

The datasets are required to run the complete analysis pipeline.

## Methodology

The project follows the workflow below:

1. **Data Loading and Preprocessing**
   Historical match records are loaded and cleaned before analysis.

2. **Chronological Processing**
   Matches are processed sequentially to ensure that ratings are based only on information available before each match.

3. **Dynamic ELO Updates**
   Player ratings are updated after each match according to match outcomes and the relative strength of competitors.

4. **Ranking Analysis**
   The evolving ELO ratings are used to construct and analyze player rankings.

5. **Machine Learning Analysis**
   Engineered ranking and performance features are used for downstream predictive analysis with machine learning models.

6. **Evaluation**
   Time-aware evaluation methods are used to assess performance while minimizing data leakage.

## Project Structure

```text
dynamic-elo-ranking-system/
│
├── README.md
├── requirements.txt
│
├── notebooks/
│   └── dynamic_elo_ranking_system.ipynb
│
└── ├── md.csv
    ├── ms.csv
    ├── wd.csv
    └── ws.csv
```

## How to Run

### 1. Clone the repository

```bash
git clone git clone https://github.com/Rushipatel01092003/dynamic-elo-ranking-system.git
cd dynamic-elo-ranking-system
```

### 2. Create a virtual environment (recommended)

```bash
python -m venv venv
```

Activate the environment.

**Windows:**

```bash
venv\Scripts\activate
```

**macOS/Linux:**

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
notebooks/dynamic_elo_ranking_system.ipynb
```

Alternatively, the notebook can be opened directly in JupyterLab or Google Colab.

## Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* Matplotlib
* Jupyter Notebook

## Reproducibility

The repository includes the datasets required for the analysis pipeline. To reproduce the project:

1. Install the dependencies listed in `requirements.txt`.
2. Run the notebook sequentially from top to bottom.

## Results

The Dynamic ELO framework provides a mechanism for tracking changes in competitive player strength over time and generating rankings from historical match outcomes.

The complete implementation, analysis, visualizations, and experimental workflow are available in the accompanying Jupyter Notebook.
