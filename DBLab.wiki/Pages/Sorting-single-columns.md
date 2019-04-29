`Question` Get the names of people from the people table, sorted alphabetically.
``` sql
Select name
From people
Order By name
```

***

`Question` Get the names of people, sorted by birth date.
``` sql
Select name
From people
Order By birthdate
```

***

`Question` Get the birth date and name for every person, in order of when they were born.
``` sql
Select name, birthdate
From people
Order By birthdate
```

***

`Question` Get the title of films released in 2000 or 2012, in the order they were released.
``` sql
Select title
From films
Where release_year In (2000, 2012)
Order By release_year
```

***

`Question` Get all details for all films except those released in 2015 and order them by duration.
``` sql
Select *
From films
Where release_year <> 2015
Order By duration
```

***

`Question` Get the title and gross earnings for movies which begin with the letter 'M' and order the results alphabetically.
``` sql
Select title, gross
From films
Where title LIKE 'M%'
Order By title
```



