# SC1015 - Chess Game Analysis

## About The Project

This is the mini project for SC1015 (Intro to Data Science and AI) which analyses 6.2 million chess games played on Lichess from [Chess Games (Kaggle)](https://www.kaggle.com/datasets/arevel/chess-games). For the entire walkthrough of the project, please view the notebooks in this order:

1. [Data cleaning](https://github.com/yijisuk/SC1015-Z137-Team7/blob/main/1-data-cleaning.ipynb)
2. [Visualisation](https://github.com/yijisuk/SC1015-Z137-Team7/blob/main/2-visualization-eda.ipynb)
3. [Feature extraction](https://github.com/yijisuk/SC1015-Z137-Team7/blob/main/3-feature-extraction.ipynb)
4. [Data processing](https://github.com/yijisuk/SC1015-Z137-Team7/blob/main/4-encoding-normalization.ipynb)
5. [Logistic Regression](https://github.com/yijisuk/SC1015-Z137-Team7/blob/main/5-logistic-regression.ipynb)
6. [Random Forests](https://github.com/yijisuk/SC1015-Z137-Team7/blob/main/6-random-forests.ipynb)
7. [Gradient Boosting](https://github.com/yijisuk/SC1015-Z137-Team7/blob/main/7-gradient-boosting.ipynb)

## About the Datasets

Due to dataset file capacity, we have uploaded our dataset separately on Google Drive. Access the dataset [here](https://drive.google.com/drive/folders/1q_pA9sS2QZCJ__U6mw-oV9Hr_PmSsgCo?usp=share_link).

## Problem Definition
**Primary Objective**: Utilizing the initial and pre-mid-game stages of a given game, can we accurately predict the game's outcome through classification techniques?

**Task**: Classify game outcomes into win/loss categories and identify the determining factors contributing to the termination of games.

## Models Used

1. [Logistic Regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)
2. [Random Forests Classifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)
3. [AdaBoost Classifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.AdaBoostClassifier.html)
4. [XGBoost Classifier](https://xgboost.readthedocs.io/en/stable/)

## Main Takeaways from our EDA

1. Estimated Scores & Winning Probabilities and win/loss results, derived from the initial Elo ratings of both White and Black players, do not guarantee a direct correlation with the ultimate outcome of the match. A player with a considerably higher projected score or probability of winning may not necessarily secure a win. This highlights the inherent probabilistic nature of chess, where numerous factors influence the game's progression. Consequently, an evaluation of the match outcome should not rely solely on the initial data but also incorporate each player's performance throughout the game.
2. About 800K of the games are evaluated from Stockfish; this will be used for the main classification tasks.
3. `A00`, `A40`, `B00`, `B01`, `B20`, `C00`, `C20`, `C41`, `D00` are the most frequently used openings based on crosstab normalisation of greater than 0.1.

## Conclusion

1. **Accuracy**: In the context of this study, accuracy is defined as the proportion of correct predictions made by the model out of the total number of predictions. A higher accuracy score is generally indicative of a more effective model. Upon examination, we find that the Random Forest model outperforms the other models, achieving the highest accuracy in predicting White's Win/Loss and Black's Win/Loss outcomes. This result can be attributed to the model's ability to create an ensemble of decision trees, which helps in reducing overfitting and improving generalization. Following the Random Forest model, XGBoost demonstrates the next highest level of accuracy, benefiting from its gradient-boosted trees that focus on reducing errors iteratively. Conversely, Logistic Regression and AdaBoost models exhibit the lowest accuracy scores, suggesting that they may not be as effective in capturing the complex patterns and relationships within the chess game data.

2. **Macro F1-score**: This metric represents the harmonic mean of precision and recall, offering a comprehensive measure of the model's performance. A higher F1-score is preferable, as it indicates a balance between precision (how many true positive predictions were made out of all positive predictions) and recall (how many true positive predictions were made out of all actual positive instances). In our analysis, we observe that the Random Forest model has the lowest F1-score for predicting Termination, while the other three models—XGBoost, Logistic Regression, and AdaBoost—display relatively similar F1-scores. Despite these similarities, it is important to note that all the F1-scores are considerably low, suggesting that there is substantial room for improvement in predicting Termination outcomes.

3. **Inherent Probabilistic Nature of Chess**: Chess is a highly probabilistic game, with a myriad of potential outcomes that can be influenced by unexpected moves, such as last-minute blunders or strategic surprises. Despite this inherent unpredictability, our analysis shows that it is still possible to predict Win/Loss outcomes with an accuracy of 0.81. This achievement highlights the potential for machine learning models to effectively analyze and predict complex game scenarios, even in the face of uncertainty and the vast possibility space of chess games.

## Contributors
- [@yijisuk](https://github.com/yijisuk) (SUK Yiji) - Data cleaning & processing, Feature Engineering, EDA, Random Forests & Decision Trees, XGBoost
- [@Moon0002](https://github.com/Moon0002) (MOON Seongwon) - Data processing, Logistic Regression, Presentation Slides.
- [@Lyroxide](https://github.com/Lyroxide) (OH Jing Hong, Daryl) - Data cleaning & processing, AdaBoost & XGBoost, Presentation Slides & Recording

## References

- https://lichess.org
- https://www.365chess.com/eco.php
- https://towardsdatascience.com/xgboost-regression-training-on-cpu-and-gpu-in-python-5a8187a43395
- https://en.wikipedia.org/wiki/Elo_rating_system
- https://www.chessprogramming.org/Pawn_Advantage,_Win_Percentage,_and_Elo
- https://www.chess.com/terms/chess-middlegame
