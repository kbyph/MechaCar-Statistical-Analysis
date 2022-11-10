# MechaCar Statistical Analysis - Statistics and R

## Overview of Project
- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

## Resources
- Software
  - RStudio
  - R
- Tools
  - dplyr
  - ggplot2
- Data Source
  - MechaCar_mpg.csv
  - Suspension_Coil.csv

## Linear Regression to Predict MPG 
The MechaCar dataset contains a sample size of 50 prototypes measuring the miles per gallon across multiple variables. To perform the linear regression, calculations were made using R in RStudio.
### Linear Regression
A multiple linear regression analysis was performed to determine which variables predict the mpg of MechaCar prototypes.
- ![image](https://user-images.githubusercontent.com/102638461/182289420-7056ecdf-9740-49ab-a60c-cfe5f894833a.png)

### Linear Regression Summary
The summary of the linear regression determines the quality of the dataset, measuring values such as the residuals, coefficients, significant codes, R-squared and p-values.
- ![image](https://user-images.githubusercontent.com/102638461/182289534-7ff96b1d-ff81-4a99-816c-6fe925a0e365.png)

Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
- The vehicle length and ground clearance are both likely to provide non-random amounts of variance towards the model. In contrast, the vehicle weight, spoiler angle, and AWD have p-Values that indicate random amounts of variance. 

Is the slope of the linear model considered to be zero? Why or why not?
- Since the p-Value for this model is much smaller than the assumed significance level of 0.05%, this indicates that there is enough evidence to reject the null hypothesis, meaning that the slope of this linear model can not be zero.

Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
- According to the linear regression summary, the r-squared value is 0.7149, meaning that 71.49% of the variability of the dependent variable mpg is explained by the model. Therefore, the linear model does predict mpg of MechaCar protypes quite effectively.

## Summary Statistics on Suspension Coils
The Suspension Coil dataset provided contains the results of testing the weight capacities for multiple suspension coils in three different production lots.
### Total Summary
- ![image](https://user-images.githubusercontent.com/102638461/182292576-db30a307-1b3f-4199-9245-38df1d2e3fba.png)

### Lot Summary
- ![image](https://user-images.githubusercontent.com/102638461/182292900-318aedeb-a1af-4954-a1da-a06346a108f1.png)

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
- The overall variance, as shown in the Total Summary data above, is under 100 psi and meets quality specifications. However, the variance for Lot 3 shown in the lot summary is well over the acceptable threshold at 170.28.

## T-Tests on Suspension Coils
### T-test for all Lots
All Manufacturing Lots: p-value = .6028 > 0.05, which means the total manufacturing lot is not statistically significant from the normal distribution.
- ![image](https://user-images.githubusercontent.com/102638461/182290052-cba5e301-fc2b-4302-afe5-43ef5dfb701e.png)

### T-test for Lot 1
Lot 1: p-value = 1 > 0.05, which means Lot 1 is not statistically significant from the normal distribution.
- ![image](https://user-images.githubusercontent.com/102638461/182290156-f056a786-50c4-422b-a151-b72efd444d3b.png)

### T-test for Lot 2
Lot 2: p-value = 0.6072 > 0.05, which means Lot 2 is not statistically significant from the normal distribution.
- ![image](https://user-images.githubusercontent.com/102638461/182290216-b37299c2-adae-461c-ae61-450ea9fa0b8d.png)

### T-test for Lot 3
Lot 3: p-value = 0.04168 < 0.05, which means Lot 3 is very much statistically significant from the normal distribution.
- ![image](https://user-images.githubusercontent.com/102638461/182290348-f9a35535-2093-4027-83a1-c2a6db21beea.png)

The overall manufacturing, Lot 1, and Lot 2 show a normal distribution. However, there is not enough evidence to reject the null hypothesis, showing that the two are statistically similar.

## Study Design: MechaCar vs Competition
In comparison to MechaCar's competitors, metrics that could be measured that would spark a consumer's interest could include car prices, fuel efficiency, horsepower, safety ratings, or average service costs.

- What metric or metrics are you going to test?
  - The metrics I would test would be fuel efficiency, service costs and safety ratings because those metrics would be prioritized in order to determine the longevity of the vehicle itself.
- What is the null hypothesis or alternative hypothesis?
  - The null hypothesis is that the mean of each criteria equals zero. The alternative hypothesis is that the mean is any value above or below zero.
- What statistical test would you use to test the hypothesis? And why?
  - ANOVA tests to determine the means of each variable, and multiple linear regression summaries to compare between each competitor in the market.
- What data is needed to run the statistical test?
  - A sample size of around 50 cars for each competitor, including the same variables and data values as above. 
  
