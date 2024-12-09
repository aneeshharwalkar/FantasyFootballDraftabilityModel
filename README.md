# FantasyFootballDraftabilityModel

## Overview
This project leverages NFL player statistics from 2017 to 2023 to predict players' fantasy rankings based on their stats. By using machine learning models, we aim to assist fantasy football managers in making smarter decisions when drafting players for their rosters.

## Objectives
- Build a predictive model to estimate players' fantasy rankings by position.
- Analyze key factors influencing fantasy draftability.
- Provide a demo tool to help fantasy football managers optimize their draft picks.

## Dataset
The dataset was sourced from Kaggle: Fantasy Football Data 2017-2023.
- Features: 27 columns (player stats and attributes)
- Rows: 3,388 (NFL player data points)

### Data Preprocessing
1. Dropped irrelevant columns like player names and IDs.
2. Established PosRk (Position Rank) as the label for prediction.
3. Used one-hot encoding for categorical features like player position (QB, RB, WR, TE).
4. Applied:
  - PowerTransformer for skewed numerical columns.
  - StandardScaler to normalize the data for Principal Component Analysis (PCA).

## Methodology
### Model Selection
Models Tested:
- Linear Regression
- Support Vector Regression (SVR)
-  Decision Trees
- Random Forest
- Gradient Boosting
Evaluated using:
- Mean Squared Error (MSE)
- Mean Absolute Error (MAE)
- R-squared values

### Feature Engineering
- Conducted feature correlation analysis to reduce redundancy.
- Implemented PCA to address multicollinearity and reduce dimensionality.
### Final Model
- Random Forest achieved the best performance with:
- MSE: 20.91
- High 𝑅^2: Indicates strong predictive accuracy.
## Demo
A demo tool showcases the model's capabilities. Users can input NFL player statistics and get a predicted fantasy position ranking.

### Files
- `FantasyFootballDemo.ipynb`: Interactive notebook with a demo of the model.
- `Random_Forest.pkl`: Saved Random Forest model.
- `Fantasy_Football_Stats.csv`: Preprocessed dataset used for training and testing.
- `FantasyFootball.ipynb`: Full implementation of model training, evaluation, and preprocessing.
## Results
Key Findings:
  - PPR (Points Per Reception) and positional metrics are critical for draftability predictions.
  - Random Forest consistently outperformed other models in prediction accuracy.
Limitations:
  - Temporal changes in player trends (e.g., injuries, trades) are not captured.
  - Lack of real-time data affects immediate applicability.
## Future Applications
- Develop a real-time draft assistance tool integrated with live NFL data.
- Extend the model to support other fantasy sports, such as basketball or baseball.

## Contributors
- David Doan
- Jonah Lessuk
- Dillan Hong
- Aneesh Harwalkar
