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
query: select count(*) from films where release_year = 2000

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
