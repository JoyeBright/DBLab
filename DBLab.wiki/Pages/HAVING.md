`Question` In how many different years were more than 200 movies released?
``` sql
Select release_year
From films
Group By release_year
Havinf Count(title) > 200
```

***

`Question` Get the country, average budget, and average gross take of countries that have made more than 10 films. Order the result by country name, and limit the number of results displayed to 5. You should alias the averages as avg_budget and avg_gross respectively.
``` sql
Select country, AVG(budget) AS avg_budget, AVG(gross) AS avg_gross
From films
Group By country
Having Count(title) > 10
Order By country
Limit 5
```