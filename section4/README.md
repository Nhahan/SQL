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

`SELECT * FROM <tablename>;`

- Warning 보기

`SHOW WARNINGS;`

- Default 설정

```
CREATE TABLE <tablename>
  (
    <columnname> (value, value) DEFAULT (value),
    <columnname> (value, value) DEFAULT (value)
  );
```

- Default 설정 with Not Null condition (Null을 허용하지 않음)

```
CREATE TABLE <tablename>
  (
    <columnname> (value, value) NOT NULL DEFAULT (value),
    <columnname> (value, value) NOT NULL DEFAULT (value)
  );
```

- PRIMARY KEY 설정

```
CREATE TABLE cats 
  (
    cat_id INT NOT NULL AUTO_INCREMENT,
    name VARCHAR(100),
    age INT,
    PRIMARY KEY(cat_id)
  );

  CREATE TABLE cats 
  (
    cat_id INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    age INT
  );
```