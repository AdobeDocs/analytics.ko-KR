---
description: 유료 검색 감지는 검색 엔진 및 검색 키워드 보고서에서 유료 검색과 자연어 검색을 구별합니다.
title: 유료 검색 감지
feature: Admin Tools
exl-id: 6b513ad2-f955-4a34-92f8-57a141e44801
source-git-commit: def7d071de1765acf524a638a8f8d13ae69e1a1f
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 100%

---

# 유료 검색 감지

[!UICONTROL 유료 검색 감지는 검색 엔진 및 검색 키워드 보고서에서 유료 검색과 자연어 검색을 구별합니다. ] 유료 광고를 사용할 검색 엔진을 지정하고 유료 광고에서 방문 URL에 있는 문자열을 지정할 수 있습니다.

## 구성 옵션 {#configuration}

다음 표에서는 [유료 검색 감지를 구성](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/t-paid-search-detection.md)하는 데 사용하는 필드 및 옵션에 대해 설명합니다.

| 옵션 | 설명 |
| --- | --- |
| [!UICONTROL 검색 엔진] | 드롭다운 목록에서 검색 엔진을 선택합니다. 검색 엔진에 따라 다른 쿼리 문자열 매개 변수를 사용하는 경우는 엔진을 지정합니다. 일반적으로는 `Any` 값으로 충분합니다. |
| [!UICONTROL 쿼리 문자열] | “?” 뒤의 URL 부분인 쿼리 문자열 매개 변수의 모든 부분과 일치하는 대소문자를 구분하는 문자열을 지정합니다. <br>**참고**: [!UICONTROL 유료 검색 감지]는 대소문자를 구분합니다. 예를 들어 쿼리 문자열 매개 변수로 “PID”를 지정하는 규칙은 “pid”와 일치하지 않습니다. 조직에서 대/소문자를 혼용하는 경우는 원하는 쿼리 문자열 매개 변수를 모두 찾을 수 있도록 정확한 값을 별도의 규칙으로 배치합니다. |
