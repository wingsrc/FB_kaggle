# FB_kaggle

Link: https://www.kaggle.com/c/facebook-recruiting-iv-human-or-bot

My first Kaggle competition, "Facebook Recruiting IV: Human or Robot?". It was a lot of fun. More importantly, I learned a lot! I achieved top 35% on the final leaderboard.

Here's my approach. In "feature_extraction.r", I wrote several functions to extract features from the bidders' info provided by FB. The features I used are: min and max bidding time, avg number of bids in each auction, avg number of bidders in each auction, avg # of devices, url, countries in each auction, and total number of bids. In this competition, we can discover that machine learning algorithms such like random forest work appropriately. Therefore I used caret to tune the parameters in random forest model. I also played with ensemble model of a mix of models: gbm, random forest and svm. Then I run 4-fold cv to pick the best model. 

Even though the ensemble method gives much better result in private leaderboard, it's much worse than my original random forest model (so much regrets). Lesson learned: Use more folds in cv. CV is your only friend!
