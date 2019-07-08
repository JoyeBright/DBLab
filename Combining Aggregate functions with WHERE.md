Use the SUM function to get the total amount grossed by all films made in the year 2000 or later.

Select SUM(gross) from films
Where release_year >= 2000

Get the average amount grossed by all films whose titles start with the letter 'A'.

Select avg(gross) from films
Where title Like 'A%'

Get the amount grossed by the worst performing film in 1994.

Select min(gross) from films
Where release_year = 1994

Get the amount grossed by the best performing film between 2000 and 2012, inclusive.

Select max(gross) from films
Where release_year between 2000 and 2012
