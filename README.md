This  project is to see who the data says the greatest NBA player of all time is, the NBA's GOAT for short. To develop a GOAT score a weighted average of different features was used.
The first step of creating a score was to determine which features to  include in the weighted average. A little over a year ago, a Reddit user, natekchua, posted a poll  to see who people thought the GOAT was and what measurements voters thought were important when evaluating who the GOAT is (https://docs.google.com/forms/d/1iEbVeolgRd8VuFOx7WygLEPWk4XNVexktswDJyt0n5U/viewanalytics). Nine of the top ten most voted measurements in the survey were used (Could not find career win rate by player data).

Top 9 were

1. Career Stats (split between minutes per game, points, rebounds per game, assists per game, steals per game and blocks  per game)
2. Championships 
3. Regular Season MVPs (Most Valuable Player Award) 
4. Win Shares per 48 minutes
5. Advanced Stats (Split between PER, BPM, and VORP)
6. Finals MVPs 
7. Total Points
8. All-Star Selections
9. All NBA Selections

The Data for all these features was taken from https://www.basketball-reference.com/.  One hurdle for this project, however, was that not all data goes back to the beginning of the NBA. In particular the finals MVP award was not introduced until 1969 and VORP and BPM are not available until the  1973-1974 season. To work around this, two lists were created in which  1979 (the year the 3 point line was established and the NBA and ABA  merged) served as the bifurcation point. To determine which list each player was placed in, their career midpoint was used, with players whose  career midpoint was before 1979 being put in the Old School (OS) list  and players whose career midpoint was after 1979 put in the modern list.  The missing measurements for the OS list were evenly split among those available.
Once the data was ingested, processed, and split between the two eras(pre and post-1979) all the features were normalized between 0 and  1. After normalizing the data, a weighted average was taken, using the percentage of total votes from the survey, to compute the final GOAT  score of each player.