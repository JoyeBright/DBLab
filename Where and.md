Get the title and release year for all Spanish language films released before 2000.
select title, release_year from films where language='Spanish' and release_year < 2000

Get all details for Spanish language films released after 2000.
select * from films where language='Spanish' and release_year > 2000

Get the title and release year for films released in the 90s.
select title, release_year from films where release_year >= 1990 and  release_year < 2000
 