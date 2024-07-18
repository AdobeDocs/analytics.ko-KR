---
title: 일반 보트 서명
description: 봇의 공통 식별자를 인식합니다.
feature: Bot Removal
role: Admin
exl-id: 57622af6-c1d3-4ef1-b3e6-10c14f04a55c
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 100%

---

# 일반 보트 서명

환경에 따라 데이터 세트에서 봇을 식별하는 것은 다르지만 다음은 봇을 식별하는 몇 가지 일반적인 방법입니다.

## 높은 방문당 페이지 조회수

IP 주소, 페이지 조회수, 고유 방문자가 포함된 Data Warehouse 보고서를 가져올 수 있습니다. 그런 다음 방문당 페이지 조회수를 Excel로 계산하고 가장 높은 것에서 가장 낮은 것 순으로 정렬합니다. 봇은 일반적으로 방문당 페이지 조회수가 매우 높습니다 (수백에서 수천). 실제 진짜 트래픽으로 이동하면 급격한 감소를 확인할 수 있습니다.

## 레퍼러 없음

일반적으로 봇에는 참조 URL이 없습니다. 세분화에서 `Referring Domain equals Typed/Bookmarked`로 필터링될 수 있습니다.

## 이상한 사용자 에이전트

봇은 종종 브라우저 차원에서 분류되지 않거나 `unknown` 버전의 표준 브라우저로 표시되는 사용자 지정 사용자 에이전트를 사용합니다. 알 수 없는 Safari 및 알 수 없는 Opera는 봇이 될 가능성이 매우 높습니다.

## Linux 또는 “지정되지 않은” 운영 체제

훌륭한 오픈 소스 Linux 운영 체제의 평판을 망치려는 의도는 아니지만 봇이 설정하기 좋아하는 운영 체제인 것으로 여겨집니다. 그러나 Linux 사용자의 합법적인 트래픽을 제외하지 않도록 주의해야 합니다. 봇은 또한 `Operating System &#x200B;equals Not Specified`로 분할할 수 있는 운영 체제는 설정하지 않는 것을 좋아합니다.

## 페이지 조회수 = 방문 횟수 = 고유 방문자

이는 특히 사용자 에이전트 보고서에 적용됩니다. 아래 스크린 샷에서 볼 수 있듯이 이러한 “알 수 없는 버전”의 브라우저는 고유 방문자와 거의 동일한 방문자 수 (그리고 거의 동일한 페이지 조회수)를 가지고 있습니다. `Single Page Visits equals Enabled` 또는 `Hit Depth is less than 2`에 대한 [!UICONTROL Include]컨테이너를 빌드하여 세분화에서 분리될 수 있습니다.

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/assets/bots-browsers-unknown.png)

## 방문 횟수 1

봇은 일반적으로 실행할 때마다 새 방문자 ID를 가져오므로 한 번의 방문만 발생하고 모든 트래픽은 방문 횟수 1로 구성됩니다.

## 낮은 모니터 해상도

현대 사용자들은 과거보다 훨씬 높은 해상도의 모니터를 사용합니다. 다음 해상도의 히트가 봇에게 매우 인기 있는 것처럼 보입니다.

* 1024 x 768&#x200B;&#x200B;
* 1366 x 768
* 1600 x 864
* 800 x 600
* 1600 x 1200
* 지정되지 않음
* 1024 x 667

## 국가 + 시간대 불일치

시작된 국가와 시간대 사이의 불일치를 알아차릴 수 있을 것 있습니다. 예를 들어 위치는 미국이지만 시간대는 GMT일 수 있습니다.

![](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/assets/bots-country-time-zone.png)

## 로그인되지 않음

사용자가 방문 중 어느 시점에서도 로그인하지 않으며 이전 방문에서의 사용자 식별 eVar가 유지되지 않습니다. 일부 봇은 인증하도록 설정할 수 있지만 대다수는 그다지 스마트하지 않습니다.

## 방문 중 KPI 없음

봇은 일반적으로 장바구니에 제품을 추가하거나 결제하지 않습니다. 대부분의 경우 리드 양식이나 기타 성공 이벤트를 제출하지 않지만 일부 봇은 간단한 HTML 양식을 제출합니다. &#x200B;

## 특정 쿼리 문자열이 있음

때때로 봇은 잘못된 URL이나 존재하지 않는 URL (예: 일반적인 LAMP 또는 Wordpress 관리 페이지)을 누르거나 특정 쿼리 문자열을 추가하여 캐시를 파괴하거나 사이트를 중단시키려고 합니다.

## 분산 컴퓨팅 플랫폼에서 비롯된 IP 주소

Amazon Web Services 또는 Google Cloud와 같은 웹 호스팅 서비스는 봇 팜으로 악용될 수 있습니다. 이러한 IP 주소는 봇이 될 위험이 높습니다.
&#x200B;
* [Google Cloud](https://cloud.google.com/compute/): `&#x200B;35.199` 또는 `35.194&#x200B;`로 시작하는 IP 주소
