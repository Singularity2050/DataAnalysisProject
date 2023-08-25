# DataAnalysisProject

# Objective
The World Happiness Report is a landmark survey of the state of global happiness that ranks countries by how happy their citizens perceive themselves to be. The report gains global recognition as governments, organizations and civil society increasingly use happiness indicators to inform their policy-making decisions. This project allows us to gain insight into the state of happiness in the world today.

# Data Collection & Data Preprocessing
<img width="893" alt="Screenshot 2023-08-25 at 5 00 37 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/47c4f23a-b40e-48bc-81b2-3e43245dce4d">

# Contextual Descriptive Analysis
## Cardinality and Count

<img width="419" alt="Screenshot 2023-08-25 at 5 01 58 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/236c4e3f-739d-48fa-bb13-fa2406ad71c3">

Some countries' happiness rankings have improved, some have remained stable, and others have declined. More countries have seen an improvement than a decline, with stable countries in between. Countries that have improved may have experienced economic, social, or political improvements, while stable countries tend to have strong support systems and low corruption. Countries that have declined have experienced significant drops in their rankings, with examples ranging from Japan to Zimbabwe.

## Distribution
The values represent the density of the Happiness Scores at specific points for each year. 
The density values indicate how concentrated the Happiness Scores are around the specific points for each year. Higher density values mean that there are more observations with Happiness Scores close to that specific point for the given year.

<img width="191" alt="Screenshot 2023-08-25 at 5 02 50 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/fb50a590-39f5-4923-bb70-13305ea3daaa">

## Q-Q Plot of Happiness Score 2015-2019
<img width="784" alt="Screenshot 2023-08-25 at 5 03 43 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/f38ca447-ea9a-4c44-93c1-282fa1f09721"><img width="181" alt="Screenshot 2023-08-25 at 5 03 57 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/8df9bca9-6315-4fb6-8e51-d770dfbb6897">

The Q-Q plots show that the points lie approximately along a straight line, further suggesting that the Happiness Scores could be normally distributed or at least follow a distribution similar to normal. While there may be some deviation from a perfect normal distribution, these visualizations indicate that the data is close to being normally distributed, and any statistical analyses that assume normality can be considered reasonably valid


## Shapiro-Wilk test
<img width="290" alt="Screenshot 2023-08-25 at 5 04 21 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/7519db72-0987-4b2e-9081-dd80262b8489">

The Shapiro-Wilk test is a statistical test to assess the null hypothesis that a given sample comes from a normally distributed population. If we choose a p-value of 0.01, none of the years' Happiness Scores are rejected as coming from a normally distributed population.

It's worth noting that the test statistics for all years are very close to 1, which implies that the deviation from normality is likely to be small, even for the years where the null hypothesis is rejected.

## Quantile Statistics 
<img width="396" alt="Screenshot 2023-08-25 at 5 05 25 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/4f0f40cb-bb90-40f9-b7fa-2a2828011bc7">

By examining these quantile statistics, we can observe the central tendency (median) and spread (difference between Q1 and Q3) of the Happiness Scores for each year. These quantile statistics can help us understand how the Happiness Scores are distributed across countries in each year's dataset and provide insights into the overall trends in happiness levels across different countries.

## Central Tendency
<img width="376" alt="Screenshot 2023-08-25 at 5 05 51 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/88e1e881-5984-4533-b463-7ae9755d78c2">


The output displays the mean, median, and mode of Happiness Scores for each year from 2015 to 2019. The mean and median both show a slight increase in happiness levels over time, while the mode varies, indicating that the most common happiness level has changed each year.
The mode, however, might not be the best measure to represent the central tendency of the data, as it varies more and may not accurately reflect the overall trend in happiness scores.

## Variability
<img width="391" alt="Screenshot 2023-08-25 at 5 06 12 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/cfc8a48f-ca17-4698-bfd2-1c11bc22cba6">

The variability of happiness scores, which provides insight into the spread or variability of the data, has also remained relatively stable across the years, even decreasing slightly.

# Correlation Analysis
## Qualitative Analysis
<img width="447" alt="Screenshot 2023-08-25 at 5 07 00 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/17d2939c-d728-49f8-b6a7-5a6284203715">

The scatterplots show that Happiness Score and Economy (GDP per Capita) and Family have a strong positive correlation. Happiness Score and Health (Life Expectancy) and Freedom have a moderate positive correlation. Happiness Score and Trust (Government Corruption) and Generosity have a weak positive correlation.

## Quantitative Analysis
<img width="340" alt="Screenshot 2023-08-25 at 5 07 30 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/4c16bf98-4d22-437f-963f-099c52a7cd99">

Based on the correlation matrix, the features that contribute the most to happiness are Economy, Family, and Health. A president of a country should focus on improving the economy, fostering social support, and promoting public health to make citizens happier. Additionally, they may also consider promoting freedom, reducing corruption, and encouraging generosity, as these factors also have a statistically significant, positive correlation with happiness.

# Feature Selection
## Model Selection

We chose Embedded methods because they are more efficient and can potentially perform better than filter and wrapper methods. 
For this task, the embedded methods to be used are:

1. Ridge Regression
2. Decision Tree Regressor
3. Random Forest Regressor

These models were chosen because they are simple and easy to interpret, commonly used for regression tasks, are relatively fast to train, and can handle large datasets.


## Model Training 
Split the data into features and target variables
Separated Train and evaluate data to be used by each model
Trained the default models 
Fine-tuned the default models and trained them, too*
* Fine-tuning involves cross-validation

## Model Testing Ridge regression
Default Model
<img width="405" alt="Screenshot 2023-08-25 at 5 11 08 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/797a0162-09a7-4fed-ae0e-9eb2d5cea0e1">

Fine Tuning Model
<img width="405" alt="Screenshot 2023-08-25 at 5 10 43 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/bd653cb2-d30c-4a59-ae44-5109646c433b">

<img width="364" alt="Screenshot 2023-08-25 at 5 11 41 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/bba1f33f-e20b-4bd3-9648-db3f7c033bc8">

## Model Testing 
Default Model
<img width="405" alt="Screenshot 2023-08-25 at 5 12 05 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/f40d187f-08f9-4189-93ba-7bdf38b976d1">

Fine Tuning Model
<img width="405" alt="Screenshot 2023-08-25 at 5 12 38 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/0136051d-9690-4ca6-bfbb-800257fcae0a">

<img width="364" alt="Screenshot 2023-08-25 at 5 12 41 PM" src="https://github.com/Singularity2050/DataAnalysisProject/assets/67400401/e60ea190-0a68-498d-8036-ec9296dd8f73">









