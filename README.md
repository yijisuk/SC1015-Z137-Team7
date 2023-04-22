# SC1015 - Chess Game Analysis

## About Our Project

This is the mini project for SC1015 (Intro to Data Science and AI) which analyses 6.2 million chess games played on Lichess from [Chess Games](https://www.kaggle.com/datasets/arevel/chess-games). For the entire walkthrough of the project, please view the notebooks/readmes in this order:

[1. Data cleaning] (https://github.com/yijisuk/SC1015-Z137-Team7/blob/main/1-data-cleaning.ipynb)
[2. Visualisation] (https://github.com/yijisuk/SC1015-Z137-Team7/blob/main/2-visualization-eda.ipynb)
[3. Feature extraction] (https://github.com/yijisuk/SC1015-Z137-Team7/blob/main/3-feature-extraction.ipynb)
[4. Data processing] (https://github.com/yijisuk/SC1015-Z137-Team7/blob/main/4-encoding-normalization.ipynb)
[5. Logistic Regression] (https://github.com/yijisuk/SC1015-Z137-Team7/blob/main/5-logistic-regression.ipynb)
[6. Random Forests] (https://github.com/yijisuk/SC1015-Z137-Team7/blob/main/6-random-forests.ipynb)
[7. Gradient Boosting] (https://github.com/yijisuk/SC1015-Z137-Team7/blob/main/7-gradient-boosting.ipynb)

## About the Datasets
Due to dataset file capacity, we have uploaded our dataset separately on Google Drive.
<br>Access the dataset [here] (https://drive.google.com/drive/folders/1q_pA9sS2QZCJ__U6mw-oV9Hr_PmSsgCo?usp=share_link).

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
