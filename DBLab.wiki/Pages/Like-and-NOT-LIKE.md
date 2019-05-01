`Question`  Get the names of all people whose names begin with 'B'. The pattern you need is `'B%'`.
 ``` sql
Select name
From people
Where name Like 'B%' 
```

***

`Question` Get the names of people whose names have 'r' as the second letter. The pattern you need is `'_r%'`.
``` sql
Select name
From people
Where name Like '_r%'
```