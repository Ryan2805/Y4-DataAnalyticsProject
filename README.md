# FIFA 20 Player Data Analysis 

This project explores and analyses the **FIFA 20 player dataset** using Python.
The goal is to clean the data, perform exploratory analysis, test statistical hypotheses, and build simple predictive models based on player attributes.

The dataset contains detailed information about professional football players including ratings, wages, potential, positions, and technical attributes.

---

## Dataset

The dataset used is **`players_20.csv`**, which includes attributes for thousands of FIFA 20 Career Mode players.

Source:
https://www.kaggle.com/datasets/stefanoleone992/fifa-20-complete-player-dataset

The data was originally scraped from **sofifa.com**.

Key features in the dataset include:

* Player age
* Overall rating
* Potential rating
* Market value
* Wage
* Preferred foot
* Team position
* Technical attributes (shooting, passing, etc.)

---

# Project Objectives

This analysis focuses on:

* Data cleaning and preprocessing
* Exploratory data analysis (EDA)
* Statistical hypothesis testing
* Correlation analysis
* Predictive modelling using machine learning

---

# Technologies Used 

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy
* Scikit-learn
* Jupyter Notebook

---

# Data Cleaning

The raw dataset contains many columns and missing values.
Several preprocessing steps were applied to prepare the data for analysis.

Key steps included:

* Selecting relevant columns for analysis
* Handling missing values
* Removing duplicate records
* Creating derived variables

Two new variables were created:

**position_group**

Players were grouped into broader categories:

* Defence
* Midfield
* Attack
* Other

**high_potential**

Binary variable indicating whether a player has high future potential:

* 1 → Potential ≥ 80
* 0 → Potential < 80

Rows with missing values in key variables (age, rating, wage, position, etc.) were removed to produce a cleaned dataset used for analysis.

---

# Exploratory Data Analysis

Exploratory analysis was used to understand the distribution of player characteristics.

Key insights:

* Player ages cluster mostly between **20 and 30 years old**
* Overall ratings are generally concentrated between **65 and 80**
* Potential ratings are slightly higher on average than overall ratings
* Player wages and values are **highly skewed**, with a small number of extremely high-earning players

Visualisations include:

* Histograms of player ratings and age
* Boxplots of wages by position group
* Distribution plots of key attributes

---

# Hypothesis Testing

Several statistical hypothesis tests were conducted to evaluate differences between groups of players.

Example test:

### Shooting Ability – Attack vs Defence

Question:
Do attacking players have higher shooting ratings than defenders?

Hypotheses:

* **H₀:** There is no difference in mean shooting ratings between attacking and defensive players
* **H₁:** Attacking players have different shooting ratings than defensive players

An independent **two-sample t-test** was used.

Result:

* The p-value was **< 0.001**
* The null hypothesis was rejected
* Attacking players have **significantly higher shooting ratings** than defenders

---

# Machine Learning Models 

Two predictive models were implemented:

## Linear Regression

Used to explore relationships between player attributes and ratings.

## Logistic Regression

Used to classify whether a player belongs to the **high potential** category.

These models demonstrate how player statistics can be used to predict performance characteristics.

---

# Repository Structure

```
FIFA-Player-Analysis
│
├── FIFA_PlayersDone.ipynb
├── players_20.csv
├── fifalogo.jpg
└── README.md
```

---

# How to Run the Project

1. Clone the repository

```
git clone https://github.com/yourusername/fifa-player-analysis.git
```

2. Install required libraries

```
pip install pandas numpy matplotlib seaborn scikit-learn scipy
```

3. Run the notebook

```
jupyter notebook FIFA_PlayersDone.ipynb
```

---

# Example Analysis Questions

Some questions explored in this project include:

* Do attackers have higher shooting ability than defenders?
* How are wages distributed across player positions?
* What attributes correlate most strongly with player ratings?
* Can we predict high-potential players using machine learning?

---

# Key Skills Demonstrated

* Data cleaning and preprocessing
* Exploratory data analysis
* Data visualisation
* Statistical hypothesis testing
* Machine learning with Python
* Working with large real-world datasets

---

# Future Improvements

Possible extensions of the project:

* Use more advanced models (Random Forest, Gradient Boosting)
* Predict player market value
* Perform feature importance analysis
* Build an interactive dashboard for player analysis

---

# Author

Ryan Daly
Software Development Student
