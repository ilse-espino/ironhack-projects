# Billboard Top Weekly Songs 1999-2019 Tableau Visualization

## Overview

The goal of this project is to analyze the genres, gender and duet trends through the years, as well as visualize the songs that remained for the greater number of weeks in the top 5 Billboard Charts and a comparison between the top 10 songs on Billboard and Spotify from 2017 - July 2019.
The visualizations created can be seen on Tableau Public through the following [link]().


## Data Source and Cleaning

### Data Source

The data was obtained from [Kaggle](https://www.kaggle.com/danield2255/data-on-songs-from-billboard-19992019). The data used from this source were the following files:
* billboardHot_100_1999-2019
* artistDf
* spotifyWeeklyTop200Stream

### Data Cleaning

*Billboard Hot 100*
    1. The Genre column was equally converted to a list because it contained several genres for one song. After analyzing the data, it was assumed the the first genre listed was the top genre for each song.
    2. A new column (top_genre) was created containing the first element from the list previously made. This will be considered as the genre of the song. Various songs and their list of genres were analyzed in order to get the conlcusion that the list of genres is sorted by top genre.
    3. The Artists column was converted into a list separating artists by commas because the original file contained a string separated by a comma when more than one artist performed in the song.
    4. A new column (main_artist) was created containing the first element from the list previously made. This will be considered as the artist for analysis.
    5. Since the approach for this project will not cover the lyrics, the Lyrics column was dropped.
    
*Merge*

Billboard Hot 100 and Artists dataframes were merged in order to obtain the gender of the artist.

   1. The Billboard Hot 100 data frame was merged with the artists data frame through a left join. This is due to the fact that not all of the artists on Billboard Hot 100 were in the Artists list.
    
Note: Some of the genders for top artists were filled manually in order to complete the list, there are still some null values for some artists which could indicate two things: Gender was not found or Group was composed of both female and male artists.


## Approach

[Billboard Top Weekly Songs from 1999-2019]()

*Top Genres*

The top genres through the years were first analyzed in order to visualize the genres through time.

* This was achieved by taking the distinct songs, since a song can appear through various weeks, and choosing does who were on the top 10 (peak positions).
* It can be seen that Pop, Rap and R&B are the top genres through two decades.
* There are so many diferent types of genres.
* The top genres for this two decades are visualized through time:
    - Hip-Hop gained top popularity on 2018
    - Pop started to loose popularity, but on the top genres per year visualization, different Pop styles are introduced (Dream-Pop, Dance-Pop. From this it can be inferred that Pop still has a high presence, but in different and more specific styles.
    - A clear decrease on R&B popularity can be seen for the last 5 years, but it has still remained on the top positions for two decades.
    - Rap reached its peak on 2007 and started to decrease since then. However, it has still remained on the peak positions for two decades.
    - Pop-Rock was also one of the top genres through two decades, but Rock was decided to be analyzed instead since is a different style. Rock has been loosing popularity and has not been present on the top 10 the last three years.


*Gender*

Gender was analyzed through the ages for all the songs present each year in order to visualize the gender gap.

* A visualization was made presenting two color bar graphs and the percentage from all artists present on the Billboard Top 100.
* Null values were excluded. As stated before, this may represent missing information or a group composed of both genders.
* It can be concluded from the graph that males have a strong presence through the years, composing from 67% to 79%.
* There is an overall 70-30 male-female representation through two decades.
* The graph shows that more artists have been introduced to the top weekly, but the gender representation remains the same.

*Duets*

Duets were analyzed through the years in order to visualize if there was an increase or decrease in them.

* A new column was created with values 1, representing a duet, and 0, representing single artist or group.
* The frequency of songs with two or more artists is represented on a bar graph.
* A clear increase can bee seen through the two decades, having its peak on 2018.
* Is it possible to infer that if an artist makes a duet with another one it is more likely for them to be on the Billboard Hot 100?

*Top 5 songs per year*

* A treemap diagram was created to visualize the top songs per year.
* The songs that remained more weeks on the charts and were on the top 5 are represented.
* Some songs may be present in two years, this may be due to their release date (it could have been near the end of one year, making the song present for the end of their release year and the beginning of the next one).
* The songs may differ from Billboard Top 100 per year because they are calculated differently. The time range used for this analysis is 01-Jan to 31-Dec, while Billboard starts from December to the third week in November.
* Top Artists:
    - Ed Sheeran has been 4 times on the Top 5, having two songs on 2018.
    - Maroon 5 and Lifehouse have been 4 times on the top 5 for different years.
    - Imagine Dragons has the most popular song "Radioactive" that was in the top 5 for two years.
    - Imagine Dragons, Taylor Swift, matchobx Twenty, and Train have been 3 times in the top 5.

*Billboard vs Spotify*

detailed explanation of your approach and code for constructing visualizations and organizing them into a Story as well as your results, obstacles encountered, lessons learned, and a link to your completed Tableau workbook.

## Further Questions

* The analysis of the origin the artists come from is also interesting and can be an addition to this analysis.
    - Where do artists from Billboard's Hot 100 come from?
    - Is there any country with an increase or decrease in popularity?

* Further analysis on why Billboard's top 10 differ from Spotify's.
    - Is Spotify the biggest streaming service?
    - Which country has the most Spotify users? Does this influence Spotify's top weekly?
    

## Resources

The compelte data could not be uploaded to the repository due to its large capacity. The link for the Kaggle source and final file on Google Sheets is below.

-[Kaggle: Data on Songs from Billboard 1999-2019](https://www.kaggle.com/danield2255/data-on-songs-from-billboard-19992019#billboardHot100_1999-2019.csv)
-[Billboard Hot 100 and Artists](https://docs.google.com/spreadsheets/d/1MfknE837BIQViaMjCnRkUL3ime6BU0htCTv39x9Dbms/edit?usp=sharing)
-[Spotify]()
-[Data Cleaning]()

