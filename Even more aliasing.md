Get the percentage of people who are no longer alive. Alias the result as percentage_dead. Remember to use 100.0 and not 100!

Select count(deathdate) * 100.0 / count(*) as percentage_dead from people

Get the number of decades the films table covers. Alias the result as number_of_decades. The top half of your fraction should be enclosed in parentheses.

Select (max(release_year) – min(release_year)) / 10.0 as number_of_decades from films
