# Defensive-Overview-of-Premier-League-21-22
## A comparison of some of the best defensive performances in the Premier League last season, as well as general analysis

![PL 21_22 Defenders (1)](https://user-images.githubusercontent.com/23167040/183028786-fea28e3f-e197-4259-bcf2-2679ecf7bda9.png)


With a brand new Premier League season almost upon us, it's only fitting that we take a look back at last season's defensive performances and summarize them. I always try to see if I can find "unlikely heroes" in my analysis, which means that I want to bring players who have performed exceptionally well for their respective teams but seem to go under the radar because they don't get as much media exposure as some of the game's superstars and high-earners.

This visualization exhibits the best individuals from last season in terms of three important defensive metrics: shots blocked, interceptions, and clearances. I was surprised to see a couple of non-defenders stand out in these metrics as well, which is credit to their defensive work ethic despite not being traditional defenders.

## Data

The data was acquired from fbref.com, you can check it out here: https://fbref.com/en/comps/9/11160/defense/2021-2022-Premier-League-Stats

## Preprocessing and cleaning on Python

Upon ingesting the csv data via Python, I performed three main preprocessing steps:
* Removed a set of columns from the data that were irrelevant for my analysis, including Rk (a kind of index), Position, Age, Born (date of birth), and Matches (number of matches played)
* Checked for null values, and found them in the columns of Tackle% and SuccessfulPress%, decided to drop records with null values
* Checked for duplicated rows - found none
* The Nation column had repetitive values for the nation name, in lowercase and in uppercase, so I processed the column to make it only store a single instance of upper case nation codes for each player
* Finally, renamed the columns to make them more understandable beyond just acronyms that only a football geek would understand!
* Saved the resulatant dataset as a csv for further analysis and visualization in Tableau

## Insights from the visualizations

* The first visualization is a plot of the top 15 defenders in the Premier League last season in terms of number of shots blocked per game and number of interceptions made per game. Some stand-out performers in this regard have been Newcastle's Dan Burn, and Arsenal's Calum Chambers. Special shout-out goes to Brighton's Jeremy Sarmiento, who despite being an attacking winger, has averaged an impressive 2 interceptions and blocks per 90, which suggests excellent defensive work ethic

* Secondly, I look at defenders who have committed the most errors that have resulted in opponent's shot on goal. Again, Calum Chambers leads the pack, despite having put in good performances in other key defensive areas for his team. He is followed by the likes of Newcastle's Paul Dummett and West Ham's Ryan Fredericks

* Finally, we look at the most number of clearances made per 90 by individuals. We see a famililar face - Dan Burn - at the top leading with close to 12 clearances per match, followed by yet another familiar face - Calum Chambers - with a little over 10 clearances averaged per match.

* Big takeaway: Newcastle struck gold by investing in Dan Burn, he's been pretty much everywhere in terms of defensive metrics, with an impressive number of blocks, interceptions, and clearances per game that have no doubt helped his team. In fact, he has clearly been pivotal in the team's blistering success during the second half of the season, in which only Liverpool and Manchester City amassed more points than Newcastle
