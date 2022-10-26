- Char

CHAR has a fixed length
예를 들어, CHAR(5)일 때 'abc'를 넣으면 'abc  '로 저장되고, 'abcdefg'를 넣으면 'abcde'로 저장됨.
근데 거의 안쓰고, 극한의 최적화를 할 때 씀.

- VARCHAR

웬만하면 이거 씀.

- DECIMAL

```
CREATE TABLE items(price DECIMAL(5,2));

INSERT INTO items(price) VALUES(7); // 7.00
INSERT INTO items(price) VALUES(7987654); // 999.99
INSERT INTO items(price) VALUES(34.88); // 34.88
INSERT INTO items(price) VALUES(298.9999); // 299.00
INSERT INTO items(price) VALUES(1.9999); // 2.00
```

