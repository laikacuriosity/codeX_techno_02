# codeX_techno
Internship task 02 for CodeX Techno<br>

This project performs Data Exploration and Cleaning, Feature selection, Model Training, Model Evaluation, and Visualization on a Housing dataset containing 545 records. The dataset includes features related to house structure, amenities, and location.<br>

Project Goal: Predicting house prices with Linear Regression.<br>
The goal of this analysis is to uncover patterns in housing characteristics, identify key price drivers, and prepare the dataset for building a predictive linear regression model.<br>

1.DATASET DESCRIPTION:<br>
   Total rows:545<br>
   Total columns:13<br>
   Missing values: none<br>
   Duplicates: none<br>
   Consistency: all categorical values appear consistent<br>

   DATA TYPES:<br>
   Numeric: price, area, bedrooms, bathrooms, stories, parking.<br>
   Categorical: mainroad, guestroom, basement, hotwaterheating, airconditioning, prefarea, furnishingstatus.<br>


ANALYSIS WORKFLOW:<br>

1. DATA OVERVIEW:<br>
   Checked dataset structure, data types, and missing values.<br>
   Verified all columns have non-null values.<br>
   Identified skewness in total amount due to a few high-vaue houses.<br>
   
2. VARIABLE EXPLORATION<br>
   Numeric variables: examined distributions, mean, mdian, standard deviation, outliers. <br>
   Categorical variables: frequency counts and category proportions. <br>
   Outlier analysis: focused on price, area, bedrooms, bathrooms, stories and parking.<br>

3. DATA VISUALIZATION:<br>
   Histograms and Boxplots : identified outliers in numerical variables.<br>
   Bar charts / countplots : For categorical variables like mainroad, furnishingstatus, airconditioning.<br>
   Heatmaps: Identify correlations between numerical and categorical features with target price.<br>


4. INSIGHTS:<br>

4.1 Housing Characteristics: <br>

   Most houses are mid-sized, family homes; luxury homes are rare.<br>
   Bedrooms & Bathrooms: Mostly 2–3 bedrooms, 1–3 bathrooms.<br>
   Stories & Parking: 1–2 stories, 0–2 parking spots.<br>
   Price & Area: Right-skewed; high-value outliers affect regression modeling.<br>


4.2 Categorical Feature Insights: <br>

   Mainroad: Majority of houses near main road.<br>
   Air Conditioning: Few houses with AC.<br>
   Furnishing Status: Semi-furnished dominate, then unfurnished, then fully furnished.<br>
   Guestroom & Basement: Most houses lack these amenities.<br>
   Hot Water Heating: Few houses have this.<br>
   Preferred Area: Majority are not in prime locality.<br>


4.3 Correlation and Multicollinearity: <br>

   Low multicollinearity → linear regression is suitable.<br>
   Strong predictors of price: area, bathrooms, stories, airconditioning, parking, bedrooms. <br>

4.4 OUTLIERS ANALYSIS AND HANDLING:<br>

   High number of iutliers are detected in features like area, price and bedrooms. these    outliers affect high priced houses, large area, and large number of bedrooms, this  can       significantly distort regression results.<br>
   Hence they were handled by removing extreme values in price, area, and bedrooms.<br>

4.5 REGRESSION MODEL PERFORMANCE: <br>

Linear Regression:<br>
R²: 0.719 → Explains ~72% of price variability.<br>
RMSE: 919,252 → Reasonable deviation for high-priced houses.<br>
High-priced houses slightly underestimated.<br>

Ridge Regression:<br>
MSE: 894,983,045,776<br>
R²: 0.70 → Slightly lower than linear regression, more stable.<br>

Lasso Regression:<br>
MSE: 845,024,981,326<br>
R²: 0.719 → Slightly better than RidgeCV<br>
Captures linear patterns; better generalization for mid-priced houses.<br>


5. SUMMARY & RECOMMENDATIONS:<br>

   Dataset is clean and ready for modeling.<br>
   Outliers exist in price, area, bedrooms, bathrooms, stories, parking → handle for regression accuracy.<br>
   Most houses are mid-sized, family homes; luxury homes are rare.<br>
   Key price drivers: area, bathrooms, stories, airconditioning, parking, bedrooms.<br>
   Linear models perform well; Ridge adds stability; Lasso slightly improves fit.<br>
   High-priced houses remain challenging due to fewer samples and skewed distribution.<br>
   Despite good model performance for mid-range houses, high-priced houses remain challenging due to limited sample representation, highlighting the need for potential feature engineering or advanced modeling techniques for better predictions in the upper price range.<br>

6. CONCLUSION:<br>
   Overall, this analysis equips us with the insights needed to build a robust predictive model for estimating house prices and informs strategies for feature selection, outlier handling, and model evaluation.<br>
