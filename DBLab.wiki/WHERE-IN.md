`Question` Get the title and release year of all films released in 1990 or 2000 that were longer than two hours. Remember, duration is in minutes!
``` sql
Select title, release_year
From films
Where release_year In (1990, 2000)
And duration > 120
```

