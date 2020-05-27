ETL Project Report
Jordon, Kelby, Mitra, Niama

Extract & Transform
The  first two datasets we used to build our Player Profiles were all csv files from Kaggle.com('Players' and 'player_data').
-	We want Player Names, Career Positions, Height in Centimeters, Weight in Pounds, College, City and State of Birth.
'Players.csv' holds data for players' birth city and birth states as and weight in pounds, we import that csv into a Pandas DataFrame. Next, we see 'players_data.csv'  holds data for players' college, Career Position, and height in centimeter , we import that csv into a Pandas DataFrame as well and rename the column ‘name’ to ‘Player’.
Now we will merge the two data frames together on ‘Player’ .
Next, we create 3 data frames to ensure the most full and accurate information is selected (PPD, P_htwt, and P_college).
Now we import the Latitude and Longitude for all 50 American states(‘50_lat_lng.csv’), with was retrieved from INKPlant.com and rename the column ‘Place Name’ to ‘State’ and then we merge the DataFrame with ‘PPD’.
Next, we removed all non US born players with a .dropna().
Then, we merge that data Frame with the P_htwt (players height and weight) DataFrame and once again remove players with incomplete data, such as weight, and removed all Duplicates as well.
------We have a Complete Player Profile----
Now we import the Latitude and Longitude for all NBA teams 2010-2015 and the NBA Player  Association((‘NBATeamLL.csv’)wikipedia.com & Google.com).
- NBA team LAt and Lng cam from Wikipedia. of which was copied and pasted in to excel and saved as a csv file which were than reformatted in VSCode and save for use in Python.
Additionally we’ll import NBA Yearly Season Stats (‘season_stats.csv’) and rename columns of which will plan to use. (team, Rebounds, Steals, Blocks, Assists, Points, Player Rating).
Next, we merge the two DataFrames on ‘Team’ and create a new DataFrame selecting only the columns of which we plan to explore, and create another DataFrame from the previous Selecting those rows with or between the ‘Years (2010-2015).
Once more we merge or ‘Player Profile’ DataFrame with our Seasonal Stats on ‘Player’ and for the final time we will remove all player with incomplete data from the dataFrame. 
and for our final merge we bring include P-College(player colleges) on players as well. And add Column ‘MapPt’ with a consistent value of “3” for data Mapping on Goggle Maps. 
Load:
 Databases were cleaned and formatted in pandas then transferred to SQL tables using an engine connection using SQLAlchemy.  Along the way we were reminded by multi errors that lower casing is best for pandas unles you Define the your tables with quotations.
(ex. Nba = bad  ,  nba= good or "Nba"=good ) . with that problem solved uploading and our data frame to our SQL NBA DataBAse was complete.


