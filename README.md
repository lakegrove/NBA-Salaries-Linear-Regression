# NBA-Salaries-Linear-Regression

Using stats from [Basketball Reference](https://www.basketball-reference.com/) I will look at players and use statistical categories like points, age and steals as features to map players to an expected salary or worth.

This will help franchises realize which players are under or over achieving within their team to give them ideas of who to trade for to make their team better.  Most importantly, using these predictions, general managers will have a salary in mind for which players to target and how much their fair market value will be based on comparable salary for statistically similar players around the league.  These predictions will then be used to rank or discuss top players for the 2021 free agency market.

## Question/need:
How much should are the 2021 free agent players worth? What should be expected to be paid to be in contention to sign the best players and how do they rank amongst each other?

The beneficiaries of this information are general managers looking to either sign players or not (depending on budget and fit) and who they should target to get the best value on talent. 

## Data Description:

Salary and statistical information will be provided by [Basketball Reference](https://www.basketball-reference.com/).

Considerations include categories like rebounds, points, steals, blocks, assists, turnovers, 3%, height, age and year (salaries tend to be going up over time)

My target for predictions will be salary. 

## Tools

I intend to use beautifulsoup/selenium to scrape the data from the publically available website.  I also intend to use python, pandas, numpy and sickit-learn.

While I am not planning at the start to use other tools, I will consider cloud computing and SQL if they work within the timeline. 

## MVP Goal 

Show simple regression looking at points as the feature to predict salary from the training set.
