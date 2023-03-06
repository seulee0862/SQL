링크
https://school.programmers.co.kr/learn/courses/30/lessons/131112

* like 'HE%' -> 'HE' 로시작하는 모든 값 조회

```mysql
SELECT
    factory_id, factory_name, address
from
    food_factory
where
    address like '강원도%'
order by
    factory_id
```