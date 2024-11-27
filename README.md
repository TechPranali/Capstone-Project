# IPL Cricket Data Analysis

### Author: Pranali Baban Dhobale

---

## Project Outline
1. Data Loading
2. Data Cleaning
3. Exploratory Data Analysis (EDA)
4. Summary of Key Findings

---

## 1. Project Overview

This project involves analyzing IPL (Indian Premier League) cricket data from 2008 to 2020. The objective is to uncover insights about team performance, player achievements, and factors affecting match outcomes.

### Objectives
- Identify trends in team and player performance across seasons.
- Explore the impact of toss decisions on match results.
- Highlight top players based on 'Player of the Match' awards.

---

## 2. Data Description

### Data Source
The dataset used in this project is sourced from [Kaggle](https://www.kaggle.com/datasets/patrickb1912/ipl-complete-dataset-20082020) and includes IPL match data from 2008 to 2020.

### Key Attributes
- `match_id`: Unique identifier for each match.
- `season`: Year of the IPL season.
- `team1`, `team2`: Competing teams.
- `winner`: Team that won the match.
- `player_of_match`: Awarded player for outstanding performance.
- `toss_winner`, `toss_decision`: Team that won the toss and their decision.
- `venue`: Location of the match.

---

## 3. Data Loading

### Steps
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load dataset
data = pd.read_csv('IPL_Cricket_Project.csv')
print(data.head())
4. Setting Up the Project Virtual Environment
To keep the project dependencies organized and ensure compatibility across environments, set up a Python virtual environment.

Steps
Create a Virtual Environment:

bash
Copy code
python3 -m venv .venv
This will create a folder .venv in your project directory.

Activate the Virtual Environment:

bash
Copy code
.venv\Scripts\activate
Install Project Dependencies:

bash
Copy code
pip install -r requirements.txt
Ensure the requirements.txt file contains all necessary packages.

5. Exploratory Data Analysis (EDA)
This section includes an in-depth analysis of team performance, player statistics, and match outcomes.

Key Steps:
Perform descriptive statistics and distribution checks.
Visualize match outcomes, toss decisions, and player performances.
Conduct correlation analysis to understand the relationships between different factors.
Identify seasonal trends and patterns in team performance.
Example of Data Visualization:
python
Copy code
sns.countplot(x='winner', data=data, order=data['winner'].value_counts().index)
plt.xticks(rotation=90)
plt.title("Number of Wins by Each Team")
plt.show()
6. Predictive Analysis
Overview
This project leverages machine learning to analyze IPL data and predict match outcomes. Advanced models like Gradient Boosting are used to uncover trends and key factors influencing match results.

Objectives:
Predict match outcomes based on historical IPL data.
Identify key predictors of match success.
Evaluate and compare multiple machine learning models for predictive accuracy.
Machine Learning Workflow
1. Data Preprocessing
Handle missing values and impute where necessary.
Perform one-hot encoding for categorical features.
Engineer new features like average player performance metrics.
2. Exploratory Data Analysis
Analyze toss decisions, venue impact, and player contributions using bar charts and correlation heatmaps.
3. Modeling
Three machine learning models were implemented:

Logistic Regression
Random Forest
Gradient Boosting (XGBoost)
4. Model Evaluation
Model	Accuracy	Precision	Recall	F1-score
Logistic Regression	78%	0.75	0.72	0.74
Random Forest	85%	0.82	0.80	0.81
Gradient Boosting	88%	0.85	0.83	0.84
5. Feature Importance
Using SHAP values, the most influential features for predicting match outcomes were:

Toss Decisions
Player Performance
Venue Conditions
7. Key Insights
Toss Impact: Teams opting to bat first after winning the toss had a higher success rate.
Player Analysis: Players like Virat Kohli and MS Dhoni significantly influenced match outcomes.
Venue Trends: Certain venues favored specific teams due to pitch conditions.
8. Challenges and Solutions
Challenges:
Imbalanced dataset.
Multicollinearity in highly correlated features.
Solutions:
Applied SMOTE to address class imbalance.
Removed highly correlated features to reduce multicollinearity.
9. Future Work
Incorporate additional datasets like weather and pitch conditions.
Develop a real-time dashboard for predictions.
10. Deliverables
Overleaf Report: Link to Overleaf Report
GitHub Repository: GitHub Repository Link
Jupyter Notebooks: Link to Notebooks
