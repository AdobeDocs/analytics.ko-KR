---
description: 'null'
keywords: DFA
seo-description: 'null'
seo-title: 전제 조건
solution: Analytics
title: 전제 조건
topic: Data connectors
uuid: B 5 F 5 E 30 C-E 269-41 A 4-9236-5 DDC 404 BFD 94
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# 전제 조건{#prerequisites}

DFA에 대한 Adobe Data Connectors 통합을 시작하기 전에 다음을 수행하십시오.

* 통합 버전 1.5에 통합할 것인지 아니면 버전 2.0을 기다릴 것인지 결정합니다. 이러한 결정은 DFA 계정에서 사용하는 기능과 통합할 기간에 따라 다릅니다. 자세한 내용은 [버전 2.0 정보](../dfa-data-connector-analytics/dfa-version-differences.md#concept-2c7d6a6ab8524dccad96ea0c17228664)를 참조하십시오.
* DFA 광고주가 Adobe Analytics 보고서 세트에 매핑하는 방법을 결정합니다. 예를 들어, 여러 DFA 광고주와 여러 보고서 세트가 있는 경우 보고서 세트와 함께 사용할 광고주를 결정해야 합니다.
* 데이터 수집 코드 버전 H.22 이상을 사용하여 추적할 모든 페이지에 Adobe 데이터 수집 코드를 구현합니다.
* 통합하려는 Floodlight 구성에 포함된 DFA 계정의 광고주 ID를 확인합니다. 통합은 Floodlight 구성 내에 있는 모든 광고주를 자동으로 가져옵니다.
* DFA 계정 사용자 이름과 암호를 확인합니다.
* 각 DFA 광고주를 한 Adobe Analytics 보고서 세트에만 연결합니다. 기본 DFA용 Genesis 통합에서는 여러 보고서 세트에 태그를 지정할 수 없습니다.
* 클릭스루 쿼리 문자열 매개 변수를 통합에 포함될 각 DFA 게재위치에 대한 랜딩 페이지에 추가합니다. 이 쿼리 문자열 매개 변수는 클릭스루를 올바르게 계산하는 데 필요합니다.
* 방문자가 여러 도메인을 통해 리디렉션되지 않도록 DFA 게재위치를 구성합니다. 예를 들면, 마이크로 사이트에서 다른 사이트, www.fgh.com으로 응답자 수를 리디렉션하는 경우 게재 위치는 www.xyz.com에서 호스팅하는 마이크로 사이트로 응답자 수를 보내지 않습니다. 캠페인 응답이 여러 도메인을 포괄하는 경우 클릭스루와 뷰스루 데이터가 늘어나고 잘못될 수 있습니다.
* 캠페인 정보를 보유할 보고 및 분석의 사용자 지정 변수를 식별합니다.
* DFA 뷰스루 정보를 저장할 보고 및 분석 eVar을 식별합니다. 이 eVar은 이 DFA 통합에만 사용합니다.
* 노출 횟수 및 클릭 수 데이터를 저장할 보고 및 분석 이벤트를 식별합니다. 이러한 이벤트의 이름을 적절하게 바꾸어야 할 수 있습니다.
* (선택 사항) DFA 비용 데이터를 저장할 보고 및 분석 이벤트를 식별합니다. 이러한 이벤트의 이름을 적절하게 바꾸어야 할 수 있습니다.
* (선택 사항) DFA 오류 및 시간 초과를 저장할 보고 및 분석 사용자 지정 변수와 성공 이벤트를 식별합니다. 이러한 변수는 통합에서 발생할 수 있는 문제를 진단하는 데 도움이 됩니다.
* (선택 사항) DFA에 대한 Data Connectors 통합과 관련된 정보 및 알림을 받을 특수 이메일 계정을 만듭니다.

