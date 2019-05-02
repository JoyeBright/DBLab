## Quest: Select the title column from the films table.
category: selecting single column</br>
query: select title from films

## Quest: Select the release_year column from the films table.
category: selecting single column</br>
query: select release_year from films

## Quest: Select the name of each person in the people table.
category: selecting single column</br>
query: select name from people

## Quest: Get the title of every film from the films table.
category: selecting single column</br>
query: select title from films

## Quest: Get the title and release year for every film.
category: selecting multiple columns</br>
query: select title, release_year from films

## Quest: Get the title, release year and country for every film.
category: selecting multiple columns</br>
query: select title, release_year, country from films

## Quest: Get all columns from the films table.
category: selecting multiple columns</br>
query: select * from films

## Quest: Get all the unique countries represented in the films table.
category: select distinct</br>
query: select distinct country from films

## Quest: Get all the different film certifications from the films table.
category: select distinct</br>
query: select distinct certification from films

## Quest: Get the different types of film roles from the roles table.
category: select distinct</br>
query: select distinct role from roles

## Quest: Count the number of rows in the people table.
category: learning to count</br>
query: select count(*) from people

## Quest: Count the number of (non-missing) birth dates in the people table.
category: null and is null, count</br>
query: select count(birthdate) from people where birthdate is not null

## Quest: Count the number of unique birth dates in the people table.
category: count, distinct</br>
query: select count(distinct birthdate) from people

## Quest: Count the number of unique countries in the films table.
category: count, distinct</br>
query: select count(distinct country) from films

## Quest: Get all details for all films released in 2016.
category: selecting multiple columns, filtering results</br>
query: select * from films where release_year = 2016

## Quest: Get the number of films released before 2000.
category: count, filtering results</br>
query: select count(*) from films where release_year < 2000

## Quest: Get the title and release year of films released after 2000.
category: filtering results, selecting multiple columns</br>
query: select title, release_year from films where release_year > 2000

## Quest: Get all details for all French language films.
category: select multiple columns, filtering results</br>
query: select * from films where language = 'French'

## Quest: Get the name and birth date of the person born on November 11th, 1974. Remember to use ISO date format ('1974-11-11')!
category: selecting multiple columns, filtering resuls</br>
query: select name, birthdate from people where birthdate = '1974-11-11'

## Quest: Get the number of Hindi language films.
category: count, filtering results</br>
query: select count(*) from films where language = 'Hindi'

## Quest: Get all details for all films with an R certification.
category: selecting multiple columns, filtering results</br>
query: select * from films where certification = 'R'

## Quest: Get the title and release year for all Spanish language films released before 2000.
category: filtering results, where AND, selecting multiple columns</br>
query: select title, release_year from films where language = 'Spanish' and release_year < 2000

## Quest: Get all details for Spanish language films released after 2000.
category: filtering results, where AND, selecting multiple columns</br>
query: select * from films where language = 'Spanish' and release_year > 2000

## Quest: Get the title and release year for films released in the 90s.
category: selecting multple columns, filtering results, BETWEEN</br>
query: select title, release_year from films where release_year between 1990 and 1999

## Quest: Get the title and release year of all films released between 1990 and 2000 (inclusive).
category: selecting multiple columns, filtering results, BETWEEN</br>
query: select title, release_year from films where release_year between 1990 and 2000

## Quest: Get the title and release year of all films released in 1990 or 2000 that were longer than two hours. Remember, duration is in minutes!
category: selecting multiple columns, where or, where in</br>
query: title, release_year from films where release_year in (1990, 2000) and duration > 120

## Quest: Get the names of people who are still alive, i.e. whose death date is missing.
category: select single column, null and in null</br>
query: select name from people where deathdate is null

## Quest: Get the number of films which don't have a language associated with them.
category: count, null and is null</br>
query: select count(*) from films where language is null

## Quest: Get the names of all people whose names begin with 'B'. The pattern you need is 'B%'.
category: select single column, like and not like</br>
query: select name from people where name like 'B%'

## Quest: Get the names of people whose names have 'r' as the second letter. The pattern you need is '_r%'.
category: select single column, like and not like</br>
query: select name from people where name like '_r%'

## Quest: Use the SUM function to get the total duration of all films.
category : aggregate functions</br>
query: select sum(duration) from films

## Quest: Get the duration of the longest film.
category: aggregate functions</br>
query: select max(duration) from films

## Quest: Get the average duration of all films.
category: aggregate functions</br>
query: select avg(duration) from films

## Quest: Get the average amount grossed by all films.
category: aggregate functions</br>
query: select avg(gross) from films

## Quest: Use the SUM function to get the total amount grossed by all films made in the year 2000 or later.
category: aggregate functions, filtering results</br>
query: select sum(gross) from films where release_year >= 2000

## Quest: Get the average amount grossed by all films whose titles start with the letter 'A'.
category: aggregate functions, filtering results, like and not like</br>
query: select avg(gross) from films where title like 'A%'

## Quest: Get the amount grossed by the worst performing film in 1994.
category: aggregate function, filtering results</br>
query: select min(gross) from films where release_year = 1994

## Quest: Get the amount grossed by the best performing film between 2000 and 2012, inclusive.
category: aggregate function, filtering results, BETWEEN</br>
query: select max(gross) from films where release_year between 2000 and 2012

## Quest(Type2): What is the result of SELECT (10 / 3);?
3

## Quest: Get the title and net profit (the amount a film grossed, 
minus its budget) for all films. Alias the net profit as net_profit.
category: selecting multiple columns, alias (as), arithmetic</br>
query: select title, (gross - budget) as net_profit from films

## Quest: Get the title and duration in hours for all films. The duration is in minutes, so you'll need to divide by 60.0 to get the duration in hours. Alias the duration in hours as duration_hours.
category: selecting multiple columns, alias (as), arithmetic</br>
query: select title, (duration / 60.0) as duration_hours from films

## Quest: Get the average duration in hours for all films, aliased as avg_duration_hours.
category: aggregate duration, arithmetic</br>
query: select avg(duration / 60.0) from films

## Quest: Get the percentage of people who are no longer alive. Alias the result as percentage_dead. Remember to use 100.0 and not 100!
category: count, arithmetic, multiple selects, null and is null, alias (as)</br>
query: select (count(*) * 100.0 / (select count(*) from people)) as percentage_dead from people where deathdate is not null

## Quest: Get the number of decades the films table covers. Alias the result as number_of_decades. The top half of your fraction should be enclosed in parentheses.
category: count, distinct, arithmetic, alias (as)</br>
query: select count(distinct (release_year / 10)) as number_of_decades from films

## Quest: Get the names of people from the people table, sorted alphabetically.
category: order by, selecting single column</br>
query: select name from people order by name

## Quest: Get the names of people, sorted by birth date.
category: selecting single column, order by</br>
query: select name from people order by birthdate

## Quest: Get the birth date and name for every person, in order of when they were born.
category: selecting multiple columns, order by</br>
query: select birthdate, name from people order by birthdate

## Quest: Get the title of films released in 2000 or 2012, in the order they were released
category: selecting single column, where in, filtering results, order by</br>
query: select title from films where release_year in (2000, 2012) order by release_year

## Quest: Get all details for all films except those released in 2015 and order them by duration.
category: selecting multiple columns, filtering columns, order by</br>
query: select * from films where release_year != 2015 order by duration

## Quest: Get the title and gross earnings for movies which begin with the letter 'M' and order the results alphabetically.
category: selecting multiple columns, like and not like, order by</br>
query: select title, gross from films where title like 'M%' order by title

## Quest: Get the IMDB score and film ID for every film from the reviews table, sorted from highest to lowest score.
category: selecting multiple columns, order by (desc)</br>
query: select imdb_score, film_id from reviews from reviews order by imdb_score desc</br>
note : i used distinct function to detect if there is any non unique film_id in reviews meaning multiple reviews on same film so if it had became true then there would be a need to use foreign key with multiple select queries between films table and reviews table but i understood there is no need to do this here.

## Quest: Get the title and duration for every film, in order of longest duration to shortest.
category: selecting multiple columns, order by (desc)</br>
query: select title, duration form films order by duration desc

## Quest: Get the birth date and name of people in the people table, in order of when they were born and alphabetically by name.
category: selecting multiple columns, order by (multiple)</br>
query: select birthdate and name from people order by birthdate, name

## Quest: Get certifications, release years, and titles of films ordered by certification (alphabetically) and release year.
category: selecting multiple columns, order by (multiple)</br>
query: select certification, release_year, title from films order by certification, release_year

## Quest: Get the release year and count of films released in each year.
category: count, selecting multiple columns, group by</br>
query: select release_year, count(*) films group by release_year

## Quest: Get the release year and average duration of all films, grouped by release year.
category: aggregate functions, selecting semi multiple columns, group by</br>
query: select release_year, avg(duration) from films group by release_year

## Quest: Get the release year and largest budget for all films, grouped by release year.
category: selecting semi multiple columns, group by, aggregate functions</br>
query: select release_year, max(budget) from films group by release_year

## Quest: Get the language and total gross amount films in each language made.
category: selecting semi multiple columns, group by, aggregate functions</br>
query: select language, sum(gross) from films group by language

## Quest: Get the release year, country, and highest budget spent making a film for each year, for each country. Sort your results by release year and country.
category: selecting multiple columns, aggregate function, group by (multiple), order by (multiple)</br>
query: select release_year, country, max(budget) from films group by release_year, country order by release_year, country
 |
 |
\ /
 .
## Quest: In how many different years were more than 200 movies released? (Having)
category: selecting multiple columns, aggregate function, group by (multiple), order by (multiple), having</br>
query: select release_year, country, max(budget) from films group by release_year, country having (count(*) > 150) order by release_year, country

## Quest: Get the country, average budget, and average gross take of countries that have made more than 10 films. Order the result by country name, and limit the number of results displayed to 5. You should alias the averages as avg_budget and avg_gross respectively.
category: selecting semi multiple columns, aggregate functions, group by, having, order by, count, limit, alias (as)</br>
query: select country, avg(budget) as avg_budget, avg(gross) as avg_gross from films group by country having (count(*) > 10) order by country limit 5
