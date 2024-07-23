---
title: DB 주의점
tags:
    - db
date: 2023-02-13 18:49:36
---

## sql 구문 순서
select *
from table
where a = b
group by sth
having sth
order by

:::tip

하지만 실제는
from
where
group by
having
select
order by
순서로 만들기 때문에 그룹에서 특정 조건이 끝나고 select 가 시작 된다.

:::


## 더블 group by
단일 년도에 가장 많은 홈런을 날린 팀?
팀 단위로 묶고 년 단위로도 묶어야 한다.(1팀 1년도가 한 row 일 경우)
group by teamID,yearID 같은 방식으로 조회 가능

## 서브쿼리

select *
from players
where playerID IN (select playerID from battingPost )

select *
from players
where Exists (select playerID from battingPost where battingPost.playerID = players.playerID)

사실상 같은 일을 함, 기본 구성을 눈에 익혀둘 것