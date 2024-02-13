# Project_1

Data used: https://www.kaggle.com/datasets/nikhil1e9/myanimelist-anime-and-manga showing scraped user rankings from https://myanimelist.net/

**Jordan: Does Amount of Volumes in a Manga Effect Popularity?


**Rachel: Do People Like Anime Adaptations?** 

I began by merging our anime and manga data by title, which created a dataset of anime and manga that had the same title. This did not contain every adaptation in both lists, as some adaptations have different titles, but still left me with 2700+ titles to compare data on. I also dropped the columns with hyperlinks to pictures since that would not be useful for this project. 

My initial assumption was that there would be an overall trend of anime being rated worse than manga. This was based on personal experience of book adaptations generally being poorly received by the public. When I compared ratings of anime and manga adaptations by subtracting the rating of the manga from the rating of the anime, however, I found that there was enough difference of opinion to leave no clear correlations. It was when I divided by adaptation type that I began to see, notably that Specials were ranked much more highly than any other anime type–their average comparative ranking was -32, showing they actually tended to be ranked more highly than the manga. 

There were a few limitations to my approach and data set. The data set was derived from an anime and manga fan site, so the population polled was already predisposed to like anime and manga and the rankings probably couldn’t be taken as objective indicators of quality so much as personal preference. The way I combined the data sets also did not account for adaptations that had similar but not identical titles. There were also some manga which were adaptations of the anime of the same title, rather than the other way around, though they were in the minority. 
