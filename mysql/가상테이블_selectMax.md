링크
https://school.programmers.co.kr/learn/courses/30/lessons/131124

* WITH 별칭 () SELCET 별칭 으로 가상테이블 사용 가능
* GROUP BY 1 만족하는 데이터 없을경우 결과 출력되지 않음
* ORDER BY 숫자에 해당하는 열 기준으로 오름차순 or 내림차순 정렬
* SELECT MAX 해당열중 최대값 출력

``` mysql
WITH A
AS (
    SELECT MEMBER_ID
           ,COUNT(1) as "cnt"
    FROM REST_REVIEW
    GROUP BY 1 /* 조건 만족하는 행 없을때 결과가 안나오기 위함*/
    )
SELECT B.MEMBER_NAME
        , C.REVIEW_TEXT
        , date_format(C.REVIEW_DATE ,'%Y-%m-%d')
FROM A, MEMBER_PROFILE B, REST_REVIEW C
 WHERE A.cnt = (SELECT MAX(A.cnt) FROM A)
   AND A.MEMBER_ID = B.MEMBER_ID
   AND B.MEMBER_ID = C.MEMBER_ID
ORDER BY  1, 3 /* 해당 열 기준으로 오름차순 정렬 */
```
