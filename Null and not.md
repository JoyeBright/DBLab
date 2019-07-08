Get the names of people who are still alive, i.e. whose death date is missing.
select name from people where deathdate is null

Get the number of films which don't have a language associated with them.
select * from films where language is null