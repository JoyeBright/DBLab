Count the number of rows in the people table.
select count(*) from people

Count the number of (non-missing) birth dates in the people table.
select count(birthdate) from people

Count the number of unique birth dates in the people table.
select count(DISTINCT(birthdate)) from people

Count the number of unique countries in the films table.
select count(country) from films