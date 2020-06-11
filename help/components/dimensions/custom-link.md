---
title: 사용자 지정 링크
description: 사용자 지정 링크의 이름입니다.
translation-type: tm+mt
source-git-commit: c9e696201d0e9ec97dcdd6ff797ca72244dcf366
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---


# 사용자 지정 링크

&#39;사용자 지정 링크&#39; 차원은 사이트에 구현된 사용자 지정 링크의 이름을 보고합니다. 이 차원은 방문자가 가장 많이 클릭하는 링크 유형을 이해하려는 경우 유용합니다.

## 데이터로 이 차원 채우기

이 차원은 값이 있는 [`pev2` 쿼리 문자열도 포함하는 히트의 이미지 요청에 있는](/help/implement/validate/query-parameters.md) 쿼리 문자열 `pe` 데이터로부터 `lnk_o`수집합니다. 쿼리 문자열에 `pe` 히트에서 다른 값이 있는 경우 이 차원은 데이터를 수집하지 않습니다.

AppMeasurement를 사용하여 데이터를 이 차원으로 보내려면:

* 원하는 값으로 [`linkName`](/help/implement/vars/config-vars/linkname.md) 변수를 채웁니다.
* Set the [`linkType`](/help/implement/vars/config-vars/linktype.md) variable to `"o"`.
* 이미지 [`tl()`](/help/implement/vars/functions/tl-method.md) 요청 전송

## 차원 값

이 변수는 구현의 사용자 지정 문자열을 기반으로 하므로 조직에서 차원 값이 무엇인지 결정합니다. 보고 요구 사항에 따라 링크를 의미 있는 카테고리로 그룹화하는 것이 좋습니다.
