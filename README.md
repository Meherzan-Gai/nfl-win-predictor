# NFL Win Predictor
This is a win predictor for NFL games based on previous data (the current season as well as past seasons).
It uses machine learning and web scraping to gather data and then train on the data.


## Scraping
I used the requests library to get html data from the proreferencefootball database. The html was parsed using BeautifulSoup to find the stats tables for each team during each season scraped.
Regular Season data was scraped for the past 5 seasons.


## Cleaning
Empty values for Home/Away columns, TO columns, and Bye weeks were adjusted to ensure proper data formatting for every team's table.