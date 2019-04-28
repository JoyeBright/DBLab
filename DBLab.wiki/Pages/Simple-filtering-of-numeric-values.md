`Question` Get all details for all films released in 2016.
``` sql
Select *
From films
Where release_year = 2016
```

***

`Question` Get the number of films released before 2000.
``` sql
Select Count(*)
From films
Where release_year < 2000
```

***

`Question` Get the title and release year of films released after 2000.
``` sql
Select title, release_year
From films
Where release_year > 2000
```

