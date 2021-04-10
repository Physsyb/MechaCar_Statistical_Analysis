# MechaCar_Statistical_Analysis
# Project Overview
A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team. This assignment consists of three technical analysis deliverables and a proposal for further statistical study. You’ll submit the following:
- Deliverable 1: Linear Regression to Predict MPG
- Deliverable 2: Summary Statistics on Suspension Coils
- Deliverable 3: T-Test on Suspension Coils
- Deliverable 4: Design a Study Comparing the MechaCar to the Competition

In this challenge, you’ll help Jeremy and the data analytics team do the following:
- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

# Resources
Data Source: `MechaCar_mpg.csv` and `Suspension_Coil.csv`
Data Software: 'RSudio` and `R`

# Deliverable 1
> The `MechaCar_mpg.csv` dataset contains mpg test results for 50 prototype MechaCars. The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. Using your knowledge of R, you’ll design a linear model that predicts the mpg of MechaCar prototypes using several variables from the `MechaCar_mpg.csv file`. Then, you’ll write a short interpretation of the multiple linear regression results.

## Technical Analysis
- #### An RScript is written for a linear regression model to be performed on all six variables
    ![1](https://user-images.githubusercontent.com/76136277/114251426-f6bd8580-996e-11eb-8300-c339aa2999eb.PNG)

- #### An RScript is written to create the statistical summary of the linear regression model with the intended p-values
    ![2](https://user-images.githubusercontent.com/76136277/114251431-fd4bfd00-996e-11eb-9def-2e9a1e0d0fcc.PNG)

## Linear Regression to Predict MPG 
1. #### Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
    - The vehicle length, and vehicle ground clearance are likely to provide non-random amounts of variance to the model. That is, the vehicle length and vehicle ground clearance have a significant impact on miles per gallon on the MechaCar prototype. The vehicle weight, spoiler angle, and All Wheel Drive (AWD) have p-Values that indicate a random amount of variance with the dataset.
2. #### Is the slope of the linear model considered to be zero? Why or why not?
    - The p-Value for this model, p-Value (5.35e-11), is smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis, and further indcates that the slope of this linear model is not zero.
3. #### Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
    - This linear model has an r-squared value of 0.7149, which means that about 71% of all mpg predictions will be determined by this model. Therefore, this multiple regression model does predict mpg of MechaCar prototypes effectively.
![2](https://user-images.githubusercontent.com/76136277/114252019-41400180-9971-11eb-826a-b4a2fa023b65.PNG)

 # Deliverable 2
  > The MechaCar Suspension_Coil.csv dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots.

## Technical Analysis
- #### An RScript is written to create a total summary dataframe that has the mean, median, variance, and standard deviation of the PSI for all manufacturing lots   
  ![3](https://user-images.githubusercontent.com/76136277/114252244-39cd2800-9972-11eb-9d69-d48d643b71eb.PNG)
  ![3b](https://user-images.githubusercontent.com/76136277/114252247-3c2f8200-9972-11eb-861d-3f604ce63fa2.PNG)

- #### An RScript is written to create a lot summary dataframe that has the mean, median, variance, and standard deviation for each manufacturing lot 
   ![4](https://user-images.githubusercontent.com/76136277/114252311-8153b400-9972-11eb-80e6-94609ef85b21.PNG)
   ![4b](https://user-images.githubusercontent.com/76136277/114252314-83b60e00-9972-11eb-9fa8-8c4bc83cb57a.PNG)

- #### There is a summary that addresses the design specification requirement for all the manufacturing lots 
   ![Rplot for Whole Lot](https://user-images.githubusercontent.com/76136277/114252330-929cc080-9972-11eb-8331-f826c496b785.png)

- #### There is a summary that addresses the design specification requirement for each lot individually
   ![Rplot Individual Lot](https://user-images.githubusercontent.com/76136277/114252339-9af4fb80-9972-11eb-8de7-fc4f45d36e6c.png)

## Summary Statistics on Suspension Coils
The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
- Looking at the entire production lot, the variance of the coils is 62.29 PSI, which is well within the 100 PSI variance requirement. However, Lot 1 and Lot 2 are significantly more consistent and well within the 100 PSI variance requirement; with variances of 0.98 and 7.47 respectively. Finally, Lot 3 shows larger variance in performance and consistency, with a variance of 170.29. Therefore, Lot 3 is disproportionately causing the variance at the full lot level.
![Rplot Individual Lot](https://user-images.githubusercontent.com/76136277/114252507-a7c61f00-9973-11eb-9cbf-55b8e62e052a.png)

# Deliverable 3
> sing your knowledge of R, perform t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.

## Technical Analysis
- #### An RScript is written for t-test that compares all manufacturing lots against mean PSI of the population
  ![5](https://user-images.githubusercontent.com/76136277/114252762-f2946680-9974-11eb-911d-baafcd8b6dd6.PNG)

- #### An RScript is written for three t-tests that compare each manufacturing lot against mean PSI of the population 
   ![6](https://user-images.githubusercontent.com/76136277/114252766-f627ed80-9974-11eb-8154-4ddc6949da75.PNG)

## T-Tests on Suspension Coils
> There is a summary of the t-test results across all manufacturing lots and for each lot.

1. **ALL Lots**  - The mean of the sample is 1498.78 and the 'p-Value` is 0.06 which is higher than the common significance level of 0.05. Therefore, we do not have enough evidence to support rejecting the null hypothesis. That is, the mean of all three of these manufacturing lots is statistically similar to the presumed population mean of 1500.

    ![5](https://user-images.githubusercontent.com/76136277/114252926-ccbb9180-9975-11eb-92a5-dfff33e763b8.PNG)

2. **Lot 1** - The mean of the sample is **1500** and the `p-Value` is **1** , therefore,  we cannot reject the null hypothesis that there is no statistical difference between the observed sample mean and the presumed population mean of 1500.
   ![6a](https://user-images.githubusercontent.com/76136277/114253077-89155780-9976-11eb-9a67-46d858d78f05.PNG)

3. **Lot 2** - The mean of the sample is **1500.02** and the `p-Value` is **0.61**. The null hypothesis cannot be rejected, and the sample mean and population mean of 1500 are statistically similar.

   ![6b](https://user-images.githubusercontent.com/76136277/114253129-cc6fc600-9976-11eb-8917-166b5bd5b8d1.PNG)

4. **Lot 3** - this is a different from other lots because the sample mean is **1496.14**, and the `p-Value` is **0.04**. This is lower than the common significant level of 0.05, and has safely indicated to reject the null hypothesis, that is, the sample mean and the presumed population mean are not statistically different.

   ![6c](https://user-images.githubusercontent.com/76136277/114253315-be6e7500-9977-11eb-90c8-f029ea5c525d.PNG)

# Deliverable 4
> Using your knowledge of R, design a statistical study to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers.

## Study Design: MechaCar vs Competition
1. #### Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating. The statistical study design has the following:
  - A metric to be tested
  - A null hypothesis or an alternative hypothesis described
  - A statistical test to test the hypothesis
Also, this study would involve collecting data on MechaCar and its comparable models across several different manufacturers over the last 3 years. Some of the data to be collected includes, the competitor's comparable models, factors to help determine the selling price, cars MechaCar will be competing with etc.
2. #### In your description, address the following questions:
- #### What metric or metrics are you going to test?
   - Average Annual Cost of ownership (Maintenance)
   - Safety Feature Rating
   - Engine (Electric, Hybrid, or  Gasoline)
   - Current Selling Price:
   - Resale Value
   - Fuel Efficiency

- #### What is the null hypothesis or alternative hypothesis?
   - Null Hypothesis (Ho): MechaCar is priced correctly based on its performance of key factors for its genre.
   - Alternative Hypothesis (Ha): MechaCar is not priced correctly based on performance of key factors for its genre.

- #### What statistical test would you use to test the hypothesis? And why?
A multiple linear regression would be used to determine the factors that have the highest correlation/predictability with the list selling price, and which combination has the greatest impact on price.
