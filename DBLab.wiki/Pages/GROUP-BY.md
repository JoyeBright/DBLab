`Question` Get the release year and count of films released in each year.
``` sql
Select release_year, COUNT(*)
From films
Group By release_year
```

***

`Question` Get the release year and average duration of all films, grouped by release year.
``` sql
Select release_year, AVG(duration)
From films
Group By release_year
```

***

`Question` Get the release year and average duration of all films, grouped by release year.
``` sql
Select release_year, AVG(duration)
From films
Group By release_year
```

***

`Question` Get the release year and largest budget for all films, grouped by release year.
``` sql
Select release_year, MAX(budget)
From films
Group By release_year
```

***

`Question` Get the language and total gross amount films in each language made.
``` sql
Select language, SUM(gross)
From films
Group By language
```

***

`Question` Get the release year, country, and highest budget spent making a film for each year, for each country. Sort your results by release year and country.
``` sql
Select release_year, country, MAX(budget)
From films
Group By release_year, country
Order By release_year, country
```


