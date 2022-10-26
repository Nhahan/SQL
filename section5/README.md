- 단순 SELECT 구문

`SELECT * FROM cats;`

`SELECT age, breed, name, cat_id FROM cats;`

- WHERE 절

`SELECT * FROM cats WHERE age=4;`

- Aliases

`SELECT name AS 'cat name' breed AS 'kitty breed' FROM cats;`

- UPDATE 절

`UPDATE cats SET breed = 'Shorthair WHERE breed = 'Tabby';`

`UPDATE cats SET age=14 WHERE name='Misty';`

- DELETE 절

`DELETE FROM cats WHERE name='Egg';`