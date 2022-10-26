- CONCAT

```
SELECT
  CONCAT(author_fname, ' ', author_lname)
  AS 'full name'
FROM books;
```
 
```
SELECT author_fname AS first, author_lname AS last, 
  CONCAT(author_fname, ' ', author_lname) AS full
FROM books;
```

```
SELECT author_fname AS first, author_lname AS last, 
  CONCAT(author_fname, ', ', author_lname) AS full
FROM books;
```
 
```
SELECT CONCAT(title, '-', author_fname, '-', author_lname) FROM books;
를 아래처럼 표현 가능
SELECT 
    CONCAT_WS(' - ', title, author_fname, author_lname) 
FROM books;
```
