- DISTINCT

`SELECT DISTINCT author_lname FROM books;`

`SELECT DISTINCT CONCAT(author_fname,' ', author_lname) FROM books;`

`SELECT DISTINCT author_fname, author_lname FROM books;`

- ORDER BY

```
SELECT title, author_fname, author_lname 
FROM books ORDER BY 1 DESC;
```

``` 
SELECT author_lname, title
FROM books ORDER BY 2;
```

``` 
SELECT author_fname, author_lname FROM books 
ORDER BY author_lname, author_fname;
```

- LIMIT

```
SELECT tite, released_year from books
ORDER BY released_year DESC LIMIT 10;
```

```
SELECT tite, released_year from books
ORDER BY released_year DESC LIMIT 5, 10; // LIMIT (shift, count)
```

- LIKE

`SELECT title FROM books WHERE  title LIKE 'the';`

`SELECT title FROM books WHERE  title LIKE '%the';`

`SELECT title FROM books WHERE title LIKE '%the%';`

`SELECT title, stock_quantity FROM books WHERE stock_quantity LIKE '____';`
 
`SELECT title, stock_quantity FROM books WHERE stock_quantity LIKE '__';`
 
`(235)234-0987 LIKE '(___)___-____'`