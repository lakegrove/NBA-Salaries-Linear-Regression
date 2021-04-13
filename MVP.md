
## NBA Salary Regression

![Screen Shot 2021-04-12 at 9 03 49 PM](https://user-images.githubusercontent.com/19785958/114486035-ab0b1600-9bd2-11eb-941b-cf6c38ca4543.png)

So after splitting our data into train, validation and test splits, we took a look at just what points score per game (PTS - the highest correlation in our heat map) would look like as a single predictor of salary using our training set only with a simple linear regression.  What we saw was pretty that we are off by nearly 3.3 million dollars a player with heavy misses coming for players at the higher end of the salary pool in reality. The shape of this distribution also has me wondering if this category will be a candidate for polynomials. 

While our initial heatmap correlation for scoring was in the low .60s, the above analysis is pointing to an R Squared of just .37.  We've seen from playing around with the whole data set and observing the output from stats package, that something in the .50 to .60 is doable with the entire data set (adjusting salary target distributions and impact of low game outliers). So clearly points alone won't suffice.

The key will be finding the leaders from each bucket (scoring, defense, rebounding, availability, ect) what to pick without over doing a category and causing colinearity issues.  The initial p-values weren't matching up perfectly with the heat map correlations we saw for particular categories (depending on target distribution and outlier allowance) and so there will need to be some experimentation and most likely use of LASSO to help figure out which categories are robust.

The other dilemma we will have in testing is this data is prediction of salary data for actual real life salaries.  We played around with distributions of salary looking at square root salary, log salary and real salary numbers with the latter two lagging the former in terms of helping accuracy (based on the stats model high level overview).  The trick will be to tune the best model while also trying to make for interpretable results.  For now I've ditched log salary as it looks numerically similar to normal salary (though distribution looked better) and will run square root as a side analysis to see how much it can improve vs regular salary.
 
**Residuals**

![Screen Shot 2021-04-12 at 9 33 17 PM](https://user-images.githubusercontent.com/19785958/114488356-d7289600-9bd6-11eb-9e50-db95856f4ccb.png)


Again there seems to be better accuracy around the lower income players (as there is also alot more data for them as they are more common) and salaries become more varied in preidiction as we get to higher paid players

