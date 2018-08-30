# Ames-Iowa-Housing-Machine-Learning-Python
This project was written for a Kaggle competition: https://www.kaggle.com/c/dsi-us-5-project-2-regression-challenge/data . My goal was to predict houses' prices based on theirs parameters. I used data comes from Ames housing dataset. Outcomes represented sale price of house at the market.

I did some feature engineering: 
- Created new 'Rate' columns for every categorical column grouping them by theirs value and calculated mean sale price. Than I sorted values by increasing of mean sale price and assigned every value it's rate - just a serial number (1, 2, 3 etc.)
- Created dummies.
- Assigned number for Qual and Cond columns: from 1 for Poor to 5 for Excellent.

Then I used MultinomialFeatures (2 degree), selected only columns that have correlation with sale price over 0.6 and apply a lasso regression.

I also did some useful observations. First of all, I hoped that lasso will select only significant features, but result of lasso regression showed me that almost all of features are significant. Second, the strongest impact in sale price have neighborhood rate and lot area (in square feet).
