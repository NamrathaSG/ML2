# BOSTON

## Introduction:
A dataset containing information collected by the U.S Census Service concerning housing in the area of Boston Mass has been given.The dataset contains 14 variables. 

## Aim:
• To perform Exploratory Data Analysis and understand the given data
• To predict Nitrous Oxide Levels for a given value of other variables
• To predict the median value of the House.

## About the Data:
From the given dataset, we can see that there are 14 columns and 506 rows. After checking for duplicates, we observe that there are no duplicates and we retain the dataset as it is.
Out of the 14 variables, 12 of them are continuous whereas, 2 of them , CHAS and RAD are categorical. CHAS has already been substituted by dummy variables and RAD is indexed.

Now, observing the structure of the data:
Mean and Median:
• We see that the mean and median are similar except in the case of ZN, which could be
attributed to the range of values it takes up. Thus showing that ZN is not equally
distributed throughout its range.
• Other variables show slight deviances from in values of mean and median
Inter-Quartile Range and Outliers
• Thus Outliers are any values that lie below Q1 – 1.5 ×IQR or above Q3 + 1.5×IQR.
• We can see that CRIM, ZN, RM and B show significant number of outliers compared to
the rest of the other variables.
Skewness:
• We can see that the variables INDUS and RM are fairly skewed (between -0.5 and 0.5).
• The variables AGE, TAX, PTRATIO, LSTAT and NOX are moderately skewed
• Whereas, CRIM, ZN, DIS, B and MEDV are Highly skewed.
• The positively skewed variables are : CRIM, ZN, INDUS, RM, DIS, TAX, LSTAT,MEDV
and NOX
• The negatively skewed variables are : AGE, PTRATIO and B
  2
 Variance and Standard Deviation
• We see that the standard deviation of ZN, AGE, TAX and B are significantly high,
which implies their values tend to be slightly deviant form the mean.
Kurtosis:
• We see that the kurtosis for variables INDUS, RM, AGE, DIS, TAX, PTRATIO, LSTAT
and NOX lie in the interval are close to zero. Thus, it can be assumed that their values
tends towards a normal distribution.
• The variables, CRIM, ZN, B and MEDV are leptokurtic (thick tailed)
Min-Max and Left3Std and Right3Std
• Left3Std means 3 standard deviations below the mean and right3std refers to 3
standard deviations above the mean
• On comparing these values with that of the min-max values of the dataset, we can see
that B, CRIM and ZN, whose range is way higher than the 3 deviations away from the mean, might tend to have more outliers and thus have more deviation from normal distribution. 


## Treating the Data For Outliers and Missing Values:
Now, the data has been treated for outliers, after which missing values or NaN(Not a Numeric value or blank) have been replaced by the median value. Median has been used so that the outliers treatment do not affect the estimated missing values(like in the case of mean).
Now that the data has been rid of outliers, we check for heteroscedasticity, multicollinearity and autocorrelation in the dataset. 

## Modelling the Given Data
The data has been divided into a training and testing set on the ratio (8:2) and has been used to run the algorithms.
Now, starting with no predictor variables and adding each variable and checking on their impact on the R square value, we model the given dataset into a linear regression model.
