Get all details for all films released in 2016.
select * from films where release_year='2016'

Get the number of films released before 2000.
select count(*) from films where release_year < 2000

Get the title and release year of films released after 2000.
select count(*) FROM films WHERE release_year > 2000

Get all details for all French language films.
select * from films WHERE language = 'French'

Get the name and birth date of the person born on November 11th, 1974.
Remember to use ISO date format ('1974-11-11')!
select name, birthdate from people WHERE birthdate='1974-11-11'

Get the number of Hindi language films.
select count(*) FROM films WHERE language='Hindi'

Get all details for all films with an R certification.
select * from films where certification='R'