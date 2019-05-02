## Selecting Single Columns

Select the `title` column from the `films` table:
```sql
select title
from films;
```

Select the `release_year` column from the `films` table:
```sql
select release_year
from films;
```

Select the `name` of each person in the `people` table:
```sql
select name
from people;
```

Get the title of every film from the `films` table:
```sql
select title
from films;
```

## Selecting Multiple Columns

Get the title and release year for every film:
```sql
select title, release_year
from films;
```

Get the title, release year and country for every film:
```sql
select title, release_year, country
from films;
```

Get all columns from the `films` table:
```sql
select * from
films;
```
## Select DISTINCT

Get all the unique countries represented in the `films` table:
```sql
select distinct country
from films;
```

Get all the different film certifications from the `films` table:
```sql
select distinct certification
from films;
```

Get the different types of film roles from the `roles` table:
```sql
select distinct role
from roles;
```
## Learning to COUNT

Count the number of rows in the `people` table:
```sql
select count(*)
from people;
```

Count the number of (non-missing) birth dates in the `people` table:
```sql
select count(birthdate)
from people;
```

Count the number of unique birth dates in the `people` table:
```sql
select count(distinct birthdate)
from people;
```

Count the number of unique countries in the `films` table:
```sql
select count(distinct country)
from films;
```
