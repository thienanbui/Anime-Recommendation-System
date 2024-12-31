# Anime Recommendation System

#### Designed, implemented, and tested by [Thien-An Bui](https://www.linkedin.com/in/thien-an-bui/)


## Overview
This project aims to create a seamless and improved user experience by enhancing the quality of recommendations provided to the consumer, thus increasing their engagement with the service and promoting customer retention rates. 
While able to be applied to other genres and broader applications of media recommendation usages, the data used focuses on consumers who watch anime, a style of Japanese film and television animation gaining increased popularity in the USA.

For a detailed presentation of methodology and results, see [here](/Presentation/Anime_Recommender_PPT.pptx).

## Background
Streaming platforms have become increasingly competitive and commonplace in today’s entertainment industry. 
Companies like Netflix and Crunchyroll both provide anime selections for users to stream and have sought ways to differentiate themselves to retain and grow their customer basis.

Many users on these platforms have diverse preferences, and the vast catalog of animes available can be overwhelming. 
Users often struggle to discover animes aligned with their tastes and interests, leading to suboptimal engagement and potential dissatisfaction. 

#### Assumptions and Hypotheses Made
- People only add animes to their "Favorites" list when they enjoyed the show.
- All user profiles have at least one favorited anime. 
- A combination of user-item collaborative filtering will be more effective than using item-item or user-user filtering alone.

## Data Overview
Our primary data source contains user profiles and the animes they have added to their "Favorites" list. 

See below for visualizations used to draw initial insights about our user profile population.
![Exploratory Data Analysis Visuals](/Snapshots/EDA.PNG "")
- The vast majority of user profiles are young adults between the age of 20-40 and are predominantly male.
- Profiles typically have 5 favorited animes, on average.
- There are a wide range of anime genres available in the dataset, with comedy and shounen (young male) leading the charts.

