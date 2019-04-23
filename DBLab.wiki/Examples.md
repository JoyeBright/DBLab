# Examples

## Selecting Columns

1. Selecting Single Columns
1. Selecting Multiple Columns
1. Select DISTINCT
1. Learning to COUNT

### Selecting Single Column

>Select the title column from the films table.

```SQL
SELECT title from films
```

---
>Select the release_year column from the films table.

```SQL
SELECT release_year from films
```

---
>Select the name of each person in the people table.

```SQL
SELECT name from people
```

---
>Get the title of every film from the films table.

```SQL
SELECT title from films
```

---
>Get the title of every film from the films table.

```SQL
SELECT title from films
```

---

### Selecting Multiple Columns

>Get the title and release year for every film.

```SQL
SELECT title, release_year from films
```

---
>Get the title, release year and country for every film.

```SQL
SELECT title, release_year, country from films
```

---

>Get all columns from the films table.

```SQL
SELECT * from films
```

---

### Select DISTINCT

>Get all the unique countries represented in the films table.

```SQL
SELECT DISTINCT(country) FROM films
```

---
>Get all the different film certifications from the films table.

```SQL
SELECT DISTINCT(certification) from films
```

---
>Get the different types of film roles from the roles table.

```SQL
SELECT DISTINCT(role) from roles
```

---

### Learning to COUNT

>Count the number of rows in the people table.

```SQL
SELECT COUNT(*) from people
```

---
>Count the number of (non-missing) birth dates in the people table.

```SQL
SELECT COUNT(birthdate) from people
```

---
>Count the number of unique birth dates in the people table.

```SQL
SELECT COUNT(DISTINCT(birthdate)) from people
```

---
>Count the number of unique countries in the films table.

```SQL
SELECT DISTINCT(country) from films
```

---