- 데이터 삽입

```
INSERT INTO <tablename>(column, column)
VALUES (value, value);
```

- 다중 데이터 삽입(bulk insert)

```
INSERT INTO <tablename>(column, column)
VALUES (value, value)
      ,(value, value)
      ,(value, value);
```

- 데이터 선택

`SELECT * FROM <tablename>`

- Warning 보기

`SHOW WARNINGS`

- Default 설정

```
CREATE TABLE <tablename>
  (
    <columnname> (value, value) DEFAULT (value),
    <columnname> (value, value) DEFAULT (value)
  )
```