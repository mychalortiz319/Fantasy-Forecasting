## Future Steps

1. Add your own data in `./data/` and remove placeholder. Note: `.gitignore` will ignore the data folder when you push to github, save a copy of your raw and processed data, pickled models in a Google Drive folder and add the link in the `data_links.md` file.
2. Add your project documents, figures, reports, presentation pdf's in the `./docs` and remove placeholders.
3. Add your references (tutorials, papers, books etc.) in `./references`. 
4. Add your own scripts in `./src/` and remove unnecessary folders.

------------------------------------------------------------------------------

## Fantasy Forecasts
=========================

### Executive Summary

Problem Area
Fantasy football has become increasingly popular, engaging millions of participants who aim to build the best teams by carefully selecting NFL players. However, making informed decisions on which players to draft, start, or trade can be challenging due to numerous factors influencing a player's performance, such as previous stats, injuries, weather conditions, and team dynamics. This problem primarily affects fantasy football players, ranging from casual fans to serious league participants, who seek to optimize their rosters for success.

Affected Population
The primary audience impacted by this solution includes fantasy football players who need predictive insights to make strategic roster decisions. Secondary audiences could include sports analysts, fantasy league hosts, and sports betting platforms that benefit from accurate player performance forecasts.

Proposed Data Science Solution
This project proposes a data science solution utilizing machine learning techniques to predict NFL players' fantasy football statistics. By analyzing historical performance data and other contextual factors, the model will generate predictions to aid users in making better roster decisions. This solution leverages predictive modeling to uncover patterns and insights that are difficult for players to discern on their own.

Impact of the Solution
The implementation of this solution will enable fantasy football players to make more informed decisions, ultimately increasing their chances of success in fantasy leagues. Additionally, it could reduce the reliance on expert analyses, empowering users with data-driven insights directly. Beyond individual users, this model may also benefit fantasy sports platforms and betting services by enhancing user engagement and satisfaction.

Dataset Description
The dataset used in this project includes detailed NFL competition and fantasy football data sourced from Kaggle. It contains weekly player statistics, including performance metrics like touchdowns, yards gained, receptions, and points scored. Additionally, contextual variables such as player injuries, weather conditions, and team performance are included to increase the model's predictive accuracy.

### Demo

... Show your work:
...     Data visualizations
...     Interactive demo (e.g., `streamlit` app)
...     Short video of users trying out the solution


### Methodology

... High-level diagrams of entire process:
...     various data processing steps
...     various modelling directions
...     various prototyping directions


### Notebooks

**Exploratory Data Analysis**

Objective:

This notebook focuses on cleaning and analyzing player performance data, identifying trends and relationships, and preparing dataframes segmented by player positions for predictive modeling.

1. Data Ingestion:
Read data from the provided datasource into a working format.

2. Data Cleaning:
Checked for and addressed null values and duplicate entries.
Removed players marked as "Did Not Play" to maintain data relevance.
Fixed inconsistencies for players on bye weeks or listed as free agents.

3. Data Preparation:
Split the cleaned dataset into separate dataframes for Quarterbacks (QBs), Running Backs (RBs), Wide Receivers (WRs), and Tight Ends (TEs) to facilitate position-specific analysis.

4. Exploratory Analysis:
Plotted distributions for key stats (e.g., passing yards, rushing yards) to understand positional performance patterns.
Generated heatmaps to visualize correlations between features (e.g., passing yards, rushing touchdowns) and fantasy point totals.
Created scatter plots to analyze relationships between individual features and total fantasy points.

5. Data Export:
Saved the cleaned and segmented dataframes for use in predictive modeling workflows.

**Baseline Modeling**

Objective: 
This notebook focuses on feature engineering and baseline model implementation to predict fantasy football player performance.

1. Feature Engineering:
Computed 5-game rolling averages for key stats (e.g., passing yards, rushing yards, receiving yards) to capture recent performance trends.
Calculated cumulative and average stats for fantasy points, rushing, passing, and receiving metrics up to each week, excluding the current week.

2. Model Development:
Implemented baseline regression models, including Linear Regression and Ridge Regression, to predict player fantasy performance.
Used both cumulative season metrics and 5-game rolling averages as predictors to assess their impact on model accuracy.

3. Model Evaluation:
Evaluated models using Mean Absolute Error (MAE) and R-squared (R²) metrics to measure predictive power. 
Found that certain positions (e.g., Quarterbacks) achieved better metrics due to the consistent nature of their role and statistical contributions. Leveraged grid search cross-validation to optimize hyperparameters, which significantly improved predictions for all positions.

#### Repository 

* `data` 
    - contains link to copy of the dataset (stored in a publicly accessible cloud storage)
    - saved copy of aggregated / processed data as long as those are not too large (> 10 MB)

* `model`
    - `joblib` dump of final model(s)

* `notebooks`
    - contains all final notebooks involved in the project

* `docs`
    - contains final report, presentations which summarize the project

* `references`
    - contains papers / tutorials used in the project

* `src`
    - Contains the project source code (refactored from the notebooks)

* `.gitignore`
    - Part of Git, includes files and folders to be ignored by Git version control

* `conda.yml`
    - Conda environment specification

* `README.md`
    - Project landing page (this page)

* `LICENSE`
    - Project license

#### Dataset

https://www.kaggle.com/datasets/fishhead/fantasy-football

### Credits & References
