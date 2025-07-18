# NFL Quarterback Analysis (1999–2025)

## Part One: QB Playstyle Clustering

This analysis explores quarterback playstyles using merged weekly passing and rushing statistics from 1999 to 2025.

- **Data Preparation:**  
  Passing, rushing, and weekly relevant stats are merged by player and season to create a comprehensive dataset.

- **Feature Engineering:**  
  Various per-game and per-attempt metrics are calculated, such as sacks per dropback, rushing touchdowns per game, passing air yards per attempt, completion percentage, and more.

- **Dimensionality Reduction with PCA:**  
  Principal Component Analysis (PCA) reduces the dataset to **9 components**, capturing **94.08%** of the total variance. This simplifies the data while retaining most of the important information.

- **Clustering with K-Means:**  
  Using the elbow method, **5 clusters** were selected to group quarterbacks by playstyle similarity.

- **Output:**  
  - Static image:  
    (![Quarterback Play Style](images/qb_play_style.png))
    
  - Interactive scatter plot:  
    [QB Playstyle Interactive Chart](https://jevanc.github.io/nfl-stats/qb_play_style.html)  


---

## Part Two: QB Tier List Ranking

This section ranks quarterbacks using a tier list based on a combination of efficiency and production metrics.

- **Data Preparation:**  
  Similar merging of weekly, passing, and rushing stats, combined with QB names for labeling.

- **Key Metrics Included:**  
  - Touchdowns per game (passing + rushing)  
  - Yards per game (passing + rushing)  
  - Passing yards per attempt  
  - Rushing yards per run  
  - Turnovers per game (interceptions, sack fumbles, rushing fumbles)  
  - TD-to-turnover ratio  
  - Completion percentage  
  - Passing EPA per game  
  - Rushing EPA per game

- **Dimensionality Reduction with PCA:**  
  Reduced to **1 component** to create a composite score summarizing overall QB performance.

- **Composite PCA Formula:**  
  The tier score is computed as:

(0.41 × tds_per_game) + (0.38 × yards_per_game) + (0.39 × passing_yards_per_attempt) +
(0.06 × rushing_yards_per_run) - (0.23 × turnovers_per_game) + (0.40 × td:turnover) +
(0.35 × completion_pct) + (0.42 × passing_epa_per_game) + (0.10 × rushing_epa_per_game)

## Top 10 QB Seasons of All Time

| Name & Year          | Score    |
|----------------------|----------|
| Aaron Rodgers 2020   | 6.966    |
| Aaron Rodgers 2011   | 6.872    |
| Drew Brees 2011      | 6.168    |
| Matt Ryan 2016       | 5.967    |
| Peyton Manning 2004  | 5.571    |
| Tom Brady 2007       | 5.512    |
| Patrick Mahomes 2018 | 5.282    |
| Drew Brees 2019      | 5.215    |
| Lamar Jackson 2024   | 5.187    |
| Aaron Rodgers 2021   | 5.137    |

---

## Worst 10 QB Seasons of All Time (AR)

| Name & Year          | Score     |
|----------------------|-----------|
| Akili Smith 2000     | -5.930    |
| JaMarcus Russell 2009| -5.724    |
| Jimmy Clausen 2010   | -5.555    |
| Andrew Walter 2006   | -5.327    |
| Donovan McNabb 1999  | -5.180    |
| Kyle Orton 2005      | -5.053    |
| Mark Brunell 2004    | -4.964    |
| Ryan Leaf 2000       | -4.719    |
| David Carr 2002      | -4.542    |
| Doug Pederson 1999   | -4.537    |



- **Output:**  
- Static image:  
  ![Tier List](images/tier_list.png)

- Interactive tier list chart:  
  [QB Tier List Interactive Chart](https://jevanc.github.io/nfl-stats/tier_list.html)  

---

## Summary

This repository provides a detailed and comprehensive analysis of NFL quarterback performance and playstyle clustering from 1999 to 2025, utilizing advanced statistical techniques such as PCA and K-Means clustering to visualize and rank quarterbacks effectively.

---
