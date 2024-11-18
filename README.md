# IPL Cricket Data Analysis

### Author: Pranali Baban Dhobale

---

## Project Outline
1. Data Loading
2. Data Cleaning
3. Exploratory Data Analysis (EDA)
4. Summary of Key Findings
acc
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
data = pd.read_csv('IPL_Cricket_Project.csv')
data.head()


3.1 Setting Up the Project Virtual Environment

To keep the project dependencies organized and ensure compatibility across environments, it’s recommended to set up a Python virtual environment. Below are the steps to create, activate, and manage the virtual environment for this project.

1. Create a Virtual Environment
First, navigate to your project directory. Then, use the following command to create a virtual environment named .venv 
python3 -m venv .venv
This will create a folder .venv in your project directory, containing the isolated Python environment.

2. Activate the Virtual Environment

To activate the virtual environment: .venv\Scripts\activate
After activation, the terminal prompt will reflect the active environment by displaying the name of the virtual environment.

3. Install Project Dependencies
Once the virtual environment is activated, use the following command to install the required dependencies. Ensure that the requirements.txt file is available in the project directory and contains all necessary packages.
After activating the virtual environment, install the required packages by running:

pip install -r requirements.txt

This command reads the dependencies listed in requirements.txt and installs them into the isolated environment, ensuring consistent package versions.


---

3.2 Exploratory Data Analysis (EDA)
This section includes an in-depth analysis of team performance, player statistics, and match outcomes.

Key Steps
Descriptive statistics and distribution checks.
Visualization of match outcomes, toss decisions, and player performances.
Correlation analysis to understand the relationships between different factors.
Identification of seasonal trends and patterns in team performance.
python
# Example of data visualization
sns.countplot(x='winner', data=data, order=data['winner'].value_counts().index)
plt.xticks(rotation=90)
plt.title("Number of Wins by Each Team")
plt.show()
---


