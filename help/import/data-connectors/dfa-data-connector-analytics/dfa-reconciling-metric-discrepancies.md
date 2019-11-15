---
description: Adobe Analytics 지표를 DFA 지표와 비교할 때 일부 지표가 허용 가능한 차이에 속하지 않을 수 있습니다. 아래에 지표 정의 및 가능한 변화 원인이 나열되어 있습니다.
keywords: DFA
solution: Analytics
title: 지표 불일치 조정
topic: Data connectors
uuid: aa3ca006-d3cf-410e-a000-781ab17fb9e3
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 지표 불일치 조정{#reconciling-metric-discrepancies}

Adobe Analytics 지표를 DFA 지표와 비교할 때 일부 지표가 허용 가능한 차이에 속하지 않을 수 있습니다. 아래에 지표 정의 및 가능한 변화 원인이 나열되어 있습니다.

이 섹션에서는 다음과 같은 정보를 제공합니다.

## 지표 정의{#metric-definitions}

Adobe는 DFA 통합과 관련된 지표에 대해 언급할 때 다음 용어를 사용합니다.

**노출 횟수**: 노출 횟수란 광고를 본 횟수를 말합니다. 노출 횟수는 광고별로 기록되지만, 광고 그룹 또는 다른 멀티 광고 그룹으로 집계될 수도 있습니다. Analytics의 노출 횟수 지표는 매일 밤 데이터 소스 가져오기를 통해 DFA에서 가져옵니다.

**클릭 수**: 클릭 수는 DFA에서 보고한 대로 광고를 클릭한 횟수를 말합니다. 클릭 수는 방문자가 고객 웹 사이트에 방문하기 전에 DFA 리디렉션 페이지에서 등록됩니다. 노출 횟수와 마찬가지로 Analytics의 클릭 수 지표는 매일 밤 데이터 소스 가져오기를 통해 DFA에서 가져옵니다.

**클릭스루**: 클릭스루란 사용자가 광고를 클릭한 후 랜딩 페이지에 도달한 횟수를 말합니다. 이 지표는 클릭 수와 약간 다를 수 있습니다.

**뷰스루**: 뷰스루란 방문자가 광고를 본 후에 해당 광고를 클릭하지 않고 고객의 웹 사이트에 온 횟수를 말합니다. 방문자는 뷰스루 창 내에서 사이트에 와야 합니다. 기본적으로 30일로 설정되어 있습니다. 노출은 마지막 클릭보다 최근에 발생했어야 합니다. 뷰스루는 캠페인마다, 방문마다 한 번 등록되고, 통합이 DFA 캠페인 ID로 뷰스루 eVar을 채우고 뷰스루 이벤트가 설정된 경우 계산됩니다.

## 가능한 불일치 이유{#possible-reasons-for-discrepancies}

Adobe Analytics와 DFA 보고서 간에 데이터 불일치가 발생할 수 있는 여러 가지 이유를 나열합니다.

### Safari 브라우저 및 타사 쿠키를 차단하는 기타 브라우저의 사용자 {#section-4b0dc429a54a4744a33976b0bb2d1b2a}

타사 쿠키 허용이 Adobe Analytics와 DFA 간 불일치가 발생하는 가장 큰 원인입니다. Safari 및 일부 다른 브라우저는 기본적으로 타사 쿠키를 차단합니다. 즉, 기본적으로 Safari는 대부분의 Analytics 구현에 사용되는 퍼스트 파티 쿠키를 허용하지만, DFA에 사용된 타사 쿠키는 거부합니다.

Adobe Analytics 15 베타 고객의 데이터 샘플에서는 일반적으로 퍼스트 파티 쿠키를 거부하는 사용자의 0.5% 미만이 표시되는 반면, 5-12%는 서드 파티 쿠키를 거부합니다(이러한 거부 중 많은 수가 기본 브라우저 설정 때문일 수 있음).

이러한 불일치로 인해 Analytics 및 DFA에서 수집한 데이터에 큰 차이가 있을 수 있습니다.

### DFA에 보고된 노출 횟수가 Adobe Analytics에 보고된 노출 횟수보다 많은 이유는 무엇입니까? {#section-db0ad070a65a4985bcc589b2d0d30b90}

* DFA는 매일 밤 일괄처리 시 Adobe 데이터 수집 서버로 데이터를 보내므로 Analytics의 노출 횟수 데이터가 DFA 보고서보다 2일까지 느릴 수 있습니다.
* Adobe는 SAINT 분류를 사용하여 가져온 DFA 추적 코드를 여러 집계 수준(캠페인 이름, 게재위치 이름, 광고 이름 등)으로 분류합니다. 분류 보고서를 실행할 때 불일치가 표시되면 간단한 테스트를 수행하여 분류에서 가져온 지표를 아직 처리하지 않았는지 확인합니다.

   * 분류 보고서에서 "없음"이라는 라인 항목을 찾습니다.
   * 원시 DFA ID 보고서(예: 캠페인 ID)를 사용하여 같은 변수로 이 라인 항목을 분류합니다.
   * In this report, take note of any unclassified DFA tracking codes which are in the form `DFA:XXXXX:XXXXX`.
   * 이러한 추적 코드가 많이 있으면 야간 SAINT 분류 프로세스를 조사합니다.

### DFA 클릭 수가 Adobe Analytics 클릭스루보다 많은 이유는 무엇입니까? {#section-2fce4608ed044bdc9cf812cb719d5d35}

* DFA는 방문자가 고객의 웹 사이트를 방문하기 전 클릭을 기록합니다. Analytics는 랜딩 페이지에 Adobe JavaScript 비콘이 로드되고 실행된 후 클릭스루를 기록합니다. 일반적으로 DFA가 클릭을 추적한 후 또는 타이머를 누른 후에 방문자가 랜딩 페이지에 도달하지 않은 경우 `s.maxDelay` 불일치가 발생합니다.
* Ensure all placements and creatives in the Floodlight Configuration include the clickThroughParam in the landing page URL (for example "`?CID=1`"). 이 매개 변수를 설정하지 못하면 Adobe Analytics JavaScript가 첫 번째 방문 히트 이후 발생하는 클릭스루를 모두 놓치게 됩니다.
* 모든 게재위치 및 광고 소재에 JavaScript로 태그가 지정되고 DFA 통합 모듈이 있으며 해당 랜딩 페이지의 Floodlight 구성 ID가 게재된 광고의 Floodlight 구성 ID와 일치하는지 확인합니다. 주로 광고에 대한 랜딩 페이지가 타사 사이트 또는 게재된 광고로 설정되었기 때문에 불일치가 발생합니다.
* 리치 미디어 광고 또는 Flash(swf) 광고를 사용하는 경우 DFA clicktracker를 누를 때마다 방문자의 브라우저도 쿼리 문자열에 포함된 `clickThroughParam`이 있는 랜딩 페이지로 리디렉션되는지 확인합니다. 브라우저를 리디렉션하지 못하면 클릭스루가 기록되지 않습니다.
* 시간 초과는 DFA 데이터를 사용할 수 있지만 JavaScript가 제 시간에 응답을 받지 못한 인스턴스를 나타냅니다. 방문자가 랜딩 페이지에 도달하면 Adobe JavaScript는 DFA의 fls.doubleclick.net 서비스에서 방문자의 정보를 요청합니다. The `s.maxDelay` 매개 변수는 JavaScript가 FLS(Floodlight 서비스) 데이터를 기다리는 기간을 결정합니다. If `s.maxDelay` is too high, visitors can leave the site before Adobe collects the hit data; meaning that no click data is recorded. If `s.maxDelay` is set too low, the visitor's Internet connection cannot retrieve the FLS data in time; meaning that the hit is sent to Adobe without DFA click information.
* 보트 트래픽이 DFA 클릭 수를 부풀릴 수 있습니다. 보트에 광고를 클릭하는 기능이 있을 수 있지만, Analytics 비콘을 실행하거나 동기화 스크립트 태그를 실행하여 Floodlight 서버 요청 데이터를 로드하는 과정이 복잡하지 않을 수 있습니다. 이러한 보트를 클릭 수 수치에서 제거하지 않은 경우 불일치의 원인이 될 수 있습니다.
* 이전 페이지에서 나가는 방문자 `s.maxDelay` 만료 전 및 DFA 데이터 반환 전에 페이지를 나가는 방문자는 손실되어, 이들에 대한 DFA 또는 방문자 데이터가 수집되지 않습니다.
* Analytics는 중복 클릭스루를 식별하여 제거하려고 하므로 클릭스루가 방문당 캠페인별로 한 번만 계산됩니다. DFA는 "뒤로"를 클릭하고 광고 리디렉션을 여러 번 통과한 방문자를 추가 ACM 클릭으로 계산하는 반면, Analytics는 이를 여러 개의 클릭스루로 계산하지 않습니다.
* DFA Floodlight 태그는 활성화된 JavaScript를 사용하지 않지만, Analytics는 사용합니다. 이러한 이유로 Analytics가 히트를 기록하지 않을 때 DFA가 히트를 기록하는 경우가 있습니다. 이러한 경우가 문제가 되는지 식별하려면 [방문자 프로필] 메뉴에서 Analytics JavaScript 보고서를 사용합니다.

### DFA 노출 후 액티비티 수가 Adobe Analytics 뷰스루보다 많은 이유는 무엇입니까? {#section-5daa91039c404df48b6a3447c20406f7}

* Analytics는 중복 클릭스루를 식별하여 제거하려고 하므로 클릭스루가 방문당 캠페인별로 한 번만 계산됩니다. DFA는 "뒤로"를 클릭하고 광고 리디렉션을 여러 번 통과한 방문자를 추가 ACM 클릭으로 계산하는 반면, Analytics는 이를 여러 개의 클릭스루로 계산하지 않습니다.
* DFA Floodlight 태그는 비활성화된 JavaScript를 사용하지 않지만, Analytics는 사용합니다. 이러한 이유로 Analytics가 히트를 기록하지 않을 때 DFA가 히트를 기록하는 경우가 있습니다. 
* DFA는 Floodlight 태그를 사용할 때 노출 후 액티비티 수를 계산합니다. 이 태그를 클라이언트 웹 사이트에 배치할 수 있습니다. Analytics는 JavaScript 비콘(이미지 요청)이 실행된 후에 뷰스루를 계산합니다. 웹 페이지에 코드 배치를 통해 중단된 페이지 로드가 노출 후 액티비티 수 또는 뷰스루로 계산되는지 확인할 수 있습니다.

### 불일치가 허용 가능한 범위를 많이 벗어나며 위의 가능한 이유가 해당되지 않을 경우 어떻게 합니까? {#section-ca50eb75dd5d4d0396f4668b44d7547c}

통합 컨설턴트 또는 Adobe Client Care에 문의하여 불일치를 문서화하고 이를 Data Connectors 엔지니어링 팀에 보고합니다. 요청을 신속하게 처리할 수 있도록 2~3일 간 문제가 있는 지표를 비교합니다(캠페인 코드 수준에서). 요청에서 이미 취한 모든 조치를 식별하여 불일치를 조정합니다.
