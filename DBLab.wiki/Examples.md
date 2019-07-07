# Examples

Template of examples:
>English Phrase

```SQL
Corresponding SQL query
```

## Selecting Columns

1. [Selecting Single Columns](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#selecting-single-column)
1. [Selecting Multiple Columns](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#selecting-multiple-columns)
1. [Select DISTINCT](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#select-distinct)
1. [Learning to COUNT](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#learning-to-count)

### Selecting Single Column

>Select the title column from the films table.

```SQL
SELECT title from films
```

---
>Select the release_year column from the films table.

```SQL
SELECT release_year from films
```

---
>Select the name of each person in the people table.

```SQL
SELECT name from people
```

---
>Get the title of every film from the films table.

```SQL
SELECT title from films
```

---
>Get the title of every film from the films table.

```SQL
SELECT title from films
```

---

### Selecting Multiple Columns

>Get the title and release year for every film.

```SQL
SELECT title, release_year from films
```

---
>Get the title, release year and country for every film.

```SQL
SELECT title, release_year, country from films
```

---

>Get all columns from the films table.

```SQL
SELECT * from films
```

---

### Select DISTINCT

>Get all the unique countries represented in the films table.

```SQL
SELECT DISTINCT(country) FROM films
```

---
>Get all the different film certifications from the films table.

```SQL
SELECT DISTINCT(certification) from films
```

---
>Get the different types of film roles from the roles table.

```SQL
SELECT DISTINCT(role) from roles
```

---

### Learning to COUNT

>Count the number of rows in the people table.

```SQL
SELECT COUNT(*) from people
```

---
>Count the number of (non-missing) birth dates in the people table.

```SQL
SELECT COUNT(birthdate) from people
```

---
>Count the number of unique birth dates in the people table.

```SQL
SELECT COUNT(DISTINCT(birthdate)) from people
```

---
>Count the number of unique countries in the films table.

```SQL
SELECT DISTINCT(country) from films
```

---

## Filtering Rows

1. [Filtering Results](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#filtering-results)
1. [Simple filtering of numeric values](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#simple-filtering-of-numeric-values)
1. [Simple filtering of text](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#simple-filtering-of-text)
1. [WHERE AND](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#and)
1. [WHERE AND OR](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#and-or)
1. [BETWEEN](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#between)
1. [NULL and IS NULL](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#null-and-is-null)
1. [Like and NOT LIKE](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#like-and-not-like)

### Filtering Results

>Get all details for all films released in 2016.

```SQL
SELECT * FROM films WHERE release_year='2016'
```

---

### Simple Filtering of Numeric Values

>Get the number of films released before 2000.

```SQL
SELECT COUNT(*) from films WHERE release_year < 2000
```

---
>Get the title and release year of films released after 2000.

```SQL
SELECT COUNT(*) FROM films WHERE release_year > 2000
```

---

### Simple Filtering of Text

>Get all details for all French language films.

```SQL
SELECT * from films WHERE language = 'French'
```

---
>Get the name and birth date of the person born on November 11th, 1974. Remember to use ISO date format ('1974-11-11')!

```SQL
SELECT name, birthdate from people WHERE birthdate='1974-11-11'
```

---
>Get the number of Hindi language films.

```SQL
SELECT COUNT(*) FROM films WHERE language='Hindi'
```

---
>Get all details for all films with an R certification.

```SQL
SELECT * from films where certification='R'
```

---

### AND

>Get the title and release year for all Spanish language films released before 2000.

```SQL
SELECT title, release_year FRom films WHERE language='Spanish' AND release_year < 2000
```

---
>Get all details for Spanish language films released after 2000.

```SQL
SELECT * from films WHERE language='Spanish' and release_year > 2000
```

---
>Get the title and release year for films released in the 90s.

```SQL
SELECT title, release_year from films WHERE release_year >= 1990 and  release_year < 2000
```

---

### AND OR

>Get the title and release year of all films released in 1990 or 2000 that were longer than two hours. Remember, duration is in minutes!

```SQL
SELECT title, release_year from films WHERE (release_year = 1990 OR release_year=2000) AND duration > 120
```

---

### BETWEEN

>Get the title and release year of all films released between 1990 and 2000 (inclusive).

```SQL
SELECT title, release_year from films WHERE release_year BETWEEN 1990 and 2000
```

---

### NULL and IS NULL

>Get the names of people who are still alive, i.e. whose death date is missing.

```SQL
SELECT name from people WHERE deathdate is NULL
```

---
>Get the number of films which don't have a language associated with them.

```SQL
SELECT * FROM films WHERE LANGUAGE is NULL
```

---

### LIKE and NOT LIKE

>Get the names of all people whose names begin with 'B'. The pattern you need is 'B%'.

```SQL
SELECT name from people WHERE name LIKE 'B%'
```

---
>Get the names of people whose names have 'r' as the second letter. The pattern you need is '_r%'.

```SQL
SELECT name FROM people WHERE name LIKE '_r%'
```

---

## Aggregate Functions

1. [Aggregate Function](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#aggregate-function)
1. [Combining Aggregate Functions with WHERE](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#combining-aggregate-functions-with-where)
1. [A Note on Arithmetic](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#a-note-on-arithmetic)
1. [It's AS simple AS Aliasing](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#its-as-simple-as-aliasing)
1. [Even More Aliasing](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#even-more-aliasing)

### Aggregate Function

>Use the SUM function to get the total duration of all films.

```SQL
SELECT SUM(duration) FROM films
```

---
>Get the duration of the longest film.

```SQL
SELECT MAX(duration) FROM films
```

---
>Get the average duration of all films.

```SQL
SELECT AVG(duration) from films
```

---
>Get the average amount grossed by all films.

```SQL
SELECT AVG(gross) from films
```

---

### Combining aggregate functions with WHERE

>Use the SUM function to get the total amount grossed by all films made in the year 2000 or later.

```SQL
SELECT SUM(gross) FROM films WHERE release_year >= 2000
```

---
>Get the average amount grossed by all films whose titles start with the letter 'A'.

```SQL
SELECT AVG(gross) FROM films WHERE title LIKE 'A%'
```

---
>Get the amount grossed by the worst performing film in 1994.

```SQL
SELECT MIN(gross) FROM films WHERE release_year = 1994
```

---
>Get the amount grossed by the best performing film between 2000 and 2012, inclusive.

```SQL
SELECT MAX(gross) FROM films WHERE release_year BETWEEN 2000 and 2012
```

---

### A Note on Arithmetic

>What is the result of SELECT (10 / 3)?

```SQL
SELECT 10/3
```

---

### It's AS Simple AS Aliasing

>Get the title and net profit (the amount a film grossed, minus its budget) for all films. Alias the net profit as net_profit.

```SQL
SELECT title, (gross - budget) as net_profit FROM films
```

---
>Get the title and duration in hours for all films. The duration is in minutes, so you'll need to divide by 60.0 to get the duration in hours. Alias the duration in hours as duration_hours.

```SQL
SELECT title, duration/60.0 as duration_hours FROM films
```

---
>Get the average duration in hours for all films, aliased as avg_duration_hours.

```SQL
SELECT AVG(duration)/60.0 as avg_duration_hours from films
```

---

### Even More Aliasing

>Get the percentage of people who are no longer alive. Alias the result as percentage_dead. Remember to use 100.0 and not 100!

```SQL
SELECT COUNT(deathdate)/cast(COUNT(*) as DECIMAL)*100.0 as percentage_dead FROM people
```

---
>Get the number of decades the films table covers. Alias the result as number_of_decades. The top half of your fraction should be enclosed in parentheses.

```SQL
SELECT (MAX(release_year) - MIN(release_year)) / 10 as number_of_decades FROM films
```

---

## Sorting, Grouping

1. [Sorting single columns](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#sorting-single-columns)
1. [Sorting single columns (DESC)](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#sorting-single-columns-desc)
1. [Sorting multiple columns](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#sorting-multiple-columns)
1. [GROUP BY](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#group-by)
1. [HAVING](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#having)
1. [Limit](https://github.com/Nikronic/DBLab/blob/master/DBLab.wiki/Examples.md#limit)

### Sorting Single Columns

>Get the names of people from the people table, sorted alphabetically.

```SQL
SELECT name from people ORDER BY name
```

---
>Get the names of people, sorted by birth date.

```SQL
SELECT name from people ORDER BY birthdate
```

---
>Get the birth date and name for every person, in order of when they were born.

```SQL
SELECT birthdate, name FROM people ORDER BY birthdate
```

---
>Get the title of films released in 2000 or 2012, in the order they were released

```SQL
SELECT title from films WHERE release_year=2000 or release_year=2012 ORDER BY release_year
```

---
>Get all details for all films except those released in 2015 and order them by duration.

```SQL
SELECT * from films WHERE not release_year=2015 ORDER BY duration
```

---
>Get the title and gross earnings for movies which begin with the letter 'M' and order the results alphabetically.

```SQL
SELECT title, gross from films WHERE title LIKE 'M%' ORDER BY title
```

---
>Get the title and gross earnings for movies which begin with the letter 'M' and order the results alphabetically.

```SQL
SELECT title, gross from films WHERE title LIKE 'M%' ORDER BY title
```

---

### Sorting Single Columns (DESC)

>Get the title and duration for every film, in order of longest duration to shortest.

```SQL
SELECT title, duration from films WHERE duration is not NULL ORDER BY duration DESC
```

---

### Sorting Multiple Columns

>Get the birth date and name of people in the people table, in order of when they were born and alphabetically by name.

```SQL
SELECT birthdate, name from people ORDER BY birthdate, name
```

---
>Get certifications, release years, and titles of films ordered by certification (alphabetically) and release year.

```SQL
SELECT certification, release_year, title from films ORDER BY certification, release_year
```

---

### Group By

>Get the release year and count of films released in each year.

```SQL
SELECT release_year, COUNT(*) FROM films GROUP BY release_year
```

---
>Get the release year and average duration of all films, grouped by release year.

```SQL
SELECT release_year, AVG(duration) from films GROUP BY release_year
```

---
>Get the release year and largest budget for all films, grouped by release year.

```SQL
SELECT release_year, MAX(budget) from films GROUP BY release_year
```

---
>Get the language and total gross amount films in each language made.

```SQL
SELECT language, SUM(gross) from films GROUP BY language
```

---
>Get the release year, country, and highest budget spent making a film for each year, for each country. Sort your results by release year and country.

```SQL
SELECT release_year, country, MAX(budget) from films GROUP BY release_year, country ORDER BY release_year, country
```

---

### Having

>In how many different years were more than 200 movies released? (Having)

```SQL
SELECT release_year, COUNT(*) from films GROUP BY release_year HAVING COUNT(*) > 200
```

---

### LIMIT

>Get the country, average budget, and average gross take of countries that have made more than 10 films. Order the result by country name, and limit the number of results displayed to 5. You should alias the averages as avg_budget and avg_gross respectively.

```SQL
SELECT country, AVG(budget), AVG(gross) from films GROUP BY country HAVING COUNT(*) > 10 ORDER BY country LIMIT 5
```

---
