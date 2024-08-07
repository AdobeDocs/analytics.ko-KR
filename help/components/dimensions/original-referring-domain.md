---
title: 최초 참조 도메인
description: 방문자가 사이트를 클릭스루하기 전에 있었던 첫 번째 참조 도메인입니다.
feature: Dimensions
exl-id: 6b9ac662-a79a-477b-8612-7980da7cfadd
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 95%

---

# 최초 참조 도메인

&#39;원래 참조 도메인&#39; [차원](overview.md)은(는) 방문자가 사이트에 도달하기 위해 클릭했던 첫 번째 참조 도메인을 보고합니다. 설정되면 해당 방문자 ID의 전체 라이프타임 동안 동일한 값을 포함합니다. 이 차원은 처음에 사이트로 트래픽을 유도하는 서드파티 사이트를 아는 데 유용합니다.

>[!IMPORTANT]
>
>이 차원을 사용하려면 보고서 세트의 [내부 URL 필터](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md)를 구성해야 합니다. 내부 URL 필터를 구성하지 않으면 내부 도메인이 포함되거나 외부 도메인이 표시되지 않을 수 있습니다.

## 이 차원을 데이터로 채우기

이 차원을 사용하려면 Analytics 인터페이스와 구현 모두에서 구성해야 합니다.

* 구현 내에서 이 차원은 이미지 요청의 [`r` 쿼리 문자열](/help/implement/validate/query-parameters.md)에서 데이터를 검색합니다. AppMeasurement는 브라우저에서 JavaScript 변수 `document.referrer`를 사용하여 이 데이터를 수집합니다. AppMeasurement 라이브러리를 사용하는 경우(Adobe Experience Platform의 태그 등을 통해) 이 차원은 즉시 작동합니다. AppMeasurement 외부의 데이터 수집 방법을 사용하는 경우 (API 등을 통해)에는 이미지 요청에 `r` 쿼리 문자열 매개 변수를 포함해야 합니다.
* Analytics 인터페이스 내에서는 보고서 세트의 [내부 URL 필터](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md)를 구성해야 합니다. 내부 URL 필터를 구성하지 않으면 내부 도메인이 포함되거나 외부 도메인이 표시되지 않을 수 있습니다.

Adobe에서는 방문자 라이프타임 동안 최초 참조 도메인을 유지합니다. 방문자가 언제든지 나가서 다른 도메인의 링크를 클릭하는 경우 새 값이 기록되지 않습니다. 새 값을 보려면 [참조 도메인](referring-domain.md)을 참조하십시오.

## 차원 항목

차원 항목에는 방문자가 사이트를 클릭스루하는 도메인이 포함됩니다. 히트에 (설정되었거나 유지된) 레퍼러 데이터가 없으면 이 히트는 차원 항목 `"None"` 아래에 그룹화됩니다. 이 차원 항목은 방문자가 수동으로 브라우저 주소를 주소 표시줄에 입력하거나 책갈피를 클릭하는 등의 경우와 같이 레퍼러 값이 없음을 의미합니다.

## 참조 도메인과 최초 참조 도메인 비교

참조 도메인은 방문에 따라 달라질 수 있습니다. 예를 들어 방문자가 `google.com`을 통해 사용자의 사이트로 도착하고 1주일 후 `twitter.com`을 통해 사용자의 사이트에 도착합니다. 결국 이 방문자는 사용자의 사이트에서 구매를 합니다. 참조 도메인을 마지막 터치 속성이 있는 차원으로 사용하는 경우 `twitter.com`이 구매에 대한 크레딧을 받습니다. 최초 참조 도메인을 차원으로 사용하는 경우 속성 모델에 관계없이 `google.com`이 구매에 대한 크레딧을 받습니다.

최초 참조 도메인은 주어진 방문자 ID의 전체 라이프타임 동안 변경되지 않습니다.
