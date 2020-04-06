---
description: 데이터 피드를 사용한 일반 지표 계산 방법을 설명합니다.
keywords: Data Feed;job;metrics;pre column;post column;bots;date filtering;event string;common;formulas
title: 지표 계산
topic: Reports and analytics
uuid: a45ea5bb-7c83-468f-b94a-63add78931d7
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 데이터 피드를 사용한 일반 지표 계산

데이터 피드를 사용한 일반 지표 계산 방법을 설명합니다.

>[!IMPORTANT] 일반적으로 Adobe Analytics에서 제외된 히트는 데이터 피드에 포함됩니다. 원시 데이터의 쿼리에서 제외된 히트를 제거하려면 `exclude_hit > 0`을 사용합니다. 데이터 소스 데이터도 데이터 피드에 포함됩니다. 데이터 소스를 제외하려면 `hit_source = 5,7,8,9`가 있는 행을 모두 제외합니다.

## 페이지 보기 횟수

1. 값이 `post_pagename` 또는 `post_page_url`에 있는 행 수를 카운트합니다.

## 방문 횟수

1. `post_visid_high`, `post_visid_low`, `visit_num` 및 `visit_start_time_gmt`를 연결합니다.
1. 고유 값 수를 카운트합니다.

>[!NOTE] 인터넷 특이 사항, 시스템 특이 사항 또는 사용자 지정 방문자 ID의 사용은 서로 다른 방문 횟수에 대해 동일한 `visit_num` 값을 거의 사용할 수 없습니다. 방문 횟수를 카운트할 때 이러한 방문 횟수가 카운트되도록 `visit_start_time_gmt`를 사용합니다.

## 방문자 수

Adobe가 고유 방문자 수(사용자 지정 방문자 ID, Experience Cloud ID 서비스 등)를 식별하는 데 사용하는 모든 방법은 궁극적으로 모두 `post_visid_high` 및 `post_visid_low`의 값으로 계산됩니다. 이러한 두 열의 연결은 고유 방문자로 식별된 방식과 관계없이 고유 방문자 수를 식별하는 표준으로 사용될 수 있습니다. Adobe가 고유 방문자를 식별하는 데 사용한 방법을 이해하려면 열 `post_visid_type`을 사용하십시오.

1. `post_visid_high`와 `post_visid_low`를 연결합니다.
2. 고유 값 수를 카운트합니다.

## 사용자 지정, 다운로드 또는 종료 링크

1. 다음 위치의 행 수를 카운트합니다.
   * 사용자 지정 링크: `post_page_event = 100`
   * 다운로드 링크: `post_page_event = 101`
   * 종료 링크: `post_page_event = 102`

## 사용자 지정 이벤트

모든 지표는 `post_event_list` 열에서 쉼표로 구분된 정수로 계산됩니다. `event.tsv`를 사용하여 숫자 값을 원하는 이벤트와 연결합니다. 예를 들어 `post_event_list = 1,200`은 히트에 구매 이벤트와 사용자 지정 이벤트 1이 포함되었음을 나타냅니다.

1. 이벤트 조회 값이 `post_event_list`에 표시되는 횟수를 카운트합니다.

## 체류 시간

히트는 먼저 방문별로 그룹화한 다음 방문 내의 히트 번호에 따라 순서를 지정해야 합니다.

1. `post_visid_high`, `post_visid_low`, `visit_num` 및 `visit_start_time_gmt`를 연결합니다.
2. 이렇게 연결된 값으로 정렬한 다음 `visit_page_num`으로 보조 정렬을 적용합니다.
3. 히트가 방문의 마지막 히트가 아닌 경우 후속 히트의 `post_cust_hit_time` 값에서 `post_cust_hit_time` 값을 뺍니다.
4. 이 숫자는 히트에 걸린 시간(초)입니다. 필터를 적용하여 차원값 또는 이벤트에 중점을 둘 수 있습니다.

## 주문 수, 판매량 및 매출량

히트의 `currency` 값이 보고서 세트의 통화와 일치하지 않으면 해당 날짜의 전환율을 사용하여 변환됩니다. `post_product_list` 열은 변환된 통화 값을 사용하므로 모든 히트가 이 열에서 동일한 통화를 사용합니다.

1. `duplicate_purchase = 1`인 모든 행을 제외합니다.
2. `event_list`에 구매 이벤트가 들어 있는 행만 포함합니다.
3. `post_product_list` 열을 구문 분석하여 모든 가격 데이터를 추출합니다. `post_product_list` 열은 `s.products` 변수와 동일하게 형식이 지정됩니다.
4. 원하는 지표를 계산합니다.
   * 행 수를 계산하여 주문 수 계산
   * 제품 문자열에서 `quantity` 수를 합하여 판매량 계산
   * 제품 문자열에서 `price` 수를 합하여 매출량 계산
