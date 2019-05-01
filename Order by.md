Get the release year, country, and highest budget spent making a film for each year, for each country. Sort your results by release year and country.

Select country, release_year, max(budget) from films
group by release_year, country
order by release_year, country

Select country, av(budget) as avg_budget, avg(gross) as avg_gross from films
group by country
having count(title) > 10
order by country
limit 5