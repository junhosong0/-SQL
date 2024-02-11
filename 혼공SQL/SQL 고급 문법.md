# MySQL의 데이터 형식
## 정수형(INT)
아래와 같이 4개의 정수형 데이터 형식이 있음.

![Untitled (12)](https://github.com/junhosong0/MySQL/assets/117610783/60d5b130-1d00-41e2-aa1d-e82a2cab093c)

unsigned를 쓰면 아래와 같 음의자리 숫자만큼의 범위를 양의자리로 끌어쓸 수 있음.

![Untitled (13)](https://github.com/junhosong0/MySQL/assets/117610783/95509126-4e74-4a71-a319-de5442e09da1)

```SQL
CREATE TABLE hongong4 (
	tinyint_col TINYINT,
    smallint_col SMALLINT,
    int_col INT,
    bigint_col BIGINT UNSIGNED );
    
INSERT INTO hongong4 VALUES(127, 32767, 214748367, 9000000000000000001);
INSERT INTO hongong4 VALUES(127, 32767, 214748367, 10000000000000000000);

SELECT * FROM hongong4
```
![Untitled (14)](https://github.com/junhosong0/MySQL/assets/117610783/ba3b53d0-db8f-4830-bae8-4711460b151e)


```SQL
```

```SQL
```

```SQL
```

```SQL
```

```SQL
```

```SQL
```

```SQL
```

```SQL
```

```SQL
```

```SQL
```

```SQL
```

```SQL
```

```SQL
```

```SQL
```

