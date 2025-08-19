---
description: Adobe는 다양한 계산된 지표를 사용할 수 있도록 제공합니다. 이 페이지에는 해당 지표와 그 용도가 나열되어 있습니다.
title: 기본 계산된 지표
feature: Calculated Metrics
exl-id: 84468e63-f967-41cd-8084-525b1b90957a
source-git-commit: 7609ecb3c34fb0bc8293fc1ecd409cfabb327295
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 98%

---

# 기본 계산된 지표

Adobe Analytics는 가장 일반적인 사용 사례를 다루기 위해 다양한 계산된 지표를 제공합니다. 이러한 계산된 지표는 기본적으로 Analysis Workspace에서 사용할 수 있습니다.

다음은 Adobe에서 제공하는 각 계산된 지표의 목록이며, 해당 지표의 의도된 기능과 이를 계산하는 데 사용되는 기본 공식입니다.

>[!NOTE]
>
>이 페이지에 설명된 기본 계산된 지표 외에도 보고서 세트에 추가 계산된 지표를 추가할 수 있습니다.
>
>다음과 같은 작업을 수행할 수 있습니다.
>
> * [계산된 지표](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/variables/calculated-metrics.html)에 설명된 대로 스트리밍 미디어 서비스에 대한 기본 계산된 지표를 추가합니다.
> * [계산 및 고급 계산 지표](/help/components/c-calcmetrics/cm-overview.md)에 설명된 대로 기존 지표에서 사용자 정의 계산된 지표를 생성합니다.
>

>[!TIP]
>
>[데이터 사전](/help/analyze/analysis-workspace/components/data-dictionary/data-dictionary-overview.md)을 사용하여 기본 계산된 지표의 정의와 해당 정의를 구성하는 개별 구성 요소를 보다 자세히 조사합니다.
>



| 계산된 지표 이름 | 함수 | 공식 |
| --- | --- | --- |
| 확보 링크 클릭 | 사용자가 사이트로 트래픽을 유도하도록 설계된 링크를 클릭한 횟수. | `[Campaign Click-throughs]` |
| 액션 | 앱에서 수행된 총 액션 수 | `[Has an Action] (segment)`<br>`[Custom Link Instances] (metric)` |
| 앱 사용자 | 모바일 앱을 사용하는 총 사용자 수 | `[Mobile App Users] (segment)`<br>`[Unique Visitors] (metric)` |
| 평균 세션 길이 (모바일) | 방문자가 단일 세션 동안 사이트를 이용하는 평균 시간. | 빈 |
| 사이트에서 보낸 평균 시간 | 방문자가 사이트를 떠나거나 다른 곳으로 이동하기 전에 사이트를 이용한 평균 시간. | `[Average Time Spent on Site (Seconds)]` |
| 바운스 비율 | 해당 페이지의 방문 수와 비교하여 정확히 하나의 히트가 포함된 방문의 비율. 이 지표를 사용하여 바운스 비율이 가장 높은 차원 항목을 이해하거나 시간에 따른 사이트의 총 바운스 비율 집계를 볼 수 있습니다. | `[Bounces] / [Entries]` |
| 봇 페이지 조회수 비율 | 봇 페이지 조회수와 전체 페이지 조회수의 비율. | `[Bot Page Views] / [Page Views]` |
| 콘텐츠 속도 | 새 콘텐츠가 제작되고 사이트에 게시되는 속도와 이러한 콘텐츠에서 사용자 참여가 발생하는 속도. | `[Page Views] / [Visits]` |
| 전환율 | 구매와 같이 원하는 액션을 수행한 방문자의 비율. | `[Orders] / [Visits]` |
| 시작 비율 | 사이트의 총 세션 수와 비교하여 주어진 페이지에서 사이트에 들어온 방문자의 비율. | `[Entries] / [Visits]` |
| 예상되는 고유 방문자 (ITP 2.1) | ITP 방문자(Safari 브라우저 사용자)의 경우, 고유 방문자를 2명 이하로 나눕니다. 이 계산된 지표는 클라이언트측 JavaScript를 사용하여 쿠키를 설정한다고 가정합니다(CNAME 구현을 사용하지 않음). 클라이언트측 JavaScript를 사용하여 쿠키를 설정하는 구현은 ITP 2.1부터 영향을 받았습니다. 자세한 내용은 [지능형 추적 방지](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/)를 참조하십시오. | `[Unique Visitors (metric) with ITP Visitors (ITP 2.1, Non-CNAME implementations) segment] / [Unique Visitors metric + Non-ITP Visitors (ITP 2.1, Non-CNAME implementations) segment]` |
| Experience Cloud ID 범위 | Experience Cloud ID를 보유한 방문자의 비율. | `[Visitors with Experience Cloud ID] / [Unique Visitors]` |
| 이탈률 | 특정 페이지를 본 후 사이트를 떠나는 방문자의 비율. | `[Exits] / [Visits]` |
| ITP 2.1 고유 방문자 / 고유 방문자 | ITP 2.1 쿠키 제한의 영향을 받는 브라우저를 사용하는 고유 방문자의 비율. | `[Unique Visitors metric with ITP Visitors segment] / [Unique Visitors]` |
| 주문 지원 | 채널 또는 소스가 고객의 구매 여정에 기여했지만 최종 구매로는 이어지지 않은 횟수. | `[Orders (Visit Participation)] - [Orders]` |
| 주문 수 / 방문 수 | 거래가 완료된 사이트 방문 비율. | `[Orders] / [Visits]` |
| 주문 수 / 방문자 수 | 사이트의 개별 방문자가 생성한 평균 주문 또는 거래 횟수 | `[Orders] / [Unique Visitors]` |
| 페이지 조회수 / 예상되는 고유 방문자 (ITP 2.1) | 예상되는 고유 방문자(ITP 2.1)가 조회한 평균 페이지 수. | `[Unique Visitors (metric) with ITP Visitors (ITP 2.1, Non-CNAME implementations) segment] / [Unique Visitors (metric) with Non-ITP Visitors (ITP 2.1, Non-CNAME implementations) segment]` |
| 페이지 조회수 / 고유 방문자 수 | 사이트의 각 고유 방문자가 조회한 평균 페이지 수. | `[Page Views] / [Unique Visitors]` |
| 페이지 조회수 / 방문 수 | 사용자가 사이트를 한 번 방문하는 동안 본 평균 페이지 수. | `[Page Views] / [Visits]` |
| 페이지 속도 | 콘텐츠가 생성하는 추가 페이지 조회수. 이 지표는 추가 참여를 유도하는 콘텐츠를 결정하는 데 도움이 될 수 있습니다. | `[Page Views] / [Visits]` |
| 다시 로드 수 / 페이지 조회수 | 페이지 다시 로드 또는 새로 고침으로 이어진 페이지 조회수의 비율. | `[Reloads] / [Page Views]` |
| 매출 / 주문 수 | 사이트에서 완료된 각 거래 또는 주문에 의해 생성된 평균 매출. | `[Revenue] / [Orders]` |
| 매출 / 방문 수 | 사이트 1회 방문으로 생성된 평균 매출. | `[Revenue] / [Visits]` |
| 매출 / 방문자 수 | 사이트의 개별 방문자가 생성한 평균 매출. | `[Revenue] / [Unique Visitors]` |
| 상태 보기 수 | 앱의 다른 상태 또는 화면에 대한 조회수 | `[Mobile App Users] (segment)`<br>`[Page Views] (metric)` |
| 사용 시간/사용자 (상태) | 평균 방문자가 사이트에 있는 동안 특정 상태에서 보내는 시간 | `[Mobile App Users] (segment)`<br>`[Time Spent per Visitor (Seconds)] (metric)` |
| 고유 방문자 / 7일 후 돌아오는 고유 방문자 | 7일 이상의 기간 후에 돌아오는 고유 방문자 비율. | `[Unique Visitors metric with Users returning after 7 days segment] / [Unique Visitors]` |
| 사용자 (모바일) | 모바일 앱을 사용하는 총 사용자 수 | `[Mobile App Users] (segment)`<br>`[Unique Visitors] (metric)` |
| 방문 횟수 / 방문자 수 | 고유 방문자의 평균 사이트 조회 수. | `[Visits] / [Unique Visitors]` |
| 가중 바운스 비율 | 함수 | `IF([Visits] > PERCENTILE([Visits]), [Bounce Rate], 0)` |

{style="table-layout:auto"}
