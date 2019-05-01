Get the release year and count of films released in each year.

Select release_year, count(*) from films

Get the birth date and name of people in the people table, in order of when they were born and alphabetically by name.

Select birthdate, name from people
order by birthdate, name

Get certifications, release years, and titles of films ordered by certification (alphabetically) and release year.

Select certification, release_year, title from films
order by certification, release_year