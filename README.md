# Title

## About Our Project

This is the mini project for SC1015 (Intro to Data Science and AI) which analyses 6.2 million chess games played on Lichess from [Chess Games](https://www.kaggle.com/datasets/arevel/chess-games). For the entire walkthrough of the project, please view the notebooks/readmes in this order:

1. Data cleaning
2. Visualisation
3. Feature extraction
4. Data processing
5. Logistic Regression
6. Tree-Based Apparoaches
7. Gradient Boosting

## Project Folder Structure
(temp)
```terminal
.
├── datasets                          # csv files
├── data_cleaning                     # folder for data cleaning
├── data_processing                   # folder for data processing
├── EDA                               # folder for EDA
├── feature_extract                   # folder for feature extraction
├── gradient_boosting                 # folder for gradient boosting
├── presentation                      # presentation ppt
├── logistic regression.ipynb         # notebook for logistic regression
└── README.md
```

## Problem Definition

- Given the initial and mid-game states of the game, can we predict the outcome of the game?

## Models Used

1. Logistic Regression
2. Random Forest Classifier
3. Decision Trees
4. AdaBoost
5. XGBoost

## Main Takeaways from our EDA

1. About 800K of the games are evaluated from Stockfish.
2. `A00`, `A40`, `B00`, `B01`, `B20`, `C00`, `C20`, `C41`, `D00` are the most frequently used openings based on crosstab normalisation of greater than 0.1.
3. 

## Conclusion

1. Starting with accuracy, we can see that Random Forest has the highest accuracy for predicting White's Win/Loss and Black's Win/Loss, followed by XGBoost. Logistic Regression and AdaBoost have the lowest accuracy among the models. 
2. Moving onto macro F1-score, we see that Random Forest has the lowest F1-score for predicting Termination while the other three models have relatively similar F1-score. However, all the F1-scores are still very low.
3. Despite Chess being a highly probabilistic game as anything could happen at the very last few moves of the game, such as blunders that turn the tide immediately, we could still predict Win/Loss with an accuracy of 0.81.
4. 

## Contributors
- @
- @
- @lyroxide - Data processing, Gradient Boosting

## References

- https://lichess.org
- https://www.365chess.com/eco.php
- https://towardsdatascience.com/xgboost-regression-training-on-cpu-and-gpu-in-python-5a8187a43395
- https://en.wikipedia.org/wiki/Elo_rating_system
- https://www.chessprogramming.org/Pawn_Advantage,_Win_Percentage,_and_Elo
- https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.AdaBoostClassifier.html
- 