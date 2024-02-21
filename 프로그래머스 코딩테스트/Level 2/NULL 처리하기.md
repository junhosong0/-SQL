![20240221_134455](https://github.com/junhosong0/MySQL/assets/117610783/19fd04ff-5400-4497-98c6-21425268f45f)

![20240221_135858](https://github.com/junhosong0/MySQL/assets/117610783/076548c8-0845-4196-b868-3ee9ecf1944b)

내코딩

```SQL
## 동물의 생물 종, 이름, 성별 및 중성화 여부를  -> SELECT ANIMAL_TYPE, NAME, SEX_UPON_INTAKE

## 아이디 순으로 조회 -> ORDER BY ANIMAL_ID

## 이름이 없는 동물의 이름은 "No name"으로 표시해 주세요 -> 
## NAME: 
## CASE 
##    WHEN NAME IS NULL THEN 'No name' 
##    WHEN NAME IS NOT NULL THEN NAME
##    END as NAME,


SELECT ANIMAL_TYPE, 
CASE 
    WHEN NAME IS NULL THEN 'No name' 
    WHEN NAME IS NOT NULL THEN NAME
    END as NAME,
SEX_UPON_INTAKE

FROM ANIMAL_INS
ORDER BY ANIMAL_ID;
```
