---
title: 모든 검색 페이지 등급
description: 방문자가 사이트에 도달하기 위해 클릭한 검색 엔진의 페이지를 결정합니다.
translation-type: ht
source-git-commit: cd2225ec00190af6b616f313b419935c4f8dfafd
workflow-type: ht
source-wordcount: '145'
ht-degree: 100%

---


# 모든 검색 페이지 등급

모든 검색 페이지 등급 차원은 방문자가 사이트에 도달하기 위해 클릭한 검색 결과 페이지에 대한 통찰력을 제공합니다. 예를 들어, 사이트가 검색 엔진의 검색 결과 중 두 번째 페이지에 나타나는 경우 이 변수의 차원 항목은 &quot;검색 페이지 2&quot;입니다.

## 이 차원을 데이터로 채우기

이 차원이 작동하려면 보고서 세트에 [내부 URL 필터](/help/admin/admin/internal-url-filter-admin.md)가 올바로 설정되어 있어야 합니다. AppMeasurement는 구현 코드를 변경하지 않고 자동으로 이 차원을 채웁니다.

## 차원 항목

방문자가 검색 엔진에서 사이트까지 클릭하여 도달하는 경우 이 차원의 값은 &quot;검색 페이지&quot; 다음에 클릭한 페이지 번호가 옵니다. 검색 엔진에서 히트가 발생하지 않으면 이 차원의 값은 &quot;지정되지 않음&quot;입니다.
