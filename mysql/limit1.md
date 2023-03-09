링크
https://school.programmers.co.kr/learn/courses/30/lessons/131115

* limit n -> 조회값을 n번째 만큼출력
* order by와 limit을 이용하면 특정칼럼의 내림차순의 값을 쉽게 찾아낼 수 있다.

```mysql
SELECT
    *
from
    food_product
order by
    price desc
limit 1;
```