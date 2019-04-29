`Question` Get the birth date and name of people in the people table, in order of when they were born and alphabetically by name.
``` sql
Select birthdate, name
From people
Order By birthdate, name
```

***

`Question` Get certifications, release years, and titles of films ordered by certification (alphabetically) and release year.
``` sql
Select certification, release_year, title
From films
Order By certification, release_year
```
