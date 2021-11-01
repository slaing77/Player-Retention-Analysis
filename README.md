# Gamedata Project

As gamedata’s one year anniversary approaches, our group comprising Kai Lurker and Sareenah Laing have been tasked with investigating Player Retention.

First, we explored the contents of the dataset provided and can see when players first joined, what their most recent match has been against who and the result.  We can also see purchases made by players of the game.

We loaded our data set into Big Query where we were able to come to a retention rate fairly easily. 

Our team split up our questions for further exploration and we’ve agreed a particular  interest of ours is learning how winning streaks vs losing streaks impact retention, if at all? 

## We discovered the following:
1. 30 Day Rolling Retention rate
2. Avg Age of retained players
3. Regions with the most retention 
4. Regions with the least retention
5. System Preference differences 
6. Opportunities to grow retention among regional and system preference differences.

## We then loaded the results of our queries into Google Sheets.

1. Rolling retention
2. Player info

From there we transformed our data and created visualizations to share in our presentation.

## My transformations:
1. Created a new column to calculate the price per item of each distinct player_id purchase.
2. Created a new column using an IF statement to identify wins as 1, losses as 0 to determine overall wins vs overall losses for the 30 day period.
3. Created a new column with a SUMIF statement to determine purchases per wins and purchases per losses 
4. Created 2 new columns to tally overall total_purchases_by_retained vs total_purchases_other (not retained).

## Pivot Tables:
I created 4 pivot tables to further explore and compare
1. pivot_rolling_retention
2. pivot_spending_habits_of_retained_players
3. pivot_total_players_retained_by_region
4. pivot_regional_comparisons

## My Visualizations:
1. 30 Day Rolling Retention by join day
2. Avg. Age of retained players by region
3. Purchases by retained players by region
4. Winning Player Purchases by region
5. The three user groups by system preference
6. Purchases to Wins
7. Purchases to Losses

## Discovered Patterns:
When breaking down purchasing patterns by players as grouped by their system preference, we notice with the exception of MacOS users, players who lose tend to buy more items and make more purchases overall						
								
## 3 Key Observations:					
1. Regionally, there is a  small positive correlation between winning and being retained.					
2. We know that the more members of a group retained, the more the group will purchase,
and,
3. we have identified the two major groups with least engagement:  
North Americans and Mac users.	


## 3 Suggestions to increase player retention and to grow under performing player groups:						
1. Find solutions to retain more Mac users and North Americans. In order to create more interest among these two groups, drop some ads targeting Mac user forums or popular North American digital hang outs.						
2. Reward Linux users for their engagement with coupons to spend in the store as they do have the highest price per item across all groups
3. Explore the opportunity to invite  players to participate in a quick survey (no more than three questions) in exchange for extra coins or free items at mid month and again at end of month to counter the historic dip in engagement on those days of the month.		

### Deliverables:
1. This README
2. rolling_retention_query.md
3. player_info.md
4. 30_day_rolling_retention.md
5. purchases_to_losses.png 
6. purchases_to_wins.png 
7.Find a copy of my google sheets here:
https://docs.google.com/spreadsheets/d/1N0DI3EL85mpTXdJVFiqlGKbHarBtINIuyOFe2v9nTHU/edit?usp=sharing
							




