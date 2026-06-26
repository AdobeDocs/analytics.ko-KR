---
title: Data Warehouse의 구성 요소 지원
description: Data Warehouse 요청을 작성할 때 사용할 수 있는 차원 및 지표, 사용할 수 없는 차원 및 동작 방식을 알아봅니다.
feature: Data Warehouse
exl-id: ce7411a4-a720-47b7-90d5-4d867eff4bae
TQID: https://experienceleague.adobe.com/NhSEyPN3093B9M0SngJluJdZScI2lXvRyHkXQd8gg-4
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
subfeature_v2:
  - id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: d4db20e3498d54162806b3fdef0b34f45c93a6ff
workflow-type: tm+mt
source-wordcount: 362
ht-degree: 11%

---

# Data Warehouse의 구성 요소 지원

이 페이지에서는 Data Warehouse 요청을 작성할 때 사용할 수 있는 차원 및 지표에 대해 설명합니다. 섹션에는 사용 가능한 구성 요소, 사용할 수 없는 구성 요소 및 다른 Adobe Analytics 도구에서와 다르게 작동하는 구성 요소가 포함됩니다.

## Data Warehouse 전용 차원

다음 차원은 Data Warehouse에서 사용할 수 있지만 다른 Adobe Analytics 기능에서는 사용할 수 없습니다.

* [[!UICONTROL Experience Cloud 방문자 ID]](/help/components/dimensions/experience-cloud-visitor-id.md)
* [[!UICONTROL IP 주소]](/help/components/dimensions/ip-address.md)
* [[!UICONTROL 페이지 URL]](/help/components/dimensions/page-url.md)
* [[!UICONTROL 구매 ID]](/help/components/dimensions/purchase-id.md)
* [[!UICONTROL 방문자 ID]](/help/components/dimensions/visitor-id.md)

## 차원이 지원되지 않음

Data Warehouse 보고서 또는 세그먼트에서는 다음 차원을 사용할 수 없습니다.

* [[!UICONTROL 오전/오후]](/help/components/dimensions/am-pm.md)
* 허용되는 [[!UICONTROL 시작 페이지]](/help/components/dimensions/entry-dimensions.md) 및 [[!UICONTROL 원래 시작 페이지]](/help/components/dimensions/entry-dimensions.md)을 제외한 모든 시작 차원
* 허용되는 [[!UICONTROL 종료 페이지]](/help/components/dimensions/exit-dimensions.md) 및 [[!UICONTROL 종료 링크]](/help/components/dimensions/exit-link.md)를 제외한 모든 종료 차원
* [[!UICONTROL 히트 깊이]](/help/components/dimensions/hit-depth.md)
* [[!UICONTROL 반환 빈도]](/help/components/dimensions/return-frequency.md)
* [[!UICONTROL 이벤트까지 남은 시간]](/help/components/dimensions/time-prior-to-event.md)
* [[!UICONTROL 페이지 체류 시간 - 그룹화됨]](/help/components/dimensions/time-spent-on-page.md)
* [[!UICONTROL 방문당 체류 시간 - 그룹화됨]](/help/components/dimensions/time-spent-per-visit.md)
* [[!UICONTROL 모든 검색 페이지 등급]](/help/components/dimensions/all-search-page-rank.md)
* [[!UICONTROL 계층]](/help/components/dimensions/overview.md#retired-dimensions) 변수
* [[!UICONTROL 히트 유형]](/help/components/dimensions/hit-type.md)
* [[!UICONTROL 유료 검색]](/help/components/dimensions/paid-search.md)
* [[!UICONTROL 단일 페이지 방문 횟수]](/help/components/dimensions/single-page-visits.md)
* [[!UICONTROL 옵트아웃 이유 추적]](/help/components/dimensions/tracking-opt-out-reason.md)
* [[!UICONTROL 미국 주]](/help/components/dimensions/us-states.md)

일부 차원은 Data Warehouse 요청에서 사용할 수 있지만 세그먼트 내에서 사용할 수는 없습니다. 자세한 내용은 [Data Warehouse 세그먼트 호환성](segment-compatibility.md)을 참조하십시오.

## 비표준 날짜 서식이 있는 차원

Data Warehouse 보고서에서는 다음 시간 기반 차원이 지원되지만 출력은 비표준 형식을 사용합니다.

* [[!UICONTROL 년]](/help/components/dimensions/year.md)
* [[!UICONTROL 분기]](/help/components/dimensions/quarter.md)
* [[!UICONTROL 월]](/help/components/dimensions/month.md)
* [[!UICONTROL 주]](/help/components/dimensions/week.md)
* [[!UICONTROL 일]](/help/components/dimensions/day.md)
* [[!UICONTROL 시간]](/help/components/dimensions/hour.md)
* [[!UICONTROL 분]](/help/components/dimensions/minute.md)

날짜 값이 `1YYMMDDHHMM` 형식으로 출력됩니다.

* **연도(YY)**: 1900까지 오프셋합니다. 처음 세 자리 숫자에 `1900`을(를) 추가합니다. 예를 들어 `125` = **2025**&#x200B;입니다.
* **개월**: 0부터 시작. 1월 = `00`, 2월 = `01`, ..., 12월 = `11`.

예를 들어 날짜 범위 주 필드에 `1260901`이(가) 표시되면 연도는 1900 + 126 = **2026**&#x200B;이고 월은 09 = **10월**&#x200B;입니다.

## Data Warehouse에서 다르게 정의된 지표

* **[[!UICONTROL 방문 횟수]](/help/components/metrics/visits.md)**: 다른 Adobe Analytics 도구의 방문 횟수 지표와 달리 영구적이지 않은 쿠키 방문 횟수를 제외합니다.
* **[[!UICONTROL 방문 횟수 - 모든 방문자 수]](/help/components/metrics/visits.md)**: 지속되지 않는 쿠키가 있는 방문자를 포함하여 모든 방문자를 계산하여 Adobe Analytics의 다른 곳에서 사용되는 표준 [!UICONTROL 방문 횟수] 지표와 거의 비슷하게 만듭니다.

## 지표가 지원되지 않음

Data Warehouse에서는 다음 지표를 사용할 수 없습니다.

* [[!UICONTROL 바운스]](/help/components/metrics/bounces.md)
* [[!UICONTROL 진입]](/help/components/metrics/entries.md)
* [[!UICONTROL 종료]](/help/components/metrics/exits.md)
* [[!UICONTROL 다시 로드]](/help/components/metrics/reloads.md)
* [[!UICONTROL 단일 액세스]](/help/components/metrics/single-access.md)
* 모든 [[!UICONTROL 체류 시간]](/help/components/metrics/time-spent.md) 지표
* [기여도](/help/components/calculated-metrics/workflow/c-build-metrics/participation-metric.md) 속성 모델을 사용하는 모든 지표
