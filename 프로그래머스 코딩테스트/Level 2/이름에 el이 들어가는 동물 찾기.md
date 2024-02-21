![20240221_134455](https://github.com/junhosong0/MySQL/assets/117610783/19fd04ff-5400-4497-98c6-21425268f45f)

![20240221_134549](https://github.com/junhosong0/MySQL/assets/117610783/18a9b6fa-e8c3-4ba7-a4c2-84b5aa4ba222)


```SQL
## 동물 보호소에 들어온 동물 이름 중, 이름에 "EL"이 들어가는 개 이름의 대소문자는 구분하지 않습니다. -> WHERE LOWER(NAME) LIKE '%el%' AND ANIMAL_TYPE = 'Dog'
## 아이디와 이름을 조회하는 SQL문을 작성해주세요. -> SELECT ANIMAL_ID, NAME FROM ANIMAL_INS
## 결과는 이름 순으로 조회 -> ORDER BY NAME


SELECT ANIMAL_ID, NAME
FROM ANIMAL_INS
WHERE LOWER(NAME) LIKE '%el%' AND ANIMAL_TYPE = 'Dog'
ORDER BY NAME;
```
