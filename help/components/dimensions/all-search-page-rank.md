---
title: 모든 검색 페이지 등급
description: 방문자가 사이트를 통해 클릭한 검색 엔진의 페이지를 결정합니다.
translation-type: tm+mt
source-git-commit: 4a7b3a00bdbf557c219de530e3e692c2b2db4a84
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# 모든 검색 페이지 등급

&#39;모든 검색 페이지 등급&#39; 차원은 방문자가 사이트를 통해 클릭한 검색 결과 페이지에 대한 통찰력을 제공합니다. 예를 들어, 사이트가 검색 엔진 검색 결과의 두 번째 페이지에 나타나는 경우 이 변수의 차원 값은 &quot;검색 페이지 2&quot;입니다.

## 데이터로 이 차원 채우기

이 차원을 작동하려면 보고서 세트에 내부 URL 필터가 [](/help/admin/admin/internal-url-filter-admin.md) 올바르게 설정되어 있어야 합니다. AppMeasurement는 구현 코드를 변경하지 않고 자동으로 이 차원을 채웁니다.

## 차원 값

방문자가 검색 엔진에서 사이트를 클릭스루하는 경우 이 차원의 값은 &quot;검색 페이지&quot; 뒤에 클릭한 페이지 번호가 옵니다. 히트가 검색 엔진에서 발생하지 않으면 이 차원의 값은 &quot;지정되지 않음&quot;입니다.
