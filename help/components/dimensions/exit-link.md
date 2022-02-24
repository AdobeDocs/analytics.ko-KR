---
title: 종료 링크
description: 종료 링크의 이름입니다.
feature: Dimensions
exl-id: 090d5fee-4b35-4be7-866c-5ef1d1c4c0a6
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '156'
ht-degree: 100%

---

# 종료 링크

종료 링크 차원은 사이트에 구현된 종료 링크의 이름을 보고합니다. 이 차원은 사이트 외부의 도메인을 가리키는 가장 인기 있는 링크를 이해하려 할 때 유용합니다.

## 이 차원을 데이터로 채우기

이 차원은 `lnk_e` 값과 함께 `pe` 쿼리 문자열이 있는 히트의 이미지 요청에 있는 [`pev2` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 수집합니다. 히트에서 `pe` 쿼리 문자열에 다른 값이 있는 경우 이 차원은 데이터를 수집하지 않습니다.

AppMeasurement를 사용하여 데이터를 이 차원으로 보내려면 `"e"`의 링크 유형 인수로 [`tl()`](/help/implement/vars/functions/tl-method.md) 이미지 요청을 보냅니다. 링크 이름 인수를 원하는 값으로 채웁니다.

## 차원 항목

이 변수는 구현의 사용자 지정 문자열에 기반하므로 조직에서 차원 항목을 결정합니다. 보고 요구 사항에 따라 링크를 의미 있는 카테고리로 그룹화하는 것이 좋습니다.
