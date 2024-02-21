![20240221_134455](https://github.com/junhosong0/MySQL/assets/117610783/19fd04ff-5400-4497-98c6-21425268f45f)

![20240221_142818](https://github.com/junhosong0/MySQL/assets/117610783/4e8610f1-f64c-4533-89f7-85d82bfdee86)


**내코드**
```sql
## ANIMAL_INS 테이블에 등록된 모든 레코드에 대해

## 각 동물의 아이디와 이름, 들어온 날짜를 조회 -> SELECT ANIMAL_ID, NAME, DATE

## DATETIME을 DATE로 바꾸기 -> DATE_FORMAT(DATETIME, '%Y-%m-%d') AS DATE (여기서 %Y는 소문자를 쓰면 앞에 20을 날리고 마지막 2개 숫자 년도만 보여주기 때문에 꼭 대문자 %Y를 써줘야함)

## 이때 결과는 아이디 순으로 조회해야 합니다 -> ORDER BY ANIMAL_ID


SELECT ANIMAL_ID, NAME, DATE_FORMAT(DATETIME, '%Y-%m-%d') AS DATE
FROM ANIMAL_INS
ORDER BY ANIMAL_ID;
```

**배울코드**

없음

