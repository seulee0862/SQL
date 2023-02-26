링크
https://school.programmers.co.kr/learn/courses/30/lessons/59410

* ifnull(칼럼, 원하는값) -> 널이면 칼럼값'원하는값'으로 변경돼 출력

```mysql
SELECT
    animal_type, ifnull(name, 'No name') name, sex_upon_intake
from
    animal_ins
order by
    animal_id
```