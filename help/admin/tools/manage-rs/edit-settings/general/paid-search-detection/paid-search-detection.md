---
description: 유료 검색 감지는 검색 엔진 및 검색 키워드 보고서에서 유료 검색과 자연어 검색을 구별합니다.
title: 유료 검색 감지
feature: Admin Tools
exl-id: 6b513ad2-f955-4a34-92f8-57a141e44801
TQID: 'https://experienceleague.adobe.com/g26-86nQZ-k3kaID-Dq6qbwYkdqLpHDdUEswP-p361Y'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: ff9b434a-2221-4df7-81d1-5bcbf5f80bce
subfeature_v2:
  - id: fab61dd8-112a-4e5e-ad5f-fb0240b7a60b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 38cd05960c27b0bec0a713cb833907f4a658013e
workflow-type: tm+mt
source-wordcount: 187
ht-degree: 87%

---

# 유료 검색 감지

[!UICONTROL 유료 검색 감지는 검색 엔진 및 검색 키워드 보고서에서 유료 검색과 자연어 검색을 구별합니다. &#x200B;] 유료 광고를 사용할 검색 엔진을 지정하고 유료 광고에서 방문 URL에 있는 문자열을 지정할 수 있습니다.

## 구성 옵션 {#configuration}

다음 테이블에서는 [유료 검색 감지를 구성](/help/admin/tools/manage-rs/edit-settings/general/paid-search-detection/t-paid-search-detection.md)하는 데 사용하는 필드 및 옵션에 대해 설명합니다.

| 옵션 | 설명 |
| --- | --- |
| [!UICONTROL 검색 엔진] | 드롭다운 목록에서 검색 엔진을 선택합니다. 검색 엔진마다 다른 쿼리 문자열 매개 변수를 사용하는 경우 엔진을 지정합니다. 일반적으로는 `Any` 값으로 충분합니다. |
| [!UICONTROL 쿼리 문자열] | “?” 뒤의 URL 부분인 쿼리 문자열 매개 변수의 모든 부분과 일치하는 대소문자를 구분하는 문자열을 지정합니다. <br>**참고**: [!UICONTROL 유료 검색 감지]는 대소문자를 구분합니다. 예를 들어 쿼리 문자열 매개 변수로 “PID”를 지정하는 규칙은 “pid”와 일치하지 않습니다. 조직에서 대/소문자를 혼용하는 경우는 원하는 쿼리 문자열 매개 변수를 모두 찾을 수 있도록 정확한 값을 별도의 규칙으로 배치합니다. |
