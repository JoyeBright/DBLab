## Aggregate function

Use the `SUM` function to get the total duration of all films:
```sql
select sum(duration)
from films;
```

Get the duration of the longest film:
```sql
select max(duration)
from films;
```

Get the average duration of all films:
```sql
select avg(duration)
from films;
```

Get the average amount grossed by all films:
```sql
select avg(gross)
from films;
```
## Combining aggregate functions with WHERE

Use the `SUM` function to get the total amount grossed by all films made in the year 2000 or later:
```sql
select sum(gross)
from films
where release_year >= 2000;
```

Get the average amount grossed by all films whose titles start with the letter 'A':
```sql
select avg(gross)
from films
where title like 'A%';
```

Get the amount grossed by the worst performing film in 1994:
```sql
select min(gross)
from films
where release_year = 1994;
```

Get the amount grossed by the best performing film between 2000 and 2012, inclusive:
```sql
select max(gross)
from films
where release_year between 2000 and 2012;
```
## A note on arithmetic

What is the result of `SELECT (10 / 3);`?
```
3
```
## It's AS simple AS aliasing

Get the title and net profit (the amount a film grossed, minus its budget) for all films. Alias the net profit as `net_profit`:
```sql
select title, (gross - budget) as net_profit
from films;
```

Get the title and duration in hours for all films. The duration is in minutes, so you'll need to divide by 60.0 to get the duration in hours. Alias the duration in hours as `duration_hours`:
```sql
select title, (duration / 60.0) as duration_hours
from films;
```
## Even more aliasing

Get the average duration in hours for all films, aliased as `avg_duration_hours`:
```sql
select avg(duration) / 60.0 as avg_duration_hours
from films;
```

Get the percentage of `people` who are no longer alive. Alias the result as `percentage_dead`. Remember to use `100.0` and not `100`:
```sql
select count(deathdate) * 100.0 / count(*) as percentage_dead
from people;
```

Get the number of decades the `films` table covers. Alias the result as `number_of_decades`. The top half of your fraction should be enclosed in parentheses:
```sql
select count(distinct release_year / 10) as number_of_decades
from films;
```
