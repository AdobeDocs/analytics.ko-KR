---
description: Adobe은 사용할 수 있는 다양한 계산된 지표를 제공합니다. 이 페이지에는 이러한 지표와 그 사용 용도가 나열됩니다.
title: 참조 기본 함수
feature: Calculated Metrics
exl-id: 1a49435c-96d1-4617-bd1a-a5d3b74e3ebd
source-git-commit: 2874ea66765e650a92bc39537d6a9eb8cebcd6a4
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 10%

---

# 기본 계산된 지표

Adobe Analytics은 가장 일반적인 사용 사례를 다루기 위해 다양한 계산된 지표를 제공합니다. 이러한 계산된 지표는 Analysis Workspace에서 기본적으로 사용할 수 있습니다.

다음은 Adobe에서 제공하는 각 계산된 지표의 목록이며, 해당 의도된 함수와 이를 계산하는 데 사용되는 기본 공식이 포함되어 있습니다.

>[!NOTE]
>
>이 페이지에 설명된 기본 계산된 지표 외에 보고서 세트에 추가 계산된 지표를 추가할 수도 있습니다.
>
>:
> * 에 설명된 대로 스트리밍 미디어에 대한 기본 계산된 지표 추가 [계산된 지표](/https://experienceleague.adobe.com/docs/media-analytics/using/implementation/variables/calculated-metrics.html)
> * 에 설명된 대로 기존 지표에서 사용자 정의 계산된 지표 만들기 [계산 및 고급 계산(파생) 지표](/help/components/c-calcmetrics/cm-overview.md).



| 계산된 지표 이름 | 함수 | 공식 |
|---------|----------|---------|
| 바운스 비율 | 해당 페이지의 방문 수와 비교하여 정확히 하나의 히트가 포함된 방문의 비율입니다. 바운스 비율이 가장 높은 차원 항목을 이해하거나 시간에 따른 사이트의 총 바운스 비율 집계를 확인하는 데 도움이 될 수 있습니다. | 바운스 비율 |
| 매출 / 방문자 | 사이트에 대한 각 개별 방문자가 생성한 평균 매출액입니다. | <p>매출</p><p>/</p><p>고유 방문자 수</p> |
| 주문 수/방문자 수 | 사이트에 대한 각 개별 방문자가 생성한 평균 주문 또는 트랜잭션 수 | <p>기본 주문</p><p>/</p><p>방문자</p> |
| 매출 / 방문 횟수 | 사이트에 대한 단일 방문으로 생성된 평균 매출액입니다. | <p>매출</p><p>/</p><p>고유 방문 횟수</p> |
| 매출 / 주문 | 사이트에서 완료된 각 거래 또는 주문으로 생성된 평균 매출액. | <p>매출</p><p>/</p><p>주문</p> |
| 주문 수/방문 수 | 완료된 트랜잭션을 초래하는 사이트 방문 비율입니다. | <p>주문</p><p>/</p><p>방문 횟수</p> |
| 페이지 조회수/방문 수 | 사용자가 사이트를 한 번 방문하는 동안 보는 평균 페이지 수입니다. | <p>페이지 조회수</p><p>/</p><p>방문 횟수</p> |
| 방문 횟수 / 방문자 | 고유 방문자가 사이트를 방문하는 평균 횟수입니다. | <p>방문 횟수</p><p>/</p><p>고유 방문자 수</p> |
| 다시 로드 / 페이지 보기 | 페이지를 다시 로드하거나 새로 고친 페이지 보기 횟수의 비율입니다. | <p>다시 로드</p><p>/</p><p>페이지 조회수</p> |
| 가중 바운스 비율 | 함수 | if(방문>백분위수(방문),bouncerate,0) |
| 지원 주문 | 채널 또는 소스가 구매에 대한 고객의 여정에 기여했지만 최종 구매로 이어지지 않은 횟수입니다. | <p>주문(기여도\|방문)</p><p>-</p><p>주문</p> |
| 종료 비율 | 특정 페이지를 본 후 사이트를 나가는 방문자의 비율입니다. | <p>종료</p><p>/</p><p>방문 횟수</p> |
| 시작 비율 | 사이트의 총 세션 수와 비교하여 주어진 페이지에서 사이트에 들어간 방문자의 비율입니다. | <p>항목</p><p>/</p><p>방문 횟수</p> |
| 사이트의 평균 시간 | 방문자가 사이트를 떠나거나 떠나기 전에 사이트에서 보낸 평균 시간입니다. | 사이트에서 보낸 평균 시간(초) |
| 체류 시간/사용자(상태) | 평균 방문자가 사이트에 있는 동안 특정 상태에서 보내는 시간 | 방문자당 체류 시간 (초) 지표 + 모바일 앱 세그먼트 |
| 사용자(모바일) | 모바일 앱의 총 사용자 수 | 고유 방문자 수 지표 + 모바일 앱 사용자 세그먼트 |
| 앱 사용자 | 모바일 앱의 총 사용자 수 | 고유 방문자 수 지표 + 모바일 앱 세그먼트 |
| 상태 보기 | 앱의 다양한 상태 또는 화면에 대한 보기 수 | 페이지 보기 수 지표 + 모바일 앱 세그먼트 |
| 작업 | 앱에서 수행한 총 작업 수 | 사용자 지정 링크 인스턴스 지표 + 작업 세그먼트 있음 |
| 획득 링크 클릭 수 | 사이트로 트래픽을 유도하기 위해 고안된 링크를 사람들이 클릭하는 횟수입니다. | Campaign 클릭스루 지표 |
| 페이지 속도 | 콘텐츠 조각이 생성하는 추가 페이지 보기 수입니다. 이를 통해 추가 참여를 유도하는 콘텐츠를 확인할 수 있습니다. | <p>페이지 조회수</p><p>/</p><p>방문 횟수</p> |
| 전환율 | 구매와 같이 원하는 조치를 취한 방문자의 비율입니다. | <p>주문</p><p>/</p><p>방문 횟수</p> |
| 평균 세션 길이(모바일) | 방문자가 단일 세션 동안 사이트에서 보낸 평균 시간입니다. | 빈 |
| Experience Cloud ID 범위 | Experience Cloud ID가 있는 방문자의 비율입니다. | <p>Experience Cloud ID를 가진 방문자</p><p>/</p><p>고유 방문자 수</p> |
| 콘텐츠 속도 | 사이트에서 새 콘텐츠를 만들고 게시하는 속도와 사용자 참여를 생성하는 속도입니다. | <p>페이지 조회수</p><p>/</p><p>방문 횟수</p> |
| ITP 2.1 고유 방문자 수 / 고유 방문자 수 | ITP 2.1 쿠키 제한 사항의 영향을 받는 브라우저를 사용하는 고유 방문자의 비율입니다. 즉, 고객이 CNAME 구현을 사용하지 않는 경우입니다. (클라이언트측 JavaScript를 통해 쿠키를 설정하는 고객에게 적용됩니다.) | <p>고유 방문자 수 지표 + ITP 방문자 세그먼트</p><p>/</p><p>고유 방문자 수</p> |
| 고유 방문자 수/7일 후 재방문하는 고유 방문자 수 | 7일 이상의 기간이 지난 후 재방문하는 고유 방문자의 비율입니다. | <p>고유 방문자 수 지표 + 7일 세그먼트 후 재방문하는 사용자</p><p>/</p><p>고유 방문자 수</p> |
| 페이지 조회수 / 고유 방문자 | 사이트에 대한 각 고유 방문자에 대해 본 평균 페이지 수입니다. | <p>페이지 조회수</p><p>/</p><p>고유 방문자 수</p> |
| 방문 횟수 / 방문자 수 | 고유 방문자가 사이트에 대해 수행하는 평균 방문 횟수입니다. | <p>방문 횟수</p><p>/</p><p>고유 방문자 수</p> |
| 예상 고유 방문자 수(ITP 2.1) | <p>ITP 방문자(Safari 브라우저의 사용자)의 경우 고유 방문자 수를 2 이하로 나눕니다.</p><p>클라이언트측 JavaScript를 사용하여 쿠키를 설정한다고 가정합니다(CNAME 구현을 사용하지 않음). 클라이언트측 JavaScript를 사용하여 쿠키를 설정하는 구현은 ITP 2.1부터 영향을 받았습니다. 다음을 참조하십시오. [https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/)</p> | <p>고유 방문자 수 지표 + ITP 방문자(ITP 2.1, 비 CNAME 구현) 세그먼트</p><p>/</p><p>고유 방문자 수 지표 + 비ITP 방문자(ITP 2.1, 비CNAME 구현) 세그먼트</p> |
| 페이지 보기 수 / 예상 고유 방문자 수(ITP 2.1) | 예상 고유 방문자 수(ITP 2.1)에 대해 본 평균 페이지 수입니다. | <p>고유 방문자 수 지표 + ITP 방문자(ITP 2.1, 비 CNAME 구현) 세그먼트</p><p>/</p><p>고유 방문자 수 지표 + 비ITP 방문자(ITP 2.1, 비CNAME 구현) 세그먼트</p> |

{style="table-layout:auto"}