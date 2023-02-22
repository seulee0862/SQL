링크
https://school.programmers.co.kr/learn/courses/30/lessons/131114

* ifnull(칼럼, 원하는값) -> 널이면 칼럼값'원하는값'으로 변경돼 출력

```mysql
SELECT
    warehouse_id, warehouse_name,address, ifnull(freezer_yn, 'N')
from
    food_warehouse
where
    address like '%경기도%'
order by
    warehouse_id asc;
```