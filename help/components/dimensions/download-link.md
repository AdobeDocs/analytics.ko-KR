---
title: 다운로드 링크
description: 다운로드 링크의 이름입니다.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '180'
ht-degree: 100%

---


# 다운로드 링크

다운로드 링크 차원은 사이트에 구현된 다운로드 링크의 이름을 보고합니다. 이 차원은 다음과 같이 다운로드 링크에 대한 방문자 행동에 대해 자세히 알고 싶을 때 중요합니다.

* 사이트에서 가장 자주 다운로드되는 파일을 확인합니다.
* 특정 기간에 더 자주 다운로드되는 파일이 있는지 확인합니다.
* 제공되는 경우 방문자가 다른 파일 유형을 다운로드하는지 확인합니다.

## 이 차원을 데이터로 채우기

이 차원은 `lnk_d` 값과 함께 `pe` 쿼리 문자열이 있는 히트의 이미지 요청에 있는 [`pev2` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 수집합니다. 히트에서 `pe` 쿼리 문자열에 다른 값이 있는 경우 이 차원은 데이터를 수집하지 않습니다.

AppMeasurement를 사용하여 데이터를 이 차원에 보내려면

* 원하는 값으로 [`linkName`](/help/implement/vars/config-vars/linkname.md) 변수를 채웁니다.
* [`linkType`](/help/implement/vars/config-vars/linktype.md) 변수를 `"d"`로 설정합니다.
* [`tl()`](/help/implement/vars/functions/tl-method.md) 이미지 요청을 보냅니다.

## 차원 항목

이 변수는 구현의 사용자 지정 문자열에 기반하므로 조직에서 차원 항목을 결정합니다. 보고 요구 사항에 따라 링크를 의미 있는 카테고리로 그룹화하는 것이 좋습니다.
