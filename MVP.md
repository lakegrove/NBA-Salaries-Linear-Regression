## NBA Salary Regression

![Screen Shot 2021-04-12 at 9 03 49 PM](https://user-images.githubusercontent.com/19785958/114486035-ab0b1600-9bd2-11eb-941b-cf6c38ca4543.png)

So after splitting our data into train, validation and test splits, we took a look at just what points (the highest correlation in our heat map) would look like a single predictor of salary.  What we saw was pretty that we are off by nearly 3.3 million dollars a player with heavy misses coming for players at the higher end of the salary pool in reality.

While our correlation was in the low .60s for scoring on the heat map, the above analysis is pointing to an R Squared of just .37.  We've seen from playing around with the whole data set, adjusting salary target distributions and impact of low game outliers that something in the .50 to .60 range could be reasonable when we have all the categories in there, so clearly points alone won't suffice.

The key will be finding the leaders from each bucket (scoring, defense, rebounding, availability, ect) what to pick without over doing a category and causing colinearity issues.  The initial p-values weren't matching up perfectly with the heat map correlations we saw for particular categories (depending on target distribution and outlier allowance).

The other dilemma we will have in testing is this data is prediction of salary data for actual real life salaries.  We played around with square root salary, log salary and real salary numbers with the latter two lagging the former.  The trick will be to tune the best model while also trying to make for interpretable results. 


