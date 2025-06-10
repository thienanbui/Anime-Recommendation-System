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

#### Feature Engineering
- Profiles with no favorited shows were removed.
- A new dataset using dummy variables for each user profile was created and used when building the recommendation system.

## Methodology
We calculated the cosine similarity between the target user and all other users in the dataset, considering their anime-watching history based on their favorited animes. This similarity score quantified the likeness between users based on their anime preferences, and allowed us to identify users that were most similar to each other. Recommendation scores were calculated for each user-anime pair.

##### Note: Animes already watched by the target user are excluded from the recommendation list to ensure that we are not recommending shows that the user has already seen.

## Results
Overall, our model does well in providing similar recommendations to the user based on what they have favorited. It detects key thematic elements present in the target user's favorited shows and applies them to the recommendations provided, striking a balance between greatly similar shows in the same genre while including nuanced shows in adjacent categories that similar users had enjoyed.

## Broader Applications
This work focused on anime users and shows. The foundations for this recommendation system can be extended to any consumer service seeking to enhance the quality of their consumer's experience and retention rate, from streaming services to online grocery shopping.

## Future Work
We can extend the capabilities of our recommender model to determine what animes we should consider adding to our offering, based on our viewer demographic and preferential distributions. The model can be further improved by layering demographical information (such as age or gender) onto user profiles. This adds additional dimensions in which profiles can be compared to each other and lead to better recommendations. Weights should be assigned when using user-user collaborative filtering. This is largely because certain subsets (e.g. male vs. female users) tend to watch different genres – the recommender should not deviate too far from the user’s preferences.


