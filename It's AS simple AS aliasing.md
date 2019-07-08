Question Get the title and net profit (the amount a film grossed, minus its budget) for all films. Alias the net profit as net_profit.

Select title, (gross-budget) as net_profit from films

Question Get the title and duration in hours for all films. The duration is in minutes, so you'll need to divide by 60.0 to get the duration in hours. Alias the duration in hours as duration_hours.

Select title, (duration/60.0) as duration_hours from films

Question Get the average duration in hours for all films, aliased as avg_duration_hours.

Select avg(duration) / 60.0 as avg_duration_hours from films

