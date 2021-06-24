# Predicting NBA Player Salaries through Statistics

## Abstract
In every professional sport, player acquisitions during free agency is arguably one of the most important factors of a team's success when done correctly.
We have seen Championship dreams solidify during this time, way before the season begins. With Lebron James and Chris Bosh joining the Miami Heats in 2010
and Kevin Durant to the Golden State Warriors in 2016. On the other hand, we have contracts like Chandler Parson(4-Year, $94M and Joakim Noah(4-Year $72M) 
that drastically increase a team's chances of a high lottery pick. In order to predict a players salary our model uses the previous seasons statistics.
    
The initial dataset consisted of over 2000 contracts from the past decade. After filtering out head coaches, 10-day, 2-way and many others; the dataset 
dwindled down to a final 573. Using a correlation heatmap for feature selection I was able to narrow down to 10 features (9 continuous & 1 categorical) 
from the initial 38. Using Linear Regression and a Random Forest Regressor our R-Squared came back very similar, after tuning the data, we were able to 
get an R-squared of  0.53 and 0.57 respectively.

The results seem to contain a lot of extremes on both ends.Both models underestimated players like Chris Paul, Khris Middleton, and Jimmy Butler. 
On the opposite end both models overestimated veterans like Paul Pierce, Vince Carter and Manu Ginobli.

In conclusion, the rise of analytics has enabled us to understand every aspect of a players game but still a bit away from understanding a players monetary value.
Further analysis is required to understand the overvaluing and undervaluing of a player. As long as contracts are written and offered by humans there will always 
be intangible factors but with advanced analytics and machine learning we can look forward to more accurately determining a players monetary value.

## DATA Collection // Exploration

2000 individual contracts and player statistics were collected from Spotrac & Basketball-References API. After cleaning the data, 573 contracts with 10 features were
used to train the models.

![Contracts by Year](/Images/FA_signings_Per_Year.png)

Features were selected based on their correlation values to a players AAV

![Corr AAV and features](/Images/feature_correlation_W_AAV3.png)

## Linear Regression

![Linear Regression Results](/Images/LR_results.png)

## Random Forest Regressor

![RFR Results](/Images/RFR_result.png)

## Future Work & Improvements

- Better Data collection // The data collected were of every NBA contract sign in the past decade (2011-2020). Since the motivation of the project 
  is to predict free agents salary based on their performance of the previous year(s), contract such a rookie deal, free agent pick up can mess with the data.
- Run the model through a multi-year average statistics of a player(e.g Avgerage stats for the previous 3-years)
- Seperate Free-Agent contract by year. Due to the nature of the NBA salary cap, a player with the same stats can be offer different amount due to a teams cap space. 
  // AAV as a % of the total salary cap.
