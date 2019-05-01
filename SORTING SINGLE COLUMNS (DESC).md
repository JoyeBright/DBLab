Get the IMDB score and film ID for every film from the reviews table, sorted from highest to lowest score.

Select imdb_score, film_id from reviews
order by imdb_score DESC

Get the title and duration for every film, in order of longest duration to shortest.

Select title, duration from films
order by duration DESC