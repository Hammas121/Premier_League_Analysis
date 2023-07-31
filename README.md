# Premier League 2022-23 Season Data Analysis!

This repository contains code for **Exploratory Data Analysis (EDA)** of the **Premier League 2022-23** season data. The code is written in Python and utilizes popular libraries such as pandas, numpy, matplotlib and, seaborn for data manipulation, analysis, and visualization..

## Data Source

The data used in this analysis is sourced from Kaggle and can be found at the following link:
[kaggle datasets download -d thamersekhri/premier-league-stats-2022-2023](kaggle%20datasets%20download%20-d%20thamersekhri/premier-league-stats-2022-2023)

## Data Loading

The code starts by loading the Premier League data from the **Premier_League.csv** file using pandas into a DataFrame named `df`. The dataset contains information about various matches played during the season.

## Stadiums and Maximum Attendance

The data is explored by extracting the number of stadiums and their names using the following code:

    df.groupby('Home Team')['stadium'].unique()
   
   Additionally, the code calculates the maximum attendance in any game by converting the **'attendance'** column to numeric data type, removing commas, and replacing 0s with 1s, then finding the maximum attendance.


## Possession Analysis

The code calculates the average possession for each team in both home and away matches using the following code:

    home_possession_avg = grouped_home['home_possessions'].mean()
    away_possession_avg = grouped_away['away_possessions'].mean()
   
It creates a DataFrame named **`possession_avg_combined`** to store the results and visualizes the average possession using a bar chart.

## Goals Analysis

The code calculates the total home and away goals scored by each team and creates a DataFrame named `aggregated_df` to store the results. It then plots a bar chart to visualize the total goals scored for each team (both as home and away).

## Home/Away Results

The code analyzes the match results for each team, including home wins, away wins, home losses, away losses, home draws, and away draws. It creates stacked bar charts to visualize the results for each team as both home and away matches.

## Goal Difference

The code calculates the goal difference (GD) for each team, which is the difference between goals scored and goals conceded. It then visualizes the goal difference using a horizontal bar chart.

## Points Calculation

Based on the match results, the code calculates points for each team (3 points for a win, 1 point for a draw, and 0 points for a loss). It generates a points table and sorts the teams based on points to determine the team rankings. The points table is visualized using a horizontal bar chart.

## Goal Conversion Rate

The code calculates the goal conversion rate for each team, which is the percentage of shots that resulted in goals for both home and away matches. It then combines the conversion rates and formats the results as percentages. The goal conversion rates are displayed for each team.

## Conclusion

This code provides valuable insights into various aspects of the Premier League 2022-23 season, such as team performance, possession, goals, and points. The visualizations aid in better understanding the data and drawing meaningful conclusions about the teams' performances throughout the season.

Please ensure that the 'Premier_League.csv' file is present in the working directory and all required libraries are installed before running the code.

Feel free to explore the code further and modify it to perform more in-depth analysis or add additional visualizations as needed. Enjoy your data analysis journey!

## Credits

The dataset used in this analysis is provided by Kaggle user [Thamer Sekhri](https://www.kaggle.com/thamersekhri). Special thanks to the Kaggle community for sharing valuable datasets and enabling data analysis projects like this one.
