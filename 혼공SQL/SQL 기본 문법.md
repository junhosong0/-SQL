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
