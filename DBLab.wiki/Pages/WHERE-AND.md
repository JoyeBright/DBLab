`Question` Get the title and release year for all Spanish language films released before 2000.
``` sql
Select title, release_year
From films
Where release_year < 2000
And language = 'Spanish'
```

***

`Question` Get all details for Spanish language films released after 2000.
``` sql
Select *
From films
Where release_year > 2000
And language = 'Spanish'
```

***

`Question` Get the title and release year for films released in the 90s.
``` sql
Select title, release_year
From films
Where release_year >= 1990
And release_year < 2000
```
