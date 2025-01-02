
# NFL Win Predictor

This is a win predictor for NFL games based on previous data (the current season as well as past seasons).
It uses web scraping to gather general team data from past seasons and then train on the data using a Random Forest Model.


## Scraping Data
I used the requests library to get html data from the proreferencefootball database. The html was parsed using BeautifulSoup to find the stats tables for each team during each season scraped.
Stats tables were converted into pandas dataframes. This created a total of 32 teams
\* 5 seasons or 160 dataframes.
Regular Season data was scraped for the past 5 seasons.




## Fixing Data
The dataframe....****FILL IN****
Empty values for Home/Away columns, TO columns, and Bye weeks were adjusted to ensure proper data formatting for every team's table. Future games from the current season were removed from the dataset.



## Training Models 
Multiple random forest models are made with different predictors. All predictors will include the team and opponent as well as home/away. From there multiple different models are made with predictors including yards, turnovers, and other stats for both offense and defense.


## Predicting Week 17 Games
The models are all used to then make a sample prediction for future week 17 games.
This is partially used to analyze the correctness of the model. Models that tend to 
predict majority losses or majority wins instead of a 50-50 split of wins and losses
are more overfitted and hence adjustments need to be made either to the predictors or the model
