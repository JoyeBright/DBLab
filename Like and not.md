Get the names of all people whose names begin with 'B'. The pattern you need is 'B%'.
select name from people where name like 'B%'

Get the names of people whose names have 'r' as the second letter. The pattern you need is '_r%'.
select name FROM people where name like '_r%'