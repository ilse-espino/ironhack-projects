# Billboard Top Weekly Songs 1999-2019 Tableau Visualization

## Overview

The goal of this project is to analyze the genres, gender and duet trends through the years, as well as visualize the songs that remained for the greater number of weeks in the top 5 Billboard Charts and a comparison between the top 10 songs on Billboard and Spotify from 2017 - July 2019.


## Data Source and Cleaning

### Data Source

The data was obtained from [Kaggle](https://www.kaggle.com/danield2255/data-on-songs-from-billboard-19992019). The data used from this source were the following files:
* billboardHot_100_1999-2019
* artistDf
* spotifyWeeklyTop200Stream

### Data Cleaning

*Billboard Hot 100*
    1. The Genre column was equally converted to a list because it contained several genres for one song. After analyzing the data, it was assumed the the first genre listed was the top genre for each song.
    2. A new column (top_genre) was created containing the first element from the list previously made. This will be considered as the genre of the song.
    3. The Artists column was converted into a list separating artists by commas because the original file contained a string separated by a comma when more than one artist performed in the song.
    4. A new column (main_artist) was created containing the first element from the list previously made. This will be considered as the artist for analysis.
    5. Since the approach for this project will not cover the lyrics, the Lyrics column was dropped.
    
*Merge*
    1. 


## Approach

detailed explanation of your approach and code for constructing visualizations and organizing them into a Story as well as your results, obstacles encountered, lessons learned, and a link to your completed Tableau workbook.



## Resources


