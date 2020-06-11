---
title: 언어
description: 브라우저의 기본 언어 설정입니다.
translation-type: tm+mt
source-git-commit: 2c262e5345c39a71a6a54062c607273528294b24
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# 언어

&#39;언어&#39; 차원은 방문자가 컨텐트를 보는 데 선호하는 상위 언어를 보여줍니다. 이 차원은 현지화 작업에 도움이 되는 방문자의 가장 자주 사용하는 언어를 이해하려는 경우 중요합니다.

> [!NOTE] 이 차원은 사이트의 언어를 수집하지 않습니다. 차원에서 사이트의 언어를 수집하려는 경우 eVar와 같은 사용자 지정 변수를 사용하는 것이 [좋습니다](evar.md).

## 데이터로 이 차원 채우기

이 차원은 Adobe 내부 조회 테이블을 참조합니다. 조회 값은 이미지 요청의 `Accept-Language` HTTP 헤더를 기반으로 합니다. AppMeasurement 라이브러리(예: Adobe Experience Platform Launch)를 사용하는 경우 이 차원은 기본적으로 작동합니다.

## 차원 값

차원 값에는 방문자 기본 언어의 친숙한 이름이 포함됩니다. Examples include `"English (United States)"`, `"English (United Kingom)"`, `"Chinese (China)"`, and `"Spanish (Spain)"`. 이미지 요청에 HTTP 헤더에 올바른 언어가 포함되어 있지 않으면 차원 값이 됩니다 `"None"`.
