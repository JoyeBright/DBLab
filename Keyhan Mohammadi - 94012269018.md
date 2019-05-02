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
category : aggregate functions
query: select sum(duration) from films

## Quest: Get the duration of the longest film.
category: aggregate functions
query: select max(duration) from films

## Quest: Get the average duration of all films.
category: aggregate functions
query: select avg(duration) from films

## Quest: Get the average amount grossed by all films.
category: aggregate functions
query: select avg(gross) from films

## Quest: Use the SUM function to get the total amount grossed by all films made in the year 2000 or later.
category: aggregate functions, filtering results
query: select sum(gross) from films where release_year >= 2000

## Quest: Get the average amount grossed by all films whose titles start with the letter 'A'.
category: aggregate functions, filtering results, like and not like
query: select avg(gross) from films where title like 'A%'

## Quest: Get the amount grossed by the worst performing film in 1994.
category: aggregate function, filtering results
query: select min(gross) from films where release_year = 1994

## Quest: Get the amount grossed by the best performing film between 2000 and 2012, inclusive.
category: aggregate function, filtering results, BETWEEN
query: select max(gross) from films where release_year between 2000 and 2012

## Quest(Type2): What is the result of SELECT (10 / 3);?
3

## Quest: Get the title and net profit (the amount a film grossed, 
minus its budget) for all films. Alias the net profit as net_profit.
category: selecting multiple columns, alias (as), arithmetic
query: select title, (gross - budget) as net_profit from films

## Quest: Get the title and duration in hours for all films. The duration is in minutes, so you'll need to divide by 60.0 to get the duration in hours. Alias the duration in hours as duration_hours.
category: selecting multiple columns, alias (as), arithmetic
query: select title, (duration / 60.0) as duration_hours from films

## Quest: Get the average duration in hours for all films, aliased as avg_duration_hours.
category: aggregate duration, arithmetic
query: select avg(duration / 60.0) from films

## Quest: Get the percentage of people who are no longer alive. Alias the result as percentage_dead. Remember to use 100.0 and not 100!
category: count, arithmetic, multiple selects, null and is null
query: select (count(*) * 100.0 / (select count(*) from people)) as percentage_dead from people where deathdate is not null

## Quest: Get the number of decades the films table covers. Alias the result as number_of_decades. The top half of your fraction should be enclosed in parentheses.
category: count, distinct, arithmetic
query: select count(distinct (release_year / 10)) as number_of_decades from films
