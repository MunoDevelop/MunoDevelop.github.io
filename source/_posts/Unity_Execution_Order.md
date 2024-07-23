---
title: Unity 이벤트 함수 실행 순서
tags:
    - unity
date: 2023-02-14 18:49:36
---

## 이벤트 함수 실행 순서

Unity Document 에 잘 나와 있다.

https://docs.unity3d.com/kr/2021.3/Manual/ExecutionOrder.html

:::tip

fixed update -- 절대 시간 타이머형 콜백 함수.
update -- 프레임마다 호출 되기 때문에 초당 프레임이 떨어지면 호출이 줄어든다.
LateUpdate -- update 끝나면 호출, update 가 끝난후 해야 할 일이 있을 경우
lateUpdate 에 작성

:::

그외 딱히 특별한 부분은 없고 unity document 에서 보면 됨

## 더블 group by
단일 년도에 가장 많은 홈런을 날린 팀?
팀 단위로 묶고 년 단위로도 묶어야 한다.(1팀 1년도가 한 row 일 경우)
group by teamID,yearID 같은 방식으로 조회 가능

