`Question` Count the number of rows in the `people` table.
``` sql
Select Count(*)
From people
```
***
`Question` Count the number of (non-missing) birth dates in the `people` table.
``` sql
Select Count(birthdate)
From people
```
***
`Question` Count the number of unique birth dates in the `people` table.
``` sql
Select Count(Distinct birthdate)
From people
```

***

`Question` Count the number of unique languages in the `films` table.
``` sql
Select Count(Distinct language)
From films
```
