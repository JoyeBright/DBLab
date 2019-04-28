`Question` Get all details for all French language films.
``` sql
Select *
From films
Where language = 'French'
```

***

`Question` Get the name and birth date of the person born on November 11th, 1974. Remember to use ISO date format (`'1974-11-11'`)!
``` sql
Select name, birthdate
From people
Where birthdate = '1974-11-11'
```

***

`Question` Get the number of Hindi language films.
``` sql
Select Count(*)
From films
Where language = 'Hindi'
```

***

`Question` Get all details for all films with an R certification.
``` sql
Select * 
From films
Where certification = 'R'
```

