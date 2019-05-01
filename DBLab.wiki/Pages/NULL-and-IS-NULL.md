`Question` Get the names of people who are still alive, i.e. whose death date is missing.
``` sql
Select name
From people
Where deathdate Is Null
```

***

`Question` Get the number of films which don't have a language associated with them.
``` sql
Select Count(*)
From films
Where language Is Null
```

