---
title: 보고서
description: 보고 및 분석에서 각 보고서에 사용하는 차원 및 지표.
translation-type: tm+mt
source-git-commit: 1968162d856b6a74bc61f22f2e5a6b1599d04c79
workflow-type: tm+mt
source-wordcount: '1863'
ht-degree: 1%

---


# 보고서

보고 및 분석의 각 보고서는 전용 차원 및 기본 지표를 사용합니다. 각 보고서에서 지표를 변경하고 원할 경우 분류를 추가할 수 있습니다. 다음 목록은 각 보고서에서 사용되는 차원을 제공합니다.

> [!NOTE] 보고서 메뉴는 조직의 관리자가 사용자 정의한 내용에 따라 다르게 표시될 수 있습니다. See [Menu customizing](/help/admin/admin/customize-menus.md) in the Admin user guide.

## 사이트 지표

일반적으로 날짜 범위를 사용하여 트렌드를 표시하는 보고서를 포함합니다. 또한 권장 보고서 및 실시간 보고서와 같은 고유한 보고서가 포함되어 있습니다.

* 권장 보고서: 즉시 인사이트를 얻을 수 있는 여러 reportlet이 포함된 대시보드를 만듭니다.
* 주요 지표: 한 번에 최대 5개의 지표로 트렌드를 표시할 수 있는 보고서입니다. 트렌드 [페이지 보기](/help/components/metrics/page-views.md), [방문](/help/components/metrics/visits.md)및 [고유 방문자](/help/components/metrics/unique-visitors.md) 를 기본적으로지정합니다.
* 페이지 보기: 시간에 따라 [페이지 보기](/help/components/metrics/page-views.md) 지표의 트렌드를 표시합니다.
* 방문 횟수: 시간에 따른 [방문](/help/components/metrics/visits.md) 지표의 트렌드를 표시합니다.
* 방문자: 시간에 따른 다양한 [고유 방문자](/help/components/metrics/unique-visitors.md) 지표 트렌드
   * 고유 방문자 수: 선택한 전체 날짜 범위에 대해 방문자를 한 번만 카운트합니다.
   * 시간별 고유 방문자: 선택한 날짜 범위의 다른 시간 동안 방문하는 방문자를 여러 번 카운트합니다.
   * 일별 고유 방문자 수: 선택한 날짜 범위의 다른 일 동안 방문하는 방문자를 여러 번 카운트합니다.
   * 주별 고유 방문자: 선택한 날짜 범위의 여러 주 동안 방문하는 방문자를 여러 번 카운트합니다.
   * 월별 고유 방문자: 선택한 날짜 범위의 여러 달 동안 방문하는 방문자를 여러 번 카운트합니다.
   * 분기별 고유 방문자: 선택한 날짜 범위의 다른 분기 동안 방문하는 방문자를 여러 번 카운트합니다. 분기는 1월 3월, 4월 6월, 7월, 9월 그리고 10월 중 입니다.
   * 연간 고유 방문자 수: 선택한 날짜 범위의 다른 달력 연도 동안 방문하는 방문자를 여러 번 카운트합니다.
* 방문당 체류 시간: 방문당 [체류 시간 - 버킷 차원을](/help/components/dimensions/time-spent-per-visit.md) 사용합니다.
* 이벤트까지 남은 시간: 이전 [시간 차원을](/help/components/dimensions/time-prior-to-event.md) 사용합니다.
* 구매: 구매 기반 지표에 대한 보고서를 포함합니다.
   * 구매 전환 단계: 방문 횟수 [,](/help/components/metrics/visits.md)장바구니 [, 주문](/help/components/metrics/carts.md)수, 매출 [, 및](/help/components/metrics/orders.md)[](/help/components/metrics/revenue.md)[](/help/components/metrics/units.md) 단계 단위 보고서에 대한 보고서입니다. 폴아웃 시각화를 사용하여 분석 작업 공간에서 유사한 시각화가 [이루어집니다](../analysis-workspace/visualizations/fallout/fallout-flow.md).
   * 매출: 시간에 따른 지표 [매출](/help/components/metrics/revenue.md) 트렌드를 표시합니다.
   * 주문: 시간에 따른 지표 [주문](/help/components/metrics/orders.md) 트렌드를 표시합니다.
   * 판매량: 시간에 따른 지표 [판매량](/help/components/metrics/units.md) 트렌드를 표시합니다.
* 장바구니: 장바구니 지표에 대한 보고서를 포함합니다.
   * 장바구니 전환 단계: 보고서 [인스턴스](/help/components/metrics/instances.md), [체크아웃](/help/components/metrics/carts.md), 주문 [, 및](/help/components/metrics/checkouts.md)[](/help/components/metrics/orders.md)[](/help/components/metrics/revenue.md) 매출 단계 보고서에서 연속 매출.
   * 장바구니: 시간 경과에 따른 지표 [장바구니](/help/components/metrics/carts.md) 트렌드를 표시합니다.
   * 장바구니 보기: 시간 경과에 따라 지표 [장바구니 보기](/help/components/metrics/cart-views.md) 트렌드를 표시합니다.
   * 장바구니 추가: 시간 경과에 따라 지표 [장바구니 추가](/help/components/metrics/cart-additions.md) 트렌드를 표시합니다.
   * 장바구니 제거: 시간 경과에 따라 [장바구니 제거 지표를](/help/components/metrics/cart-removals.md) 추적합니다.
   * 체크아웃: 시간 경과에 따른 지표 [체크아웃](/help/components/metrics/checkouts.md) 트렌드를 표시합니다.
* 사용자 지정 이벤트: 구현과 관련된 사용자 지정 [이벤트에](/help/components/metrics/custom-events.md) 대한 모든 보고서를 포함합니다.
* 보트: 보트 관련 보고서를 표시합니다.
   * 보트: 사이트가 가장 자주 사용되는 보트를 표시합니다. See [Bot rules](../../admin/admin/bot-removal/bot-rules.md) in the Admin user guide.
   * 보트 페이지: 보트가 가장 많이 히트한 페이지를 표시합니다.
* 실시간: 데이터 수집 후 몇 초 내에 특정 차원과 지표를 표시합니다. See [Real-time reports](/help/components/c-real-time-reporting/realtime.md) for more information.

## 사이트 컨텐츠

일반적으로 사이트 컨텐츠를 표시하는 차원에 대한 보고서를 포함합니다. 이러한 보고서 중 일부에 분류를 적용할 수 있습니다. 분류를 적용하면 보고서가 소스 보고서와 분류 보고서를 포함하는 메뉴가 됩니다.

* 페이지: 페이지 [차원을](/help/components/dimensions/page.md) 사용합니다.
* 사이트 섹션: 사이트 [섹션](/help/components/dimensions/site-section.md) 차원을 사용합니다.
* 서버: 서버 [차원을](/help/components/dimensions/server.md) 사용합니다.
* 링크: 링크 추적을 사용하는 보고서를 포함합니다.
   * 종료 링크: 종료 [링크](/help/components/dimensions/exit-link.md) 차원을 사용합니다.
   * 파일 다운로드: 다운로드 [링크](/help/components/dimensions/download-link.md) 차원을 사용합니다.
   * 사용자 지정 링크: 사용자 [지정 링크](/help/components/dimensions/custom-link.md) 차원을 사용합니다.
   * 페이지를 찾을 수 없음: 페이지를 [찾을 수 없음 차원을](/help/components/dimensions/pages-not-found.md) 사용합니다.

## 모바일

기존 모바일 보고서에 대한 보고서를 포함합니다. 이러한 보고서는 사용자 에이전트 문자열을 기반으로 데이터를 만듭니다. 각 보고서에 다양한 [모바일 차원을](/help/components/dimensions/mobile-dimensions.md) 사용합니다.

* 장치: 모바일 장치 [차원을](/help/components/dimensions/mobile-dimensions.md) 사용합니다.
* 장치 유형: 모바일 장치 [유형](/help/components/dimensions/mobile-dimensions.md) 차원을 사용합니다.
* 제조업체: 모바일 제조업체 [차원을](/help/components/dimensions/mobile-dimensions.md) 사용합니다.
* 화면 크기: 모바일 [화면 크기](/help/components/dimensions/mobile-dimensions.md) 차원을 사용합니다.
* 화면 높이: 모바일 [화면 높이](/help/components/dimensions/mobile-dimensions.md) 차원을 사용합니다.
* 화면 너비: 모바일 [화면 너비](/help/components/dimensions/mobile-dimensions.md) 차원을 사용합니다.
* 쿠키 지원: 모바일 쿠키 [지원](/help/components/dimensions/mobile-dimensions.md) 차원을 사용합니다.
* 이미지 지원: 모바일 [이미지 지원](/help/components/dimensions/mobile-dimensions.md) 차원을 사용합니다.
* 색상 깊이: 모바일 [색상 깊이](/help/components/dimensions/mobile-dimensions.md) 차원을 사용합니다.
* 오디오 지원: 모바일 [오디오 지원](/help/components/dimensions/mobile-dimensions.md) 차원을 사용합니다.
* 비디오 지원: 모바일 [비디오 지원](/help/components/dimensions/mobile-dimensions.md) 차원을 사용합니다.
* 운영 체제(더 이상 사용되지 않음): 모바일 [운영 체제(더 이상 사용되지 않음)](/help/components/dimensions/mobile-dimensions.md) 차원을 사용합니다.

## 경로

방문자에 대한 경로 지정 데이터를 볼 수 있는 보고서를 포함합니다.

* 다음 페이지 흐름: 상단 페이지 차원 값에 흐름 보고서를 사용합니다. 경로 보기는 인스턴스와 [유사합니다](/help/components/metrics/instances.md). 보고된 차원 값을 변경할 수 있습니다. 분석 작업 공간의 유사한 보고서는 [흐름 시각화를 사용하여 사용할 수 있습니다](../analysis-workspace/visualizations/c-flow/flow.md).
* 다음 페이지: 상위 페이지 차원 값을 가져와서 방문자가 방문한 다음 페이지를 표시합니다.
* 이전 페이지 흐름: 상위 페이지 차원 값에 대한 흐름 보고서 사용 분석 작업 공간의 유사한 보고서는 [흐름 시각화를 사용하여 사용할 수 있습니다](../analysis-workspace/visualizations/c-flow/flow.md).
* 이전 페이지: 상위 페이지 차원 값을 가져와서 방문자의 이전 페이지를 표시합니다.
* 폴아웃: 단계에서 페이지 차원 값을 선택할 수 있도록 하며, 해당 경로를 따르고 따르지 않은 사람들의 비율을 표시합니다. 분석 작업 공간의 유사한 보고서는 폴아웃 시각화를 사용하여 사용할 [수 있습니다](../analysis-workspace/visualizations/fallout/fallout-flow.md).
* 전체 경로: 개별 경로를 차원 값으로 표시합니다. 분석 작업 공간에서 사용 중단; 흐름 [시각화를](../analysis-workspace/visualizations/c-flow/flow.md) 대신 사용하십시오.
* 경로 탐색: 경로(분석 작업 공간에서 중단)를 분석할 수 있는 여러 유형의 보고서를 제공합니다.
* 경로 길이: 방문 [깊이](/help/components/dimensions/visit-depth.md) 차원을 사용합니다.
* 페이지 분석
   * 페이지 요약: 상위 페이지 차원 값을 가져와 트렌드 보기를 표시합니다. 또한 해당 상위 페이지 차원 값에 대한 시작 지점, 이전 페이지, 종료 지점 및 다음 페이지를 표시합니다.
   * 다시 로드: 다시 로드 [지표](/help/components/dimensions/page.md) 와 함께 [페이지](/help/components/metrics/reloads.md) 차원을사용합니다.
   * 페이지에서 보낸 시간: 페이지에서 [보낸 시간(버킷된 차원)을](/help/components/dimensions/time-spent-on-page.md) 사용합니다.
   * 페이지 클릭 수: 상위 페이지 차원 값을 가져와서 주어진 방문에서 해당 페이지에 도달하는 데 걸린 클릭 수를 표시합니다.
* 시작 및 종료
   * 시작 페이지: 시작 페이지 [차원을](/help/components/dimensions/entry-dimensions.md) 사용합니다.
   * 원래 시작 페이지: 시작 [페이지 원래](/help/components/dimensions/entry-dimensions.md) 차원을 사용합니다.
   * 단일 페이지 방문: Adobe에서 제공한 [단일](/help/components/dimensions/page.md) 페이지 방문 횟수&#39; 세그먼트가 적용된 페이지 차원을 사용합니다.
   * 종료 페이지: 종료 페이지 [차원을](/help/components/dimensions/exit-dimensions.md) 사용합니다.

> [!NOTE] 다른 보고서가 이 폴더에 표시될 수 있습니다. 보고서 세트 설정에서 [경로 지정을 활성화한](../../admin/admin/c-traffic-variables/traffic-var.md) prop과 같은 다른 차원입니다.

## 트래픽 소스

방문자가 사이트에 오기 전에 있었던 위치에 대한 통찰력을 제공하는 보고서를 포함합니다. 보고서 세트 설정에서 [내부 URL 필터를](../../admin/admin/internal-url-filter-admin.md) 올바르게 설정하지 않으면 이러한 보고서가 제대로 작동하지 않습니다.

* 검색 키워드 - 모두: 검색 키워드 [차원을](/help/components/dimensions/search-keyword.md) 사용합니다.
* 검색 키워드 - 유료: 검색 [키워드 - 유료](/help/components/dimensions/search-keyword.md) 차원을 사용합니다.
* 검색 키워드 - 자연어: Search [키워드 - 자연어](/help/components/dimensions/search-keyword.md) 차원 사용
* 검색 엔진 - 모두: 검색 [엔진](/help/components/dimensions/search-engine.md) 차원을 사용합니다.
* 검색 엔진 - 유료: 검색 [엔진 - 유료](/help/components/dimensions/search-engine.md) 차원을 사용합니다.
* 검색 엔진 - 자연어: 검색 [엔진 - 자연형](/help/components/dimensions/search-engine.md) 차원을 사용합니다.
* 모든 검색 페이지 등급: 모든 [검색 페이지 등급 차원을](/help/components/dimensions/all-search-page-rank.md) 사용합니다.
* 참조 도메인: 참조 [도메인](/help/components/dimensions/referring-domain.md) 차원 사용
* 원래 참조 도메인: 원래 [참조 도메인](/help/components/dimensions/original-referring-domain.md) 차원 사용
* 레퍼러: 레퍼러 [차원을](/help/components/dimensions/referrer.md) 사용합니다.
* 레퍼러 유형: 레퍼러 [유형](/help/components/dimensions/referrer-type.md) 차원을 사용합니다.

## 캠페인

주로 [추적 코드](/help/components/dimensions/tracking-code.md) 차원과 관련된 보고서를 포함합니다.

* 캠페인 전환 단계: 단계 보고서에서 클릭스루, 체크아웃 [,](/help/components/metrics/checkouts.md)주문 [및](/help/components/metrics/orders.md)매출 [을](/help/components/metrics/revenue.md) 보고합니다. 클릭스루 지표는 [추적 코드](/help/components/metrics/instances.md) 차원 컨텍스트에서 인스턴스 [지표와](/help/components/dimensions/tracking-code.md) 유사합니다. 폴아웃 시각화를 사용하여 분석 작업 공간에서 유사한 시각화가 [이루어집니다](../analysis-workspace/visualizations/fallout/fallout-flow.md).
* 추적 코드: 추적 [코드](/help/components/dimensions/tracking-code.md) 차원을 사용합니다.

## 제품

주로 [제품](/help/components/dimensions/product.md) 차원 관련 보고서를 포함합니다.

* 제품 전환 단계: 보고서 [제품 보기](/help/components/metrics/product-views.md), [장바구니 추가](/help/components/metrics/cart-additions.md), [체크아웃](/help/components/metrics/checkouts.md),Publications, Publications Units, 및 Foundle Revenue보고서 [](/help/components/metrics/orders.md)[](/help/components/metrics/units.md)[](/help/components/metrics/revenue.md) 의 매출. 폴아웃 시각화를 사용하여 분석 작업 공간에서 유사한 시각화가 [이루어집니다](../analysis-workspace/visualizations/fallout/fallout-flow.md).
* 제품: 제품 [차원을](/help/components/dimensions/product.md) 사용합니다.
* 크로스셀: 일반적으로 함께 판매되는 제품(분석 작업 공간에서 사용 중단)을 표시합니다.
* 카테고리: 카테고리 [차원을](/help/components/dimensions/category.md) 사용합니다.

## 방문자 유지

사이트로 돌아온 방문자에 대한 보고서를 포함합니다.

* 재방문 주기: 재방문 주기 [차원을](/help/components/dimensions/return-frequency.md) 사용합니다.
* 재방문: Adobe에서 제공한 [재방문](/help/components/metrics/visits.md) &#39; 세그먼트가 적용된 시간에 따른 방문 횟수 지표의 트렌드를 표시합니다.
* 방문 번호: 방문 [번호](/help/components/dimensions/visit-number.md) 차원을 사용합니다.
* 영업 주기: 구매 관련 보고서 폴더.
   * 고객 충성도: 고객 [충성도](/help/components/dimensions/customer-loyalty.md) 차원을 사용합니다.
   * 첫 구매까지 소요된 일 수: 첫 [구매까지 소요된 일](/help/components/dimensions/days-before-first-purchase.md) 차원을 사용합니다.
   * 마지막 구매 이후 일 수: 마지막 [구매 이후 일](/help/components/dimensions/days-since-last-purchase.md) 차원을 사용합니다.
   * 일별 고유 고객: 트렌드 [Adobe에서 제공한 &#39;구매자&#39; 세그먼트가 적용된 시간에 따른 일일 고유 방문자](/help/components/metrics/unique-visitors.md) 수
   * 주별 고유 고객: 트렌드 [Adobe에서 제공한 &#39;구매자&#39; 세그먼트가 적용된 시간에 따른 주간 고유 방문자](/help/components/metrics/unique-visitors.md) 수
   * 월별 고유 고객: 트렌드 [Adobe에서 제공한 &#39;구매자&#39; 세그먼트가 적용된 시간에 따른 월별 고유 방문자](/help/components/metrics/unique-visitors.md) 수
   * 분기별 고유 고객: 트렌드 [Adobe에서 제공한 &#39;구매자&#39; 세그먼트를 사용한 시간에 따른 분기별 고유 방문자](/help/components/metrics/unique-visitors.md) 수 분기는 1월 3월, 4월 6월, 7월, 9월 그리고 10월 중 입니다.
   * 연간 고유 고객 수: 트렌드 [Adobe에서 제공한 &#39;구매자&#39; 세그먼트를 사용한 시간에 따른 연간 고유 방문자](/help/components/metrics/unique-visitors.md) 수

## 방문자 프로필

사이트를 방문하는 사람에 대한 보고서를 포함합니다.

* 지리 특성: 지구 상의 사이트 히트 위치에 대한 보고서입니다.
   * 국가: 국가 [차원을](/help/components/dimensions/countries.md) 사용합니다.
   * 지역: 지역 [차원을](/help/components/dimensions/regions.md) 사용합니다.
   * 시: 도시 [차원을](/help/components/dimensions/cities.md) 사용합니다.
   * 미국 주: 미국 [상태](/help/components/dimensions/us-states.md) 차원을 사용합니다.
   * 미국 DMA: 미국 [DMA](/help/components/dimensions/us-dma.md) 차원을 사용합니다.
* 언어: 언어 [차원을](/help/components/dimensions/language.md) 사용합니다.
* 시간대: 시간대 차원(분석 작업 공간에서 사용 중단)을 사용합니다. 차원 값은 히트의 GMT 오프셋입니다.
* 도메인: 도메인 [차원을](/help/components/dimensions/domain.md) 사용합니다.
* 최상위 도메인: 최상위 도메인 차원을 사용합니다(분석 작업 공간에서 중단). 도메인 [](/help/components/dimensions/domain.md) 차원을 상위 수준 카테고리로 그룹화합니다(일반적으로 도메인 국가별로).
* 기술: 사이트에 액세스하는 데 사용한 보고서에 대한 보고서가 들어 있는 폴더입니다.
   * 브라우저: 브라우저 [차원을](/help/components/dimensions/browser.md) 사용합니다.
   * 브라우저 유형: 브라우저 [유형](/help/components/dimensions/browser-type.md) 차원을 사용합니다.
   * 브라우저 너비: 브라우저 [너비 - 버킷 차원을](/help/components/dimensions/browser-width.md) 사용합니다.
   * 브라우저 높이: 브라우저 [높이 - Bucketed 차원을](/help/components/dimensions/browser-height.md) 사용합니다.
   * 운영 체제: 운영 [체제](/help/components/dimensions/operating-systems.md) 차원을 사용합니다.
   * 운영 체제 유형: 운영 [체제 유형](/help/components/dimensions/operating-system-types.md) 차원을 사용합니다.
   * 모니터 색상 깊이: 색상 [심도](/help/components/dimensions/color-depth.md) 차원을 사용합니다.
   * 모니터 해상도: 모니터 [해상도](/help/components/dimensions/monitor-resolution.md) 차원을 사용합니다.
   * Java: Java [활성화](/help/components/dimensions/java-enabled.md) 차원을 사용합니다.
   * JavaScript: JavaScript 활성화 차원(분석 작업 공간에서 사용 중단)을 사용합니다. 차원 값은 브라우저에 JavaScript가 활성화되어 있는지 여부에 따라 &#39;Enabled&#39;, &#39;Disabled&#39; 또는 &#39;Unknown&#39;입니다.
   * JavaScript 버전: 는 JavaScript 버전 차원(분석 작업 공간에서 사용 중단)을 사용합니다. 차원 값은 브라우저가 사용하는 JavaScript 버전을 보여 줍니다.
   * 쿠키: 쿠키 [지원](/help/components/dimensions/cookie-support.md) 차원을 사용합니다.
   * 연결 유형: 연결 유형 [차원을](/help/components/dimensions/connection-type.md) 사용합니다.
   * 이동통신사: 이동통신사 [차원을](/help/components/dimensions/mobile-dimensions.md) 사용합니다.
* 방문자 주: 상태 차원(분석 작업 공간에서 사용 중단)을 사용합니다. 차원 값은 변수에서 [`state`](../../implement/vars/page-vars/state.md) 가져옵니다.
* 방문자 ZIP/우편 번호: Zip [코드](/help/components/dimensions/zip-code.md) 차원을 사용합니다.

## 사용자 지정 전환

구현과 관련된 보고서를 포함합니다. 사용자 지정 전환 보고서는 [eVar](/help/components/dimensions/evar.md) 를 차원으로 사용합니다.

## 사용자 지정 트래픽

구현과 관련된 보고서를 포함합니다. 사용자 지정 트래픽 보고서는 [prop](/help/components/dimensions/prop.md) 을 차원으로 사용합니다.

## 마케팅 채널

마케팅 채널과 관련된 보고서 [를 포함합니다](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

* 채널 개요 보고서: 보고 및 분석과 관련된 사용자 지정 보고서입니다. 첫 번째 또는 마지막 터치 속성을 사용하는 지표와 함께 마케팅 채널을 차원 값으로 사용합니다.
* 첫 번째 터치 채널: 첫 [번째 접촉 채널](/help/components/dimensions/first-touch-channel.md) 차원을 사용합니다.
* 첫 번째 터치 채널 세부 사항: 첫 [번째 터치 채널 세부 사항](/help/components/dimensions/first-touch-detail.md) 차원을 사용합니다.
* 마지막 접촉 채널: 마지막 [접촉 채널](/help/components/dimensions/last-touch-channel.md) 차원을 사용합니다.
* 마지막 터치 채널 세부 사항: 마지막 [터치 채널 세부 사항](/help/components/dimensions/last-touch-detail.md) 차원을 사용합니다.

## 책갈피

책갈피를 표시한 보고서가 들어 있습니다. See [Bookmarks](bookmarks.md) for more information.

## 대시보드

만든 대시보드를 포함합니다. See [Dashboards](dashboard.md) for more information.

## 타겟

만든 타겟을 포함합니다. See [Targets](targets.md) for more information.

> [!NOTE] 이 도움말 페이지에서 보고서를 찾을 수 없는 경우 관리자의 이름을 바꾸거나 폴더를 조정했을 수 있습니다. See [Menu customizing](/help/admin/admin/customize-menus.md) in the Admin user guide.
