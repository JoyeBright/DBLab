Get the release year and count of films released in each year.

Select release_year, count(*) from films
group by release_year

Get the release year and average duration of all films, grouped by release year.

Select release_year, avg(duration) from films
group by release_year

Get the release year and average duration of all films, grouped by release year.

Select release_year, avg(duration) from films
group by release_year

Question Get the release year and largest budget for all films, grouped by release year.

Select release_year, max(budget) from films
group by release_year

Get the language and total gross amount films in each language made.

Select language, sum(gross) from films
group by language

Get the release year, country, and highest budget spent making a film for each year, for each country. Sort your results by release year and country.

Select country, release_year, max(budget) from films
group by release_year, country
order by release_year, country