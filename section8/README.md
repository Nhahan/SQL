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