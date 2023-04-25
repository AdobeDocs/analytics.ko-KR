---
description: Adobe은 사용할 수 있는 다양한 계산된 지표를 제공합니다. 이 페이지에는 해당 지표와 의도한 사용 목록이 표시됩니다.
title: 기본 계산된 지표
feature: Calculated Metrics
exl-id: 84468e63-f967-41cd-8084-525b1b90957a
source-git-commit: 61a0292bf2f8ff22b414c2e91da476c1da69d163
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 51%

---

# 기본 계산된 지표

Adobe Analytics은 가장 일반적인 사용 사례를 다루는 다양한 계산된 지표를 제공합니다. 이러한 계산된 지표는 Analysis Workspace에서 기본적으로 사용할 수 있습니다.

다음은 Adobe에서 제공하는 각 계산된 지표의 목록이며, 그 의도한 함수와 이를 계산하는 데 사용되는 기본 공식이 있습니다.

>[!NOTE]
>
>이 페이지에 설명된 기본 계산된 지표 외에도 보고서 세트에 계산된 지표를 추가할 수도 있습니다.
>
>:
> * 에 설명된 대로 스트리밍 미디어에 대한 기본 계산된 지표를 추가합니다. [계산된 지표](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/variables/calculated-metrics.html)
> * 에 설명된 대로 기존 지표에서 사용자 지정 계산된 지표를 만듭니다. [계산 및 고급 계산(파생) 지표](/help/components/c-calcmetrics/cm-overview.md).



| 계산된 지표 이름 | 함수 | 공식 |
| --- | --- | --- |
| 획득 링크 클릭 수 | 사용자가 사이트로 트래픽을 유도하도록 설계된 링크를 클릭한 횟수. | `[Campaign Click-throughs]` |
| 작업 | 앱에서 수행된 총 작업 수 | `[Has an Action] (segment)`<br>`[Custom Link Instances] (metric)` |
| 앱 사용자 | 모바일 앱을 사용하는 총 사용자 수 | `[Mobile App Users] (segment)`<br>`[Unique Visitors] (metric)` |
| 평균 세션 길이(모바일) | 방문자가 단일 세션 동안 사이트에서 보내는 평균 시간입니다. | 빈 |
| 사이트의 평균 시간 | 방문자가 사이트를 떠나거나 탐색하기 전에 사이트에서 보내는 평균 시간입니다. | `[Average Time Spent on Site (Seconds)]` |
| 바운스 비율 | 해당 페이지의 방문 수와 비교하여 정확히 하나의 히트가 포함된 방문의 비율입니다. 이 지표는 바운스 비율이 가장 높은 차원 항목을 이해하거나 시간에 따른 사이트의 총 바운스 비율 집계를 보는 데 도움이 될 수 있습니다. | `[Bounces] / [Entries]` |
| 보트 페이지 보기 비율 | 총 페이지 보기 수와 비교한 보트 페이지 보기 수입니다. | `[Bot Page Views] / [Page Views]` |
| 콘텐츠 속도 | 새 콘텐츠가 제작되고 사이트에 게시되는 속도와 이러한 콘텐츠에서 사용자 참여가 발생하는 속도. | `[Page Views] / [Visits]` |
| 전환율 | 구매와 같이 원하는 작업을 수행한 방문자의 비율. | `[Orders] / [Visits]` |
| 시작 비율 | 사이트의 총 세션 수와 비교하여 주어진 페이지에서 사이트에 들어온 방문자의 비율. | `[Entries] / [Visits]` |
| 예상 고유 방문자 수(ITP 2.1) | ITP 방문자(Safari 브라우저의 사용자)의 경우 고유 방문자 수를 2 이하로 나눕니다. 이 계산된 지표는 사용자가 클라이언트측 JavaScript를 사용하여 쿠키를 설정한다고 가정합니다(CNAME 구현을 사용하지 않음). 클라이언트측 JavaScript를 사용하여 쿠키를 설정하는 구현은 ITP 2.1부터 영향을 받았습니다. [지능형 추적 방지](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) 자세한 내용 | `[Unique Visitors (metric) with ITP Visitors (ITP 2.1, Non-CNAME implementations) segment] / [Unique Visitors metric + Non-ITP Visitors (ITP 2.1, Non-CNAME implementations) segment]` |
| Experience Cloud ID 범위 | Experience Cloud ID를 보유한 방문자의 비율. | `[Visitors with Experience Cloud ID] / [Unique Visitors]` |
| 종료 비율 | 특정 페이지를 본 후 사이트를 떠나는 방문자의 비율. | `[Exits] / [Visits]` |
| ITP 2.1 고유 방문자 / 고유 방문자 수 | ITP 2.1 쿠키 제한 사항의 영향을 받는 브라우저를 사용하는 고유 방문자의 비율입니다. | `[Unique Visitors metric with ITP Visitors segment] / [Unique Visitors]` |
| 지원 주문 | 채널 또는 소스가 고객의 구매 여정에 기여했지만 최종 구매로는 이어지지 않은 횟수. | `[Orders (Visit Participation)] - [Orders]` |
| 주문 수/방문 수 | 거래가 완료된 사이트 방문 비율. | `[Orders] / [Visits]` |
| 주문 수/방문자 수 | 사이트의 개별 방문자가 생성한 평균 주문 또는 거래 횟수 | `[Orders] / [Unique Visitors]` |
| 페이지 조회수 / 예상되는 고유 방문자 (ITP 2.1) | 예상되는 고유 방문자(ITP 2.1)가 조회한 평균 페이지 수. | `[Unique Visitors (metric) with ITP Visitors (ITP 2.1, Non-CNAME implementations) segment] / [Unique Visitors (metric) with Non-ITP Visitors (ITP 2.1, Non-CNAME implementations) segment]` |
| 페이지 보기 수/고유 방문자 수 | 사이트의 각 고유 방문자가 조회한 평균 페이지 수. | `[Page Views] / [Unique Visitors]` |
| 페이지 조회수/방문 수 | 사용자가 사이트를 한 번 방문하는 동안 본 평균 페이지 수. | `[Page Views] / [Visits]` |
| 페이지 속도 | 한 컨텐츠가 생성하는 추가 페이지 보기 수입니다. 이 지표는 추가 참여를 유도하는 콘텐츠를 결정하는 데 도움이 될 수 있습니다. | `[Page Views] / [Visits]` |
| 다시 로드 / 페이지 보기 횟수 | 페이지 다시 로드 또는 새로 고침으로 이어진 페이지 조회수의 비율. | `[Reloads] / [Page Views]` |
| 수입/주문 | 사이트에서 완료된 각 거래 또는 주문에 의해 생성된 평균 매출. | `[Revenue] / [Orders]` |
| 수입/방문 횟수 | 사이트 1회 방문으로 생성된 평균 매출. | `[Revenue] / [Visits]` |
| 매출/방문자 | 사이트의 개별 방문자가 생성한 평균 매출. | `[Revenue] / [Unique Visitors]` |
| 상태 보기 | 앱의 다른 상태 또는 화면에 대한 보기 수 | `[Mobile App Users] (segment)`<br>`[Page Views] (metric)` |
| 체류 시간/사용자(상태) | 평균 방문자가 사이트에 있는 동안 특정 주에서 보내는 시간 | `[Mobile App Users] (segment)`<br>`[Time Spent per Visitor (Seconds)] (metric)` |
| 7일 후 재방문하는 고유 방문자/고유 방문자 | 7일 이상의 기간 후에 돌아오는 고유 방문자 비율. | `[Unique Visitors metric with Users returning after 7 days segment] / [Unique Visitors]` |
| 사용자(모바일) | 모바일 앱을 사용하는 총 사용자 수 | `[Mobile App Users] (segment)`<br>`[Unique Visitors] (metric)` |
| 방문 횟수/방문자 | 고유 방문자의 평균 사이트 조회 수. | `[Visits] / [Unique Visitors]` |
| 가중 바운스 비율 | 함수 | `IF([Visits] > PERCENTILE([Visits]), [Bounce Rate], 0)` |

{style="table-layout:auto"}
