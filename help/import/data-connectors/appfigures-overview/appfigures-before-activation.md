---
description: 이 통합을 활성화하기 전에 Adobe Analytics® 및 이메일 소프트웨어의 배포에 대해 다음 항목을 검토하십시오.
seo-description: 이 통합을 활성화하기 전에 Adobe Analytics® 및 이메일 소프트웨어의 배포에 대해 다음 항목을 검토하십시오.
seo-title: 이 통합을 활성화하기 전에
title: 이 통합을 활성화하기 전에
uuid: fdc762bc-24e3-4c0a-904d-d4be2a4f3a20
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# 이 통합을 활성화하기 전에 {#before-you-activate-this-integration}

이 통합을 활성화하기 전에 Adobe Analytics® 및 이메일 소프트웨어의 배포에 대해 다음 항목을 검토하십시오.

이렇게 하면 정품 인증 전에 적절한 모범 사례나 사전 이수 과정이 준비되므로 최적의 통합 상태로 유지됩니다.

## Adobe Analytics Requirements{#adobe-analytics-requirements}

Adobe Analytics와 관련된 이 데이터 커넥터 통합에 대한 다음 정보를 검토하십시오.

* **** 보고서 세트별:이 통합은 보고서 세트별로 다릅니다. 통합을 활성화하기 전에 원하는 보고서 세트를 선택하고 보고서 세트에 데이터가 포함되어 있는지 확인합니다.
* **** 사용 가능하고 구성된 Analytics 변수:이 통합에는 10개의 사용자 지정 이벤트와 1개의 사용자 지정 eVar가 필요합니다. 분석 [통합 변수를 참조하십시오](appfigures-before-activation.md#analytics-integration-variables).

* **** 라이브 데이터로 초기화된 보고서 세트:이 통합을 위해 완전히 새로운 보고서 세트를 만드는 경우 라이브 추적 appFigures 요구 사항을 통해 일부(하나 이상의 히트) 데이터를 수신해야 합니다. 라이브 데이터가 기록되지 않은 경우 보고서 세트가 통합된 App Store 데이터를 받을 준비가 되지 않습니다.

* **** App Store와 기존 통합:이 통합은 13개월 동안 데이터를 채웁니다. 이전에 제공했던 모든 앱스토어 데이터 공급자와 겹치지 않도록 appFigures 담당자에게 문의하십시오. 데이터를 마지막으로 받은 날짜를 알려주십시오. appFigures는 그에 따라 채우기 기간을 조정합니다.

## appFigures Requirements{#appfigures-requirements}

appFigures와 관련된 이 데이터 커넥터 통합에 대한 다음 정보를 검토하십시오.

* **** appFigures의 현재 고객:이 통합을 사용하려면 Adobe 및 appFigures의 사용자가 되어야 합니다. 현재 appFigures Enterprise Plan의 사용자가 아닌 경우 통합 마법사를 완료하는 데 필요한 정보가 없습니다. 자세한 내용은 웹의 appFigures를 참조하십시오.
* **** appFigures 계정 키:appFigures 데이터 커넥터를 활성화하려면 appFigures 계정 키가 필요합니다. 이 계정 키는 "추가 기능" 섹션에서 생성할 수 있습니다. 자세한 [내용은 통합](../appfigures-overview/t-appfigures-integration.md) 구성을 참조하십시오.

* **데이터 종료**:다운로드, 판매 및 등급 정보는 이전 7일 동안 매일 동기화됩니다. 7일 후 데이터는 최종으로 간주되며 더 이상 업데이트되지 않습니다.

## 가격 책정{#pricing}

이 데이터 커넥터 통합에는 알아야 하는 가격 고려사항이 포함됩니다.

다음 섹션에는 추가 정보가 포함됩니다.

### Adobe 가격 고려 사항 {#section-2d1c79c895a5479bad8fdd97961ba6a3}

현재 이 통합을 활성화할 수 있는 비용은 없습니다. 그러나 데이터 소스 가져오기 때문에 서버 호출이 약간 증가할 수 있습니다.

### appFigures 가격 고려 사항 {#section-c6afad08c34b43e3a7a3637eea3328c3}

현재 이 통합과 관련된 비용이 없습니다. 이 통합은 현재 기업 고객에게만 제공됩니다. 자세한 [내용은 appFigures에](https://appfigures.com/support/contact) 문의하십시오.

## Analytics Integration Variables{#analytics-integration-variables}

appFigures의 데이터 커넥터 통합에서는 Analytics 변수를 사용하여 다양한 appFigures 지표를 추적합니다.

다음 표에서는 appFigures 통합에 대해 자동으로 활성화된 Analytics 변수에 대해 설명합니다.

### 필수 변수 {#section-3ca8dc46bab0436cba0c9ef827c8356a}

> [!NOTE] 이 통합에서는 앱스토어 데이터에 전용 변수를 사용하므로 사용자 지정 상거래 변수 및 이벤트를 할당할 필요가 없습니다.

| 변수 유형 |  이름  | 채우기 방법 | 설명 |
|---|---|---|---|
| eVar | 앱스토어 개체 ID | appFigures에서 가져옵니다. | 방문 만료, 최근 할당 및 기본 하위 관계로 이 eVar를 구성합니다. |
| 이벤트(숫자) | 앱스토어 다운로드 | appFigures에서 가져옵니다. | 모바일 애플리케이션 다운로드 수. |
| 이벤트(숫자) | 앱 스토어 구매(앱 내) | appFigures에서 가져옵니다. | 인앱 구매 및 구독 수입니다. |
| 이벤트(숫자) | 앱스토어 등급 | appFigures에서 가져옵니다. | 평균 appFigures 계산된 지표를 정의하는 데 사용됩니다. 직접 사용되지 않습니다. |
| 이벤트(숫자) | 앱스토어 등급 분류기 | appFigures에서 가져옵니다. | 평균 appFigures 계산된 지표를 정의하는 데 사용됩니다. 직접 사용되지 않습니다. |
| 이벤트(숫자) | 앱스토어 등급 | appFigures에서 가져옵니다. | 평균 appFigures 계산된 지표를 정의하는 데 사용됩니다. 직접 사용되지 않습니다. |
| 이벤트(숫자) | 앱스토어 등급 분류기 | appFigures에서 가져옵니다. | 평균 appFigures 계산된 지표를 정의하는 데 사용됩니다. 직접 사용되지 않습니다. |
| 이벤트(통화) | 앱스토어 매출(앱 내) | appFigures에서 가져옵니다. | 인앱 매출액 빼기 스토어 비용. |
| 이벤트(통화) | 앱스토어 매출(일회성) | appFigures에서 가져옵니다. | 앱 구매에서 발생한 총 매출에서 스토어 비용을 뺀 금액입니다. |
| 이벤트(통화) | 앱스토어 로열티(앱 내) | appFigures에서 가져옵니다. | 사용되지 않습니다 |
| 이벤트(통화) | 앱스토어 로열티(일회성) | appFigures에서 가져옵니다. | 사용되지 않습니다 |
