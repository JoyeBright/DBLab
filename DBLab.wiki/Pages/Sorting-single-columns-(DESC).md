`Question` Get the IMDB score and film ID for every film from the reviews table, sorted from highest to lowest score.
``` sql
Select imdb_score, film_id
From reviews
Order By imdb_score DESC
```

***

`Question` Get the title and duration for every film, in order of longest duration to shortest.
``` sql
Select title, duration
From films
Order By duration DESC
```