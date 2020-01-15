# Movies-Recommender-System

### The goal of this project is to build a simple and a content based movie recommendation system that suggests movies to the user based on his/her preferences.
    
## Simple recommender
The Simple Recommender offers generalized recommnendations to every user based on movie popularity and (sometimes) genre. The basic idea behind this recommender is that movies that are more popular and more critically acclaimed will have a higher probability of being liked by the average audience. This model does not give personalized recommendations based on the user.
The implementation of this model is extremely trivial. All we have to do is sort our movies based on ratings and popularity and display the top movies of our list. 

## Techinque:

I used the IMDB Ratings to come up with our Top Movies Chart. I will use IMDB's weighted rating formula to construct my chart. Mathematically, it is represented as follows:

Weighted Rating (WR) =  (vv+m.R)+(mv+m.C) 
where,

1. v is the number of votes for the movie
2. m is the minimum votes required to be listed in the chart
3. R is the average rating of the movie
4. C is the mean vote across the whole report

## Content based recommender
I build an engine that computes similarity between movies based on certain metrics and suggests movies that are most similar to a particular movie that a user liked. Since we will be using movie metadata (or content) to build this engine, this also known as Content Based Filtering.
I have built Content Based Recommenders based on:

1. Movie Overviews and Taglines
2. Movie Cast, Crew, Keywords and Genre

### Variables:
1. Overview
2. Description
3. Actors
4. Genre
5. Director

### Technique:
Cosine Similarity to calculate a numeric quantity that denotes the similarity between two movies. Mathematically, it is defined as follows:
cosine(x,y)=x.y⊺||x||.||y||

TF-IDF Vectorizer and Count Vectorizer to  calculate the Dot and get the Cosine Similarity Score.

