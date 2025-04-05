# Predicting-Housing-Prices-
Predicting Housing Prices : Analysing market trends and key influencing factors
1. Data Loading and Initial Exploration Loaded the dataset from train.csv using pandas

Examined basic statistics (mean, median, percentiles) for numerical features

Checked for missing values and data types in each column

Analyzed the distribution of the target variable (SalePrice)

2. Exploratory Data Analysis (EDA) Visualized the distribution of SalePrice (right-skewed, requiring log transformation)

Identified columns with >80% missing values (e.g., PoolQC, Alley)

Explored relationships between key features and sale price:

GrLivArea (living area): Strong positive correlation with price

OverallQual (quality rating): Clear quality-price trend

Neighborhood: Location-based price variations

3. Data Preprocessing Handled Missing Values:

Dropped columns with >80% missing data

Imputed categorical missing values with "None"

Filled numerical missing values with median/neighborhood-based imputation

Feature Engineering:

Created combined features: TotalSF (total square footage), TotalBath

Applied log transformation to SalePrice

Categorical Encoding:

Ordinal encoding for quality-related features (e.g., ExterQual)

One-hot encoding for nominal features (e.g., Neighborhood)

4. Model Development Trained and evaluated:

Linear Regression (Baseline: R²=0.76)

Random Forest (R²=0.89)

XGBoost (Best performance: R²=0.89, RMSE=$0.14)

Feature Importance Analysis:

Top drivers: OverallQual, GrLivArea, TotalBsmtsF

5. Geospatial Analysis Highest-priced neighborhoods: StoneBr, NridgHt

Lowest-priced neighborhoods: MeadowV, IDOTRR

Proximity impact: Homes near railroads sold for 13% less

6. Deployment and Results Processed test data using the same pipeline

Generated predictions with XGBoost

Final Metrics:

MAE: $0.10

R²: 0.888

Key Insights Top Price Drivers: Overall quality, living area size

Affordable Housing: Smaller lots (<5,000 sqft) in IDOTRR

Risk Factors: Railroad proximity reduced prices by 15%

Tools Used Python, pandas, scikit-learn, XGBoost

Files train_cleaned.csv: Processed training data

new_submission.csv: Final predictions
