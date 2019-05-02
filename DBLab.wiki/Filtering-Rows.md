## Filtering results

Get all details for all films released in 2016:
```sql
select *
from films
where release_year = 1996;
```
## Simple filtering of numeric values

Get the number of films released before 2000:
```sql
select count(*)
from films 
where release_year < 2000;
```

Get the title and release year of films released after 2000:
```sql
select title, release_year
from films
where release_year > 2000;
```
## Simple filtering of text

Get all details for all French language films:
```sql
select *
from films
where language = 'French';
```

Get the name and birth date of the person born on November 11th, 1974. Remember to use ISO date format (`'1974-11-11'`):
```sql
select name, birthdate
from people
where birthdate = '1974-11-11';
```

Get the number of Hindi language films:
```sql
select count(*)
from films
where language = 'Hindi';
```

Get all details for all films with an R certification:
```sql
select *
from films
where certification = 'R';
```
## WHERE AND

Get the title and release year for all Spanish language films released before 2000:
```sql
select title, release_year
from films
where language = 'Spanish' and release_year < 2000;
```

Get all details for Spanish language films released after 2000:
```sql
select *
from films
where language = 'Spanish' and release_year > 2000;
```

Get the title and release year for films released in the 90s:
```sql
select title, release_year
from films
where release_year >= 1990 and release_year < 2000;
```
## WHERE OR

## WHERE AND OR

Get the title and release year of all films released in 1990 or 2000 that were longer than two hours. Remember, duration is in minutes:
```sql
select title, release_year
from films
where (release_year = 1990 or release_year = 2000) and duration > 120;
```
## BETWEEN

Get the title and release year of all films released between 1990 and 2000 (inclusive):
```sql
select title, release_year
from films
where release_year between 1990 and 2000;
```
## WHERE IN

## NULL and IS NULL

Get the names of people who are still alive, i.e. whose death date is missing:
```sql
select name
from people
where deathdate is null;
```

Get the number of films which don't have a language associated with them:
```sql
select count(*)
from films
where language is null;
```
## Like and NOT LIKE

Get the names of all people whose names begin with 'B'. The pattern you need is `'B%'`:
```sql
select name
from people
where name like 'B%';
```

Get the names of people whose names have 'r' as the second letter. The pattern you need is `'_r%'`:
```sql
select name
from people
where name like '_r%';
```
