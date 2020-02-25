# Predicting Play Type and Play Yards in NFL Games
The project used game-level, play-level and player-level NFL data to conduct exploratory analysis, built machine learning models to predict play type (rush/pass) and rush yards, and built a recommendation system for defensive play.

## Contribution
This is the group project for IEOR_E4523 Data Analytics at Columbia University. It's jointly developed by Max Wong, Clover Liu, Y. Sun, and Jerome Gu. Jerome Gu is responsible for the overall planning and predicting play types.

## Technologies
The project is created with:
* Python version: 3.7
* Python TKinter GUI version: 8.5

## Introduction
This project aims at predicting NFL offensive plays using data from a variety of different sources. To enhance the feasibility of team defensive strategies based on prediction outcomes, we divided the main objective into two parts: 
- predicting offensive play types (rush/pass)
- predicting yards of rushing plays

## Data Collection
We collected the following five sources of data. The first two datasets are the base datasets for predicting type and rush yards. The last two ones are for computing extra features for the first two datasets.
* Play-by-play type data from 2016 to 2019 from [nflsavant](nflsavant.com)
* Rush play data from [Kaggle.](https://www.kaggle.com/c/nfl-big-data-bowl-2020/data)
* NFL [game-level](https://www.pro-football-reference.com/) data from 2016 to 2019 by web scraping
* Team [statistics ranking data](https://www.pro-football-reference.com/) from 2016 to 2019
  
## Data Analysis
We did exploratory analysis to better understand the game process and our data.
- Play type analysis:
  - A game process for example
  - Yards distribution analysis 
  - Formation & Play Type analysis 
  - Formation & Yards analysis 
  - Down & Yards & Play Type analysis
  - Down & Formation analysis 
  - Trend of play type in different seasons
  - Comparison of play type of different teams
  - Yards to go & Yards analysis
- Rush yards analysis:
  - Distribution analysis
  - Play-by-play analysis 
  - Athlete analysis 
  - Team ranking

## Modeling and Results
- We find GBM is the most accurate in terms of both training accuracy and test accuracy (73.17% is also close to the highest accuracy in related literature, which is around 75%).
![Type prediction result](https://github.com/tracyzg1818/NFL-Predicting-Play-Types-and-Play-Yards/blob/master/Predicting%20Play%20Types/Accuracy%20Summary%20for%20Predicting%20Play%20Types.png?raw=true)


- XGBoost Model is the best model with the smallest RSME of 2.763, thus it would be our backend algorithm for our recommendation system.
![Yards prediction result](https://github.com/tracyzg1818/NFL-Predicting-Play-Types-and-Play-Yards/blob/master/Predicting%20Rush%20Yards/Accuracy%20Summary%20for%20Predicting%20Rush%20Yards.png?raw=true)

## Defensive Play Recommendation system
At last, we created a recommendation system program to help defensive teams minimize the yardage gain by the offensive teams with <b>Python Tkinter GUI</b>. Here is the basic idea: 
- After the program receives all the inputs from the user, it would call the XGBoost model to iterate all possible combinations of DefendersInTheBox and DefensePersonnel. 
- Then, the program would sort the results with ascending order and show the Top 5 combinations the defensive team could adopt to minimize the yardage gained by the opponent. Here's a sample output:
![Yards prediction result](https://github.com/tracyzg1818/NFL-Predicting-Play-Types-and-Play-Yards/blob/master/Predicting%20Rush%20Yards/Defensive%20Play%20Recommendation%20System.png?raw=true)

## Reference
- Fernandes, C., Yakubov, R., Li, Y., Prasad, A., and Chan, T., Predicting plays in the National Football League 
- Lee, P., Chen, R., & Lakshman, V. Predicting Offensive Play Types in the National Football League.

