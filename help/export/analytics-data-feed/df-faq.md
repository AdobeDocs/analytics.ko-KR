---
description: 데이터 피드에 대한 FAQ
keywords: Data Feed;job;pre column;post column;case sensitivity
title: 데이터 피드 FAQ
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 데이터 피드 FAQ

데이터 피드에 대한 FAQ

## 접두사가 `post_` 있는 열과 `post_` 접두사가 없는 열 간의 차이점은 무엇입니까?

접두사가 없는 열에는 데이터 수집으로 전송된 것과 정확히 동일한 데이터가 포함됩니다. `post_` 접두사가 `post_` 있는 열에는 처리 후 값이 포함됩니다. 값을 변경할 수 있는 예는 변수 지속성, 처리 규칙, VISTA 규칙, 통화 변환 또는 Adobe가 적용하는 서버측 로직입니다. 가능하면 열의 `post_` 버전을 사용하는 것이 좋습니다.

If a column does not contain a `post_` version (for example, `visit_num`), then the column can be considered a post column.

## 데이터 피드는 대소문자 구분을 어떻게 처리합니까?

Adobe Analytics에서 대부분의 변수는 보고 목적으로 대소문자를 구분하지 않는 것으로 간주됩니다. 예를 들어 'snow', 'Snow', 'SNOW' 및 'sNow'는 모두 동일한 값으로 간주됩니다. 대소문자 구분은 데이터 피드에서 유지됩니다.

게시물이 아닌 열과 게시물 열 사이에 동일한 값의 대소문자가 다른 경우(예: 사전 열의 'snow', 이후 열의 'Snow') 구현에서는 사이트에서 대소문자가 모두 사용됩니다. 이후 열에서 대소문자가 다른 값은 이전에 전달되어 가상 쿠키에 저장되어 있거나, 해당 보고서 세트에 대해 동일한 시간 동안 처리되었습니다.