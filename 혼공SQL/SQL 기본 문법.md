# SELECT ~ FROM ~ WHERE

**SELECT** - 구축이 완료된 테이블에서 데이터를 추출하는 기능. (*전체 또는 열 이름들이 들어간다)

```SQL
-- addr열에서 경기, 전남, 경남인 데이터 행에서 mem_name과 addr 열의 데이터들만 뽑아내라
SELECT mem_name, addr FROM member WHERE addr IN('경기', '전남', '경남');

-- 위와 동일한 결과
SELECT mem_name, addr FROM member WHERE addr = '경기' OR addr = '전남' OR addr = '경남';
```

```SQL
-- '우'를 가장 앞에 포함하는것 전부 뽑아내라
SELECT * FROM member WHERE mem_name LIKE '우%' 
```

```SQL
-- mem_name열에서 중 앞에 두글자가 있고 뒤에는 '핑크'인 데이터행 뽑아내라
SELECT * FROM FROM member WHERE mem_name LIKE '__핑크' 
```


## SELECT절의 형식 (ORDER BY, GROUP BY)

![Untitled](https://github.com/junhosong0/MySQL/assets/117610783/d37830d2-26f7-4959-a21b-a7418c05b7a6)

### ORDER BY (정렬 기능)

```SQL
-- member테이블에서 height가 165이상인 데이터행들 중에서 debut_date로 내림차순 정렬하고 가장 위의 3번째부터 2개의 데이터행들을 보여주는데 mem_name과 debut_date 열들만 보여줘라

SELECT mem_name, debut_date --- 5
	FROM member --- 1
	WHERE height >= 165 --- 2
	ORDER BY debut_date DESC --- 3
	LIMIT 3, 2 --- 4
```

```SQL
-- 중복된것들 제거하고 하나씩만 보여줘라
SELECT DISTINCT addr FROM member 
```

### GROUP BY (묶어주는 기능)

![Untitled (1)](https://github.com/junhosong0/MySQL/assets/117610783/274ba589-0694-4a5c-828a-5038cee8a049)

```SQL
SELECT mem_id "회원 아이디", SUM(amount) "총 구매 개수" 
	FROM buy GROUP BY mem_id;
```

**결과 값**
![Untitled (2)](https://github.com/junhosong0/MySQL/assets/117610783/729a2082-e642-455b-9ac1-356b9bda9d3c)


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
