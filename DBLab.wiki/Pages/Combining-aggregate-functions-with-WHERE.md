`Question` Use the `SUM` function to get the total amount grossed by all films made in the year 2000 or later.
``` sql
Select SUM(gross)
From films
Where release_year >= 2000
```

***

`Question` Get the average amount grossed by all films whose titles start with the letter 'A'.
``` sql
Select AVG(gross)
From films
Where title Like 'A%'
```

`Question` Get the amount grossed by the worst performing film in 1994.
``` sql
Select MIN(gross)
From films
Where release_year = 1994
```

***

`Question` Get the amount grossed by the best performing film between 2000 and 2012, inclusive.
``` sql
Select MAX(gross)
From films
Where release_year Between 2000 And 2012
```







