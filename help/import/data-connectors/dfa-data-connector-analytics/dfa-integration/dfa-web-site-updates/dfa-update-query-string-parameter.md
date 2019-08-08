---
description: 'null'
keywords: DFA
seo-description: 'null'
seo-title: DFA 쿼리 문자열 매개 변수 업데이트
solution: Analytics
title: DFA 쿼리 문자열 매개 변수 업데이트
topic: Data connectors
uuid: adf 585 ac -84 ff -44 c 1-a 48 d-b 072726 c 8494
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# DFA 쿼리 문자열 매개 변수 업데이트{#update-your-dfa-query-string-parameter}

DFA 통합 전에 Adobe Analytics로 광고 캠페인을 이미 추적한 경우에는 모든 캠페인(이메일, 검색 또는 배너)에서 같은 쿼리 문자열 매개 변수를 사용하여 랜딩 페이지에서 참조하는 캠페인 ID를 식별할 수 있습니다.

DFA 광고 캠페인에 대한 DFA 데이터에서 뷰스루와 클릭스루 데이터를 요청하는 시기를 알아두려면 Data Connectors에서 방문자가 DFA 캠페인 배너 광고를 클릭한 시간을 식별할 수 있어야 합니다. 이렇게 하려면 Data Connectors에서 DFA 광고 캠페인 페이지와 웹 사이트에 있을 수 있는 다른 광고 캠페인 페이지를 구분할 수 있도록 구별된 쿼리 문자열 매개 변수를 DFA 광고 캠페인의 랜딩 페이지 URL에 추가해야 합니다. DFA에 사용되는 JavaScript 플러그인 `dfa_overrideParam` (웹 사이트 데이터 수집 코드 [](../../../dfa-data-connector-analytics/dfa-integration/dfa-web-site-updates/dfa-update-data-collection-code.md#concept-8c108723ea0b4cc9a8c5cdc2d05894e3)업데이트 참조) 에서.

>[!CAUTION]
>
>캠페인 변수를 다른 캠페인에 사용할 수 있지만 DFA 캠페인에 사용할 수는 없습니다. 캠페인 변수를 DFA 캠페인 랜딩 페이지로 설정한 경우 Adobe에서 노출 횟수와 클릭 수를 DFA 캠페인 클릭스루에 연결할 수 없습니다. 방문당 한 번, Adobe 수집 서버는 DFA 서버에서 이전 클릭스루 또는 뷰스루를 확인합니다. 이러한 이유로 DFA 플러그인 코드( [웹 사이트의 데이터 수집 코드 업데이트](../../../dfa-data-connector-analytics/dfa-integration/dfa-web-site-updates/dfa-update-data-collection-code.md#concept-8c108723ea0b4cc9a8c5cdc2d05894e3) 참조)를 일반적인 랜딩 페이지에서만 포함해야 특히 인터넷 연결 속도가 느린 사용자를 위해 페이지 로드 시간이 느려질 수 있는 불필요한 리디렉션을 방지할 수 있습니다.

