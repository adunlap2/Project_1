# Project_1
Manga and Anime Analysis

Manga and Anime have taken huge popularity not only in Japan, but globally. In the United States, the value of the Anime industry is currently sitting above $4 billion. With the growth of mass appeal to anime and manga, it's clear that these art forms have taken a strong hold in American media. 
In this data exploation and visualization project, we will delve into a data set of over 13,000 different anime's and manga's respectively, to explore various questions. 

Data used: https://www.kaggle.com/datasets/nikhil1e9/myanimelist-anime-and-manga showing scraped user rankings from https://myanimelist.net/

Data columns: 
- Title: title of anime/manga
- Rank: Ranking of anime/manga
- Type: Category of anime/manga
- Episodes (anime)
- Volumes (manga)
- Aired(anime)
- Published (manga)
- Members: Number of members who have watched/read the anime/manga
- page_url: the url link to the page of the particular anime/manga
- image_url: The URL link to the cover image of the particular anime/manga
- Score: average user rating/score of the anime/manga

Questions to be explored:

- Does the amount of voluems in a Manga series effect the popularity of the manga?
- Do people enjoy anime adaptations?
- Do people enjoy shows that are currently airing or shows that have been completed?

**Jordan: Does Amount of Volumes in a Manga Effect Popularity?
To begin my data explorations, I started by cleaning up the data and getting rid of columns that I did think were going to provide much use to me. This included the page_url and the image_url column. After that I just began looking through the column and the data to delve into a question. Something that I began to wonder about was the score of a particular manga and how it related to the amount of volumes in the manga (if any).  I began the data exploration into this question by looking at the average score of each kind of manga, the type of manga being Doujinshi, Light-Novel, Manga, Manhua, Manhwa, Novel, and One-shot. I then mapped the average scores of each kind of manga, and then plotted the average scores of the Light-Novel, Novel, and Manga. The Novel category had the highest average score above all the types of Manga, however, the Novel category has the least amount of titles which I did not think was a big enough sample size to delve into an analysis. The category of Manga has far more titles and therefore a larger dataset. And, manga is a more well known category of Manga to begin with. 

I then wanted to explore the top 20 titles of manga based on their score, this is where I wanted to explore whether the amount of volumes of the Manga played a role in the overall score of the series. After I created the bar chart I found that within the top 20 titles of the Mangas, there where some manga that had an unknown amount of volumes in the series. I cut out those rows as there was no integer value to run any analysis one.

I then created a bar graph and a pie chart based off of the amount of volumes each title of manga had, to visually have an idea of the relationship between the titles and the scores. I hypothesized that there may be a weak positive relationship to amount of volumes in a series to the score of the manga. With my limited understanding of Manga culture, I assumed that the more the merrier. The more volumes in a series, the better to manga-loving people. 

When comparing the two graphs to each other, there wasn’t a lot I could gather just visually from the graphs. I noticed that there seemed to be a positive relationship with the amount of volumes to the score of the series, but just based off of the visuals alone, I could not get a good idea if there was actually a relationship. 

I ran a linear regression on the top titles and found that the p-value was 0.18 and the r-squared was 0.19. Both of these values are not looking very good for a positive relationship. The p-value shows that there is no significant relationship between the scores and volumes, and the r-value shows a very weak positive linear relationship between score and volume size. 

This shows that although I could visually see a slight relationship from volumes to scores, that there in fact is no relationship to be seen. 

Room for error: This was only comparing the top titles of Manga with the highest scores, when considering the entire population of data that is available, there is a possibility that a relationship can arise. Additionally, the score are a subjective unit of measurement. The score that this data is based on is taken from a anime and manga fan page, for lack-of a better explanation. This in turn means that these are people that love manga and anime, and may not be experts in a literary field. These scores are based of a subjective and biased population. 


**Rachel: Do People Like Anime Adaptations?** 

I began by merging our anime and manga data by title, which created a dataset of anime and manga that had the same title. This did not contain every adaptation in both lists, as some adaptations have different titles, but still left me with 2700+ titles to compare data on. I also dropped the columns with hyperlinks to pictures since that would not be useful for this project. 

My initial assumption was that there would be an overall trend of anime being rated worse than manga. This was based on personal experience of book adaptations generally being poorly received by the public. When I compared ratings of anime and manga adaptations by subtracting the rating of the manga from the rating of the anime, however, I found that there was enough difference of opinion to leave no clear correlations. It was when I divided by adaptation type that I began to see, notably that Specials were ranked much more highly than any other anime type–their average comparative ranking was -32, showing they actually tended to be ranked more highly than the manga. 

There were a few limitations to my approach and data set. The data set was derived from an anime and manga fan site, so the population polled was already predisposed to like anime and manga and the rankings probably couldn’t be taken as objective indicators of quality so much as personal preference. The way I combined the data sets also did not account for adaptations that had similar but not identical titles. There were also some manga which were adaptations of the anime of the same title, rather than the other way around, though they were in the minority.

**Ariana: Do people are for anime shows that have been around longer?
Data Exploration:
The data set only focuses on Anime’s that have a Manga adaptation. This being a very concentrated genre of Anime eliminates any anime’s that have been out for longer period but does not have a Manga. Our focus for doing this was to be able to merge the two data sets into one section. 
For my Data Graph’s, I narrowed down my data set to looking at the topmost popular 20 Anime’s. 	By doing this I am looking at a smaller data set which could skew the results looking at an even smaller pool. 	My goal for doing this is to focus on the topmost popular and be able to nicely display the data. 
Going through the ‘Aired Date’ data I found that there were bunch of dates that were not complete, indicating that those shows were ongoing. I then created a column that shows status of whether the show is still ongoing or has been completed. My goal was to be able to organize which anime’s were still ongoing. The Formulas I found to be also sorted and add these columns came from Anime & Manga: EDA + insights dataset. 
I had some trouble converting the date from an object to integer, so I had to look at the date data in more of side by side to other data, rather than doing direct comparison. In the future, looking into CSV files where the pandas can read and nicely delaminate the dates.
I then narrowed the columns the to focus on the categories that most effect my data. The columns of my data being: Title, Adaptation Type, Aired Date, Anime Votes.
First Graph:
I compared the Aired Date vs the Aired Status. From this graph, I wanted to display side by side a visual the compares the number votes to the air dates and air status. I found that most people favored anime’s that have already been completed, and  the most voted anime’s were anime’s that started 2014-2016. From this I concluded more people enjoy anime’s that have already been completed, and a majority of people voted positively towards anime’s in the middle.
Second Graph
I used another bar graph to directly compare the member votes to the Titles. I then labeled the dates to give an idea of when these anime’s came out. I found that Shingeki no Kyojin, Death Note, and Boku no Hero Academia were the top 3 most popular anime’s. Additionally, based on the dates each of the anime’s came out I didn’t not have a strong enough correlation from the start date and popularity
Third Graph 
Based on the two first graphs, I wanted to look popularity adaptations.	I found that the TV adaptations we more favorable by 78%. I was surprised to see that OVA’s were 4% more popular that Movies. I thought that movies would be more liked. 

