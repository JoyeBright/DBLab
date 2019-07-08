In how many different years were more than 200 movies released?

Select release_year from films
group By release_year
having Count(title) > 200

Get the country, average budget, and average gross take of countries that have made more than 10 films. Order the result by country name, and limit the number of results displayed to 5. You should alias the averages as avg_budget and avg_gross respectively.

Select country, av(budget) as avg_budget, avg(gross) as avg_gross from films
group by country
having count(title) > 10
order by country
limit 5