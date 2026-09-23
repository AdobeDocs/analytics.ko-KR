---
title: 검색 키워드
description: 방문자가 사이트에 도달하기 위해 사용한 검색 키워드입니다.
feature: Dimensions
exl-id: 5a1236a6-f94b-4679-906a-b539afe36887
TQID: https://experienceleague.adobe.com/4naavrC42ddsxGFJfkOJ0wzHLTa7tdMeI9nKDgVWrBY
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
subfeature_v2:
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
    internal-label: Calculated Metrics
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 4516f6de27be12a2ae2fafe4e06d724f4a89fb83
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 70%
---
# 검색 키워드

&#39;검색 키워드&#39; [차원](overview.md)은(는) 방문자가 사이트에 도달하기 위해 사용하는 검색 키워드를 보고합니다.

>[!IMPORTANT]
>
>개인 정보 보호 정책이 강화됨에 따라 대부분의 검색 엔진이 더 이상 검색 키워드를 전달하지 않습니다. Adobe가 검색 엔진을 인식하지만 차원 항목 `"Keyword unavailable"` 아래에 키워드 그룹이 없는 히트입니다.

레퍼러는 다음 두 항목을 모두 충족해야 검색 키워드로 분류할 수 있습니다.

* 참조 도메인이 Adobe에 의해 유효한 [검색 엔진](search-engine.md)으로 인식됩니다.
* 키워드 쿼리 문자열 매개변수가 레퍼러 URL에 있습니다. 키워드 쿼리 문자열이 존재하지만 값을 포함하지 않으면 차원 항목 `"Keyword unavailable"` 아래에 그룹화됩니다.

유료 검색과 자연어 검색을 구분하려면 [유료 검색 감지](/help/admin/tools/manage-rs/edit-settings/general/paid-search-detection/paid-search-detection.md)가 필요합니다. 검색 키워드에 사용할 수 있는 여러 차원이 있습니다.

* **검색 키워드**: 유료 검색인지 또는 자연어 검색인지에 상관없이 사이트에 도달하기 위해 사용되는 검색 키워드입니다.
* **검색 키워드 - 유료**: 사이트에 도달하기 위해 사용된 검색 키워드로서 유료 검색 감지와 일치합니다.
* **검색 키워드 - 자연어**: 사이트에 도달하기 위해 사용된 검색 키워드로서 유료 검색 감지와 일치하지 않습니다.

## 이 차원을 데이터로 채우기

Adobe은 각 히트의 검색 엔진 [레퍼러](referrer.md)에서 이 차원을 파생하여 레퍼러의 쿼리 문자열에서 키워드를 추출합니다. 설정할 변수가 없습니다. 각 값은 레퍼러에 따라 다르므로 레퍼러 차원과 [내부 URL 필터](/help/admin/tools/manage-rs/edit-settings/general/internal-url-filter-admin.md)가 올바르게 구성되어 있는지 확인하십시오.

| 속성 | 값 |
| --- | --- |
| **AppMeasurement 변수** | 없음(검색 엔진 레퍼러에서 파생) |
| **웹 SDK/XDM 필드** | 없음(검색 엔진 레퍼러에서 파생) |
| **쿼리 매개 변수** | 해당 없음 |
| **XML 태그** | 해당 없음 |
| **바이트 제한** | 해당 없음 |
| **지속성** | 해당 사항 없음 |

## 차원 항목

차원 항목에는 사이트에 도달하기 위해 사용되는 검색 키워드가 포함됩니다. `"Unspecified"` 차원 항목은 모든 비검색 트래픽입니다.
