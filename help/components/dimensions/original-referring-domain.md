---
title: 원래 참조 도메인
description: 사이트를 클릭스루하기 전에 방문자가 있었던 첫 번째 참조 도메인입니다.
translation-type: tm+mt
source-git-commit: 7c722e361978a3d7517e95c23442b703e7e25270
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---


# 원래 참조 도메인

&#39;원래 참조 도메인&#39; 차원은 방문자가 사이트에 도달하기 위해 클릭했던 첫 번째 참조 도메인을 보고합니다. 설정되면 해당 방문자 ID의 전체 라이프타임에 대해 동일한 값이 포함됩니다. 이 차원은 원래 사이트로 트래픽을 유도하는 타사 사이트를 이해하는 데 유용합니다.

>[!IMPORTANT]
>
>이 차원을 사용하려면 보고서 세트의 [내부 URL 필터를](/help/admin/admin/internal-url-filter-admin.md) 구성해야 합니다. 내부 URL 필터를 구성하지 않으면 내부 도메인을 포함하거나 외부 도메인이 표시되지 않을 수 있습니다.

## 데이터로 이 차원 채우기

이 차원에서는 Analytics 인터페이스와 구현에 구성이 필요합니다.

* 구현 내에서 이 차원은 이미지 요청의 [`r` 쿼리 문자열에서](/help/implement/validate/query-parameters.md) 데이터를 검색합니다. AppMeasurement는 브라우저에서 JavaScript 변수를 사용하여 이 데이터 `document.referrer` 를 수집합니다. AppMeasurement 라이브러리(예: Adobe Experience Platform Launch을 통해)를 사용하는 경우 이 차원은 기본적으로 작동합니다. API를 통해 AppMeasurement 외부에 데이터 수집 메서드를 사용하는 경우 이미지 요청에 `r` 쿼리 문자열 매개 변수를 포함해야 합니다.
* Analytics 인터페이스 내에서 보고서 세트의 [내부 URL 필터를 구성해야 합니다](/help/admin/admin/internal-url-filter-admin.md). 내부 URL 필터를 구성하지 않으면 내부 도메인을 포함하거나 외부 도메인이 표시되지 않을 수 있습니다.

Adobe은 방문자 라이프타임을 위한 원래 참조 도메인을 유지합니다. 방문자가 언제든지 다른 도메인의 링크를 클릭하여 나가는 경우 새 값이 기록되지 않습니다. 새 값을 보려면 참조 [도메인을 참조하십시오](referring-domain.md).

## Dimension 항목

Dimension 항목에는 방문자가 사이트를 클릭스루하는 도메인이 포함됩니다. 히트에 레퍼러 데이터(설정되거나 지속된)가 없으면 차원 항목 아래에 그룹화됩니다 `"None"`. 이 차원 항목은 방문자가 브라우저 주소를 주소 표시줄에 수동으로 입력하거나 책갈피를 클릭하는 경우와 같이 레퍼러 값이 없음을 의미합니다.

## 참조 도메인과 원본 참조 도메인 비교

참조 도메인은 방문 간에 변경될 수 있습니다. 예를 들어 방문자가 사이트로 도착한 후 1주일 후 `google.com`에 사이트를 통해 사이트에 도착합니다 `twitter.com`. 결국 사이트에서 구매하게 됩니다. 마지막 터치 속성이 있는 차원으로 참조 도메인을 사용하는 경우 구매에 대한 크레디트를 `twitter.com` 받습니다. 원래 참조 도메인을 차원으로 사용하는 경우 기여도 모델에 관계없이 구매에 대한 크레딧을 `google.com` 받습니다.

원래 참조 도메인은 지정된 방문자 ID의 전체 라이프타임에 대해 변경되지 않습니다.
