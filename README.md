# The Search for the Golden Age of Video Games

![video_game](https://github.com/user-attachments/assets/f66a16b8-3084-4ed2-88ce-76c0581038b1)


## An Analysis of Sales and Scores

The global gaming market is a multi-billion dollar industry, and with so much at stake, publishers are always striving to create the next big hit. This raises a question for gamers and industry analysts alike: Are games getting better, or has the golden age of video games already passed?

This project dives into sales data, critic scores, and user ratings for 400 of the top video games released since 1977. By joining, filtering, and analyzing this data, we aim to identify the release years that were most beloved by both players and critics to determine if a "golden age" can be found.

## The Datasets

The analysis is conducted on a database containing four key tables, each providing a different view of the video game landscape.

### `game_sales` table

| Column | Definition | Data Type |
| --- | --- | --- |
|name|Name of the video game|`varchar`|
|platform|Gaming platform|`varchar`|
|publisher|Game publisher|`varchar`|
|developer|Game developer|`varchar`|
|games\_sold|Number of copies sold (millions)|`float`|
|year|Release year|`int`|

### `reviews` table

| Column | Definition | Data Type |
| --- | --- | --- |
|name|Name of the video game|`varchar`|
|critic\_score|Critic score according to Metacritic|`float`|
|user\_score|User score according to Metacritic|`float`|

### `users_avg_year_rating` table

| Column | Definition | Data Type |
| --- | --- | --- |
|year| Release year of the games reviewed |`int`|
|num\_games| Number of games released that year |`int`|
|avg\_user\_score| Average score of all the games ratings for the year |`float`|

### `critics_avg_year_rating` table

| Column | Definition | Data Type |
| --- | --- | --- |
|year| Release year of the games reviewed |`int`|
|num\_games| Number of games released that year |`int`|
|avg\_critic\_score| Average score of all the games ratings for the year |`float`|

## Analysis and Findings

### 1\. The Top 10 Best-Selling Games

The initial analysis attempted to identify the top 10 best-selling video games of all time by querying the `game_sales` table. However, the query resulted in a `SyntaxError` and failed to execute. Therefore, the list of best-selling games could not be generated from this notebook.

### 2\. The Top-Rated Years According to Critics

To find out which years produced the most critically acclaimed games, we calculated the average critic score for each year.

The analysis revealed that **1998 was the top year for critics**, with an outstanding average score of **9.32**. The rest of the top five includes 2004 (9.03), 2002 (8.99), 1999 (8.93), and 2001 (8.82), suggesting a peak period for critical acclaim around the turn of the millennium.

### 3\. Identifying the "Golden Years"

A "golden age" would be marked by exceptional games loved by everyone. We searched for these "golden years" by identifying years where **either the average critic score OR the average user score was higher than 9.0**.

This query identified six standout years: **1997, 1998, 2004, 2008, 2009, and 2010**. Interestingly, the analysis also calculated the difference between critic and user scores, showing how perceptions could vary. For example, in 1997, users rated games significantly higher than critics (9.50 vs. 7.93), while in 2004, critics rated games higher (9.03 vs 8.55).

## Conclusion

While an error prevented the analysis of the all-time best-selling games, the investigation into critic and user scores provided clear insights. The data strongly suggests that a "golden age" of video games did occur, centered around the late 1990s and again in the late 2000s.

With its top ranking from critics and high marks from users, **1998 stands out as a peak year in video game history**. Based on this analysis of review scores, the golden age appears to be a period in the past, defined by widespread critical and commercial acclaim.

### Tools

- **SQL**
