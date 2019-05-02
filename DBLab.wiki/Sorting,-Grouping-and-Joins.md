## ORDER BY

Get the names of people from the `people` table, sorted alphabetically:
```sql
select name
from people
order by name;
```

Get the names of people, sorted by birth date:
```sql
select name
from people
order by birthdate;
```

Get the birth date and name for every person, in order of when they were born:
```sql
select birthdate, name
from people
order by birthdate;
```
## Sorting single columns

Get the title of films released in 2000 or 2012, in the order they were released:
```sql
select title
from films
where release_year = 2000 or release_year = 2012
order by release_year;
```

Get all details for all films except those released in 2015 and order them by duration:
```sql
select *
from films
where release_year != 2015
order by duration;
```

Get the title and gross earnings for movies which begin with the letter 'M' and order the results alphabetically:
```sql
select title, gross
from films
where title like 'M%'
order by title;
```
## Sorting single columns (DESC)

Get the IMDB score and film ID for every film from the reviews table, sorted from highest to lowest score:
```sql
select imdb_score, film_id
from reviews
order by imdb_score desc;
```

Get the title and duration for every film, in order of longest duration to shortest:
```sql
select title, duration
from films
order by duration desc;
```
## Sorting multiple columns

Get the birth date and name of people in the `people` table, in order of when they were born and alphabetically by name:
```sql
select birthdate, name
from people
order by birthdate, name;
```

Get certifications, release years, and titles of films ordered by certification (alphabetically) and release year:
```sql
select certification, release_year, title
from films
order by certification, release_year;
```
## GROUP BY

Get the release year and count of films released in each year:
```sql
select release_year, count(*)
from films
group by release_year;
```

Get the release year and average duration of all films, grouped by release year:
```sql
select release_year, avg(duration)
from films
group by release_year;
```

Get the release year and largest budget for all films, grouped by release year:
```sql
select release_year, max(budget)
from films
group by release_year;
```

Get the language and total gross amount films in each language made:
```sql
select language, sum(gross)
from films
group by language;
```

Get the release year, country, and highest budget spent making a film for each year, for each country. Sort your results by release year and country:
```sql
select release_year, country, max(budget)
from films
group by release_year, country
order by release_year, country;
```
## HAVING

In how many different years were more than 200 movies released? (Having):
```sql
select release_year, count(*)
from films
group by release_year
having count(*) > 200;
```

Get the country, average budget, and average gross take of countries that have made more than 10 films. Order the result by country name, and limit the number of results displayed to 5. You should alias the averages as `avg_budget` and `avg_gross` respectively:
```sql
select country, avg(budget) as avg_budget, avg(gross) as avg_gross
from films
group by country
having count(*) > 10
order by country
limit 5;
```
