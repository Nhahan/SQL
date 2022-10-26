- COUNT

`SELECT COUNT(*) FROM books;`

`SELECT COUNT(author_fname) FROM books;`

`SELECT COUNT(DISTINCT author_fname) FROM books;`

`SELECT COUNT(DISTINCT author_lname) FROM books;`

`SELECT COUNT(DISTINCT author_lname, author_fname) FROM books;`

`SELECT title FROM books WHERE title LIKE '%the%';`

`SELECT COUNT(*) FROM books WHERE title LIKE '%the%';`

- GROUP BY

`SELECT released_year, COUNT(*) FROM books GROUP BY released_year;`

```
SELECT CONCAT('In ', released_year, ' ', COUNT(*), ' book(s) released') AS year 
  FROM books 
  GROUP BY released_year;
```