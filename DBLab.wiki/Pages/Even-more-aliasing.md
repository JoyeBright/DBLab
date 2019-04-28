`Question` Get the percentage of `people` who are no longer alive. Alias the result as `percentage_dead`. Remember to use `100.0` and not `100`!
``` sql
Select Count(deathdate) * 100.0 / Count(*) AS percentage_dead
From people
```

***

`Question` Get the number of decades the `films` table covers. Alias the result as `number_of_decades`. The top half of your fraction should be enclosed in parentheses.
``` sql
Select (MAX(release_year) - MIN(release_year)) / 10.0
As number_of_decades
From films
```