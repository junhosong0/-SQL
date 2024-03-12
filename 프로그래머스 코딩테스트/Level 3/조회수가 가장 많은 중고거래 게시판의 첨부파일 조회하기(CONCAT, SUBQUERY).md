
![20240312_192300](https://github.com/junhosong0/MySQL/assets/117610783/85785a41-5eed-406d-aa1b-77bc11c3f8c6)

![20240312_192315](https://github.com/junhosong0/MySQL/assets/117610783/1c5e2e0b-351d-4622-bd99-6a76fb68c317)



**내코드**
- 서브쿼리 max(views)값을 구해서 where절에서 view조건과 비교하여 코딩하였음.


```sql
SELECT concat('/home/grep/src/',board_id,'/',file_id,file_name,file_ext) as file_path
from used_goods_board
join used_goods_file using(board_id)
where views = (SELECT max(views) from used_goods_board)
order by file_id desc
```




**배울것**
- join을 굳이 안하고 from 절에 두 테이블을 선언해도 됨
- 대신 where절에서 두 테이블의 board_id가 일치되는 조건을 추가해줘야 함

```sql
SELECT CONCAT("/","home/grep/src","/",b.BOARD_ID,"/",FILE_ID,FILE_NAME, FILE_EXT)FILE_PATH
FROM USED_GOODS_BOARD as b, USED_GOODS_FILE as f
WHERE b.BOARD_ID = f.BOARD_ID
AND VIEWS = (SELECT MAX(VIEWS) 
             FROM USED_GOODS_BOARD)
order by FILE_ID desc
```
