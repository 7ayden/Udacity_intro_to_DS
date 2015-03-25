# Udacity_intro_to_DS
Section 1. Statistical Test
1.1	Which statistical test did you use to analyze the NYC subway data? Did you use a one-tail or a two-tail P value? What is the null hypothesis? What is your p-critical value?

Mann-Whitney U test is more applicable in this data analysis, since there is no prior information on the data set whether it is based on parameterized families of probability distributions.
 
In this case, using two-tailed test enables to test the possibility of the relationship in both directions. In another way of saying, two-tailed test is to see if two means are different from each other. 

In the null hypothesis, null hypothesis sets both populations are the same and p-critical value is 5%. 

1.2	Why is this statistical test applicable to the dataset? In particular, consider the assumptions that the test is making about the distribution of ridership in the two samples.

Mann-Whitney U test is used when two variables are not normally distributed and both groups have the same shapes. A graph from the problem sets on exploratory data analysis, shows that both raining and when not raining are the same shape. Therefore, a Shapiro-Wilk test is use in this case to test whether or now both data sets are normal distributed quantitatively.

1.3 What results did you get from this statistical test? These should include the following numerical values: p-values, as well as the means for each of the two samples under test.

Through the Shapiro- Wilk test,  p – value is 0.024999912793489721, the mean of the raining is 1105.4463767458733, the mean of without raining is 1090.278780151855 and U-statistic is 1924409167.0.

1.4	What is the significance and interpretation of these results?

In order to interpret the Mann-Whitney test result, first compares both unpaired group that is the mean of the rain and without rain set, and to tank the smaller number first .In this case, without rain is small that has a 10.9 % vs. rain that has 11.05%.

Secondly, know the null hypothesis in order to interpret the P value, is to find out where U (the number of comparison equals to the product of rain and without rain), is bigger than 50% bigger than accepted Null, verse vice, if smaller than 50% we accept Hypothesis.
 
Section 2.
Linear Regression

2.1 What approach did you use to compute the coefficients theta and produce prediction for ENTRIESn_hourly in your regression model:
Using gradient descent on machine learning algorithm enables to compute the coefficients. By setting the alpha to 0.04 and number of iterations to 100, the graph shows local minimum perfectly. 
2.2 What features (input variables) did you use in your model? Did you use any dummy variables as part of your features?

I selected different features and turned out variables such as rain (best one), hour, precipitation (in inches at the time and location), average of wind speed and temperature. Addressing the over-fitting issues, reducing the number of features raises the R-squared value. 
Unit is the dummy variable that uses as a feature, which is identification for each location. 

2.3 Why did you select these features in your model? We are looking for specific reasons that lead you to believe that the selected features will contribute to the predictive power of your model.
The best r-squared is from rain, precipitation, hour, the mean of wind-speed and temperature. First of all, rain is the biggest hypothesis of whether raining affects the amount of passengers. Second, other similar features such as wind-speed, temperature or precipitation affects the passenger in the same fashion.
2.4 What are the coefficients of the non-dummy features in your linear regression model?
The non-dummy features I used for my linear regression model are rain, precipi, hour, meantempi.

2.5 What is your model’s R2 (coefficients of determination) value?

My calculated R^2 value is: 0.463968815042
2.6 What does this R2 value mean for the goodness of fit for your regression model? Do you think this linear model to predict ridership is appropriate for this dataset, given this R2  value?

The goodness of fit is also known as the sum of the squares of the vertical distances of the points from the line. In which my model has 46.4% of variations that fits to the model. The low or high R-squared does not inherently bad or good, if the significant predictors in a low R-squared, conclusions still should be drawn. Likewise, a high R-squared might lead to an underspecified model (that means missing important predictors). 

Plotting residuals is a good way to exam weather the prediction of ridership is appropriate or not. 

The plot shows residuals within 0 to+- 5000 range mostly. Therefore the linear model is sufficient to predict the ridership. 
Section 3.
Visualization

3.1 One visualization should contain two histograms: one of  ENTRIESn_hourly for rainy days and one of ENTRIESn_hourly for non-rainy days.

 
3.2 A bar chart of Average Entry Hourly

 
 
Section 4.
Conclusion
4.1 From your analysis and interpretation of the data, do more people ride the NYC subway when it is raining or when it is not raining?

Before the analysis, I thought there would be less ridership during the raining. Through the Mann-Whitney U test that compares both mean of entries with and without rain, the difference is only 0.2%. However, the mean alone still does not justified which has more riders due to variance. 

At Mann-Whitney U test, the p-value of 0.025 states there are more riders in raining day.

4.2 What analyses lead you to this conclusion? You should use results from both your statistical tests and your linear regression to support your analysis.

As the previous answer stated, the ridership during the raining day has more than the non-raining day with the Mann-Whitney U test analysis that requires a deeper analysis beyond the comparison of both variable mean. Through the R squared with the 46% means that it is highly accurate.  
Section 5.
Reflection
5.1 Please discuss potential shortcomings of the methods of your analysis, including:
1.	Dataset,
2.	Analysis, such as the linear regression model or statistical test.
The dataset treats all of the Units, which are the stations locations affects equally that is part of the shortcomings. In reality the Units contribute different amount of riders, not to mention the populations density are varies from different units due to the accessibility or different other factors. Therefore, overall raining might affect the amount of riders, but a precise analysis can be done.
Speaking of the analysis, I would love to include different factors such as the traffic other transportations data, and such to raise the r squared. Also perhaps analysis through a geographic chart might be a good way to discover better questions and answers.

5.2 (Optional) Do you have any other insight about the dataset that you would like to share with us?
 
Reference: 

Choosing the Coorect Statistical test
http://bama.ua.edu/~jleeper/627/choosestat.html

Nonparametric statistics
http://en.wikipedia.org/wiki/Nonparametric_statistics

T-test
http://en.wikipedia.org/wiki/Student%27s_t-test

Mann-Whitney U test
http://en.wikipedia.org/wiki/Mann%E2%80%93Whitney_U_test

One tailed and tailed tests
https://www.khanacademy.org/math/probability/statistics-inferential/hypothesis-testing/v/one-tailed-and-two-tailed-tests

1 vs 2 Tailed Tests
http://www.chem.utoronto.ca/coursenotes/analsci/stats/12tailed.html

Mann-Whitney U Test using SPSS
https://statistics.laerd.com/spss-tutorials/mann-whitney-u-test-using-spss-statistics.php

Interpreting results: Mann-Whitney Test
http://www.graphpad.com/guides/prism/6/statistics/index.htm?how_the_mann-whitney_test_works.htm

Machines learning Andrew Ng Linear Regression: cost function
https://class.coursera.org/ml-006/lecture/40

r2, a measure of goodness-of-fit of linear regression
http://www.graphpad.com/guides/prism/6/curve-fitting/index.htm?r2_ameasureofgoodness_of_fitoflinearregression.htm

