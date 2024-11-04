# IPL Cricket Data Analysis

### Author: Pranali Baban Dhobale

---

## Project Outline
1. Data Loading
2. Data Cleaning
3. Exploratory Data Analysis (EDA)
4. Summary of Key Findings

---

### 1. Project Overview

This project involves analyzing IPL (Indian Premier League) cricket data from 2008 to 2020. We aim to uncover insights about team performance, player achievements, and factors affecting match outcomes.

### Objectives
- Identify trends in team and player performance across seasons.
- Explore the impact of toss decisions on match results.
- Highlight top players based on 'Player of the Match' awards.

---

### 2. Data Description

#### Data Source
The dataset used in this project is from [Kaggle](https://www.kaggle.com/datasets/patrickb1912/ipl-complete-dataset-20082020) and includes IPL match data from 2008 to 2020.

#### Key Attributes
- `match_id`: Unique identifier for each match.
- `season`: Year of the IPL season.
- `team1`, `team2`: Competing teams.
- `winner`: Team that won the match.
- `player_of_match`: Awarded player for outstanding performance.
- `toss_winner`, `toss_decision`: Team that won the toss and their decision.
- `venue`: Location of the match.

---

### 3. Data Loading

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load dataset
data = pd.read_csv('path_to_your_dataset.csv')
data.head()

