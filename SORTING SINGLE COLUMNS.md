Get the names of people from the people table, sorted alphabetically.

Select name from people
order by  name

Get the names of people, sorted by birth date.

Select name from people
order by birthdate

Get the birth date and name for every person, in order of when they were born.

Select name, birthdate from people
order by birthdate

Get the title of films released in 2000 or 2012, in the order they were released.

Select title from films
where release_year in (2000, 2012)
order by release_year

Get all details for all films except those released in 2015 and order them by duration.

Select * from
Where release_year = 2015
order by duration

Get the title and gross earnings for movies which begin with the letter 'M' and order the results alphabetically.

Select title, gross from films
where title like 'M%'
order by title