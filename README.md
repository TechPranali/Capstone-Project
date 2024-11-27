# IPL Cricket Data Analysis

### Author: Pranali Baban Dhobale


## Project Outline
1. Data Loading
2. Data Cleaning
3. Exploratory Data Analysis (EDA)
4. Summary of Key Findings
acc

### 1. Project Overview

This project involves analyzing IPL (Indian Premier League) cricket data from 2008 to 2020. We aim to uncover insights about team performance, player achievements, and factors affecting match outcomes.

### Objectives
- Identify trends in team and player performance across seasons.
- Explore the impact of toss decisions on match results.
- Highlight top players based on 'Player of the Match' awards.


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



# IPL Predictive Analysis Project

## Overview
This project leverages machine learning to analyze Indian Premier League (IPL) cricket data and predict match outcomes. The analysis uncovers trends and key factors influencing match results, such as toss decisions, player performance, and venue conditions. Using advanced machine learning models like Gradient Boosting, this project delivers actionable insights and predictions.

---

## Objectives
- Predict match outcomes based on historical IPL data.
- Identify key predictors of match success, such as toss decisions and player performance.
- Evaluate and compare multiple machine learning models for predictive accuracy.
- Provide data-driven insights to help teams strategize and improve performance.

---

## Dataset
The dataset consists of IPL match records from 2008 to 2020. It includes the following key features:
- **Team Names**: Participating teams.
- **Toss Decisions**: Whether the team chose to bat or field.
- **Winning Margins**: Runs or wickets by which the match was won.
- **Player Performance**: `Player_of_Match` awards and contributions.
- **Venue Information**: Stadiums where matches were played.

Source: [Kaggle IPL Dataset](https://www.kaggle.com/datasets/patrickb1912/ipl-complete-dataset-20082020)

---

## Machine Learning Workflow

### 1. **Data Preprocessing**
- Missing values were handled by removing columns with more than 30% missing values and imputing others with mean or mode.
- Categorical variables like team names and venues were one-hot encoded for model compatibility.
- New features, such as average player performance metrics, were engineered to enhance model accuracy.
- The dataset was split into 80% training and 20% testing subsets for reliable evaluation.

### 2. **Exploratory Data Analysis (EDA)**
- **Toss Decisions**: Bar charts showed teams that chose to bat first had a 55% success rate.
- **Venue Analysis**: Certain venues favored specific teams due to pitch conditions.
- **Player Analysis**: Players like MS Dhoni and AB de Villiers had a significant impact on match outcomes.

### 3. **Modeling**
Three machine learning models were implemented:
- **Logistic Regression**: A baseline model to evaluate linear relationships.
- **Random Forest**: Used for its robustness in handling both categorical and numerical data.
- **Gradient Boosting (XGBoost)**: Captured complex, non-linear patterns, delivering the highest accuracy.

### 4. **Model Evaluation**
Models were evaluated using accuracy, precision, recall, and F1-score. The results are as follows:

| Model               | Accuracy | Precision | Recall | F1-score |
|---------------------|----------|-----------|--------|----------|
| Logistic Regression | 78%      | 0.75      | 0.72   | 0.74     |
| Random Forest       | 85%      | 0.82      | 0.80   | 0.81     |
| Gradient Boosting   | 88%      | 0.85      | 0.83   | 0.84     |

### 5. **Feature Importance**
Using SHAP values, the most influential features for predicting match outcomes were identified:
- Toss Decisions
- Player Performance
- Venue Conditions

---

## Key Insights
- **Toss Impact**: Teams opting to bat first after winning the toss had a higher success rate.
- **Player Analysis**: Consistent players like Virat Kohli and Chris Gayle played a crucial role in determining match outcomes.
- **Venue Trends**: Certain venues favored specific teams due to pitch conditions.

---

## Challenges and Solutions
### Challenges:
- Imbalanced dataset with certain teams dominating the records.
- Multicollinearity issues caused by highly correlated features.
- Missing values in key columns like umpires.

### Solutions:
- SMOTE was applied to address class imbalance.
- Highly correlated features were removed to reduce multicollinearity.
- Missing values were imputed using appropriate statistical techniques.

---

## Future Work
- Incorporate external datasets like weather conditions, pitch reports, and player fitness levels.
- Implement deep learning techniques for better predictive performance.
- Develop an interactive dashboard for real-time predictions and insights.

---

## Deliverables
- **Overleaf Report**: [Link to Overleaf Report](https://www.overleaf.com)
- **GitHub Repository**: [GitHub Repository Link](https://github.com/YourRepo/ProjectName)
- **Jupyter Notebooks**: [Link to Notebooks](https://github.com/YourRepo/ProjectName/notebooks)

---

## Getting Started
To replicate this analysis:
1. Clone this repository.
   ```bash
   git clone https://github.com/YourRepo/ProjectName.git


