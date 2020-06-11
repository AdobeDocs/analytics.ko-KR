---
title: 다운로드 링크
description: 다운로드 링크의 이름입니다.
translation-type: tm+mt
source-git-commit: 87d0c7e20594e2e39f55284e8d50d425cc1cdacf
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 15%

---


# 다운로드 링크

&#39;다운로드 링크&#39; 차원은 사이트에 구현된 다운로드 링크의 이름을 보고합니다. 이 차원은 다음과 같은 다운로드 링크에 대한 방문자 행동에 대해 자세히 알고 싶을 때 유용합니다.

* 사이트에서 가장 자주 다운로드되는 파일을 확인합니다.
* 특정 기간에 더 자주 다운로드되는 파일이 있는지 확인합니다.
* 제공되는 경우 방문자가 다른 파일 유형을 다운로드하는지 확인합니다.

## 데이터로 이 차원 채우기

이 차원은 값이 있는 [`pev2` 쿼리 문자열도 포함하는 히트의 이미지 요청에 있는](/help/implement/validate/query-parameters.md) 쿼리 문자열 `pe` 데이터로부터 `lnk_d`수집합니다. 쿼리 문자열에 `pe` 히트에서 다른 값이 있는 경우 이 차원은 데이터를 수집하지 않습니다.

AppMeasurement를 사용하여 데이터를 이 차원으로 보내려면:

* 원하는 값으로 [`linkName`](/help/implement/vars/config-vars/linkname.md) 변수를 채웁니다.
* Set the [`linkType`](/help/implement/vars/config-vars/linktype.md) variable to `"d"`.
* 이미지 [`tl()`](/help/implement/vars/functions/tl-method.md) 요청 전송

## 차원 값

이 변수는 구현의 사용자 지정 문자열을 기반으로 하므로 조직에서 차원 값이 무엇인지 결정합니다. 보고 요구 사항에 따라 링크를 의미 있는 카테고리로 그룹화하는 것이 좋습니다.
