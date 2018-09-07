# Kaggle: Costa Rican Household Poverty Level Prediction
[See Kaggle Competition](https://www.kaggle.com/c/costa-rican-household-poverty-prediction)

### What is the Goal?
For this challenge, my ultimate goal is to build a income classifier based on demographics and household characteristics in Costa Rica. This project came about because the Inter-American Development Bank (IADB), the largest source of development financing for Latin America and the Caribbean, was interested in improving the accuracy of the Proxy Means Test model which focuses on traditional means of assessing income: observable household attributes such as the material of walls or on the assets found in the home. Unfortunately these means are often difficult to represent a poorer population and have led social aid programs such as IADB with uncertain standards to distribute money by. While this particular challenge will benefit Costa Rica’s aid distribution, the larger hope is to be able to apply similar methods to other developing countries. 

### Data Sets
Provided in Kaggle Competition:
- A training set with about 9500 rows representing individuals, 141 features and one target variable. This training set includes household characteristics and demographic information. The target variable indicates groups of income level: 1 = extreme poverty, 2 = moderate poverty, 3 = vulnerable households and 4 = non vulnerable households. 
  
  - Note: Multiple people can be a part of a single household; unique households are identified by an id.
  
- A testing set, including all the same features as the training set except for the target.  

### Process (work in progress...)
In order to explore the data, my first task was to assess the completeness of the information. I was fortunate to discover that of the five features with missing data, only three of them were significant and easily remedied. The first two variables were definitionally due to 0’s accidentally being represented as nulls. The third variable, only included information for those between the ages of 7-17 and therefore only made up 1629 data points out of the 9557 rows. Since imputing 0’s throughout this column would dilute any significance we could possibly extrapolate, I opted to drop it completely. The latter two columns with missing data were actually calculated columns based off of information from other connected columns. Using the data dictionary to recreate what the formula was, and after performing a quick check for accuracy, there seemed to be a discrepancy in the given values. In order to eliminate the remaining nulls, I first used my formula to correct the given information and then imputed the rest to 0 as indicated by the column’s definition. 
Before building out a model, my next step will be to explore the now complete dataset at hand. As both individuals and households are uniquely represented in the dataset, I will first attempt to create two tables and visually explore them individually. 
