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

- MIN or MAX with subquery

```
SELECT * FROM books 
WHERE pages = (SELECT Min(pages) 
                FROM books);
```

- MIN or MAX with GROUP BY

```
SELECT author_fname, 
       author_lname, 
       Min(released_year) 
FROM   books 
GROUP  BY author_lname, 
          author_fname;
```

- SUM

```
SELECT author_fname,
       author_lname,
       Sum(released_year)
FROM books
GROUP BY
    author_lname,
    author_fname;
```

- AVG

```SELECT released_year, AVG(stock_quantity) 
FROM books 
GROUP BY released_year;```