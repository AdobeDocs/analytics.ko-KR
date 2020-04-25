---
description: 이 통합을 활성화하기 전에 Adobe Analytics® 및 이메일 소프트웨어 배포에 대해 다음 항목을 검토하십시오.
title: 이 통합을 활성화하기 전에
uuid: fdc762bc-24e3-4c0a-904d-d4be2a4f3a20
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 이 통합을 활성화하기 전에 {#before-you-activate-this-integration}

이 통합을 활성화하기 전에 Adobe Analytics® 및 이메일 소프트웨어 배포에 대해 다음 항목을 검토하십시오.

이렇게 하면 활성화 전에 적절한 우수 사례와 사전 요구 사항이 준비되므로 최적화되고 성공적인 통합이 이루어지도록 할 수 있습니다.

## Adobe Analytics 요구 사항 {#adobe-analytics-requirements}

Adobe Analytics와 관련된 이 Data Connectors 통합에 대한 다음 정보를 검토하십시오.

* **보고서 세트별**: 이 통합은 보고서 세트별로 다르므로 주의하십시오. 통합을 활성화하기 전에 원하는 보고서 세트를 선택하고 보고서 세트에 데이터가 포함되어 있는지 확인합니다.
* **사용 가능하고 구성된 Analytics 변수:** 이 통합에는 10개의 사용자 지정 이벤트와 1개의 사용자 지정 eVar가 필요합니다. [Analytics 통합 변수](appfigures-before-activation.md#analytics-integration-variables)를 참조하십시오.

* **라이브 데이터로 초기화된 보고서 세트:** 이 통합을 위해 완전히 새로운 보고서 세트를 만드는 경우 라이브 추적 appFigures 요구 사항을 통해 일부(1개 이상의 히트) 데이터를 수신해야 합니다. 라이브 데이터가 기록되지 않은 경우 보고서 세트가 통합된 앱스토어 데이터를 받을 준비가 되지 않습니다.

* **앱스토어와 기존 통합:** 이 통합은 과거 13개월 동안의 데이터를 채웁니다. 이전에 제공했던 모든 앱스토어 데이터 공급자와 겹치지 않도록 appFigures 담당자에게 문의하십시오. 데이터를 마지막으로 받은 날짜를 알려주십시오. appFigures는 그에 따라 채우기 기간을 조정합니다.

## appFigures 요구 사항{#appfigures-requirements}

appFigures와 관련된 이 Data Connectors 통합에 대한 다음 정보를 검토하십시오.

* **appFigures의 현재 고객:** 이 통합을 사용하려면 Adobe 및 appFigures의 사용자가 되어야 합니다. 현재 appFigures Enterprise Plan의 사용자가 아닌 경우 통합 마법사를 완료하는 데 필요한 정보가 없습니다. 자세한 내용은 웹의 appFigures를 참조하십시오.
* **appFigures 계정 키:** appFigures Data Connector를 활성화하려면 appFigures 계정 키가 필요합니다. 이 계정 키는 &quot;추가 기능&quot; 섹션에서 생성할 수 있습니다. 자세한 내용은 [통합 구성](../appfigures-overview/t-appfigures-integration.md)을 참조하십시오.

* **데이터 확정**: 다운로드, 판매 및 등급 정보는 이전 7일 간 매일 동기화됩니다. 7일 이후 데이터는 확정으로 간주되며 더 이상 업데이트되지 않습니다.

## 가격 책정{#pricing}

이 Data Connectors 통합에는 알아야 하는 가격 고려사항이 포함됩니다.

다음 섹션에는 추가 정보가 포함됩니다.

### Adobe 가격 고려사항 {#section-2d1c79c895a5479bad8fdd97961ba6a3}

현재 이 통합을 활성화하는 데 드는 비용은 없습니다. 그러나 데이터 소스 가져오기 때문에 서버 호출이 약간 증가할 수 있습니다.

### appFigures 가격 고려사항 {#section-c6afad08c34b43e3a7a3637eea3328c3}

현재 이 통합과 관련된 비용이 없습니다. 이 통합은 현재 기업 고객에게만 제공됩니다. 자세한 내용은 [appFigures에 문의](https://appfigures.com/support/contact)하십시오.

## Analytics 통합 변수{#analytics-integration-variables}

appFigures용 Data Connectors 통합은 Analytics 변수를 사용하여 다양한 appFigures 지표를 추적합니다.

아래 표는 appFigures 통합을 위해 자동으로 활성화된 Analytics 변수를 설명합니다.

### 필수 변수 {#section-3ca8dc46bab0436cba0c9ef827c8356a}

>[!NOTE] 이 통합에서는 앱스토어 데이터에 전용 변수를 사용하므로 사용자 지정 상거래 변수 및 이벤트를 할당할 필요가 없습니다.

| 변수 유형 |  이름  | 채우기 방법 | 설명 |
|---|---|---|---|
| eVar | 앱스토어 개체 ID | appFigures에서 가져옵니다. | 방문 유효 기간, 가장 최근 할당 및 기본 하위 관계로 이 eVar를 구성합니다. |
| event (numeric) | 앱스토어 다운로드 | appFigures에서 가져옵니다. | 모바일 애플리케이션 다운로드 수. |
| event (numeric) | 앱스토어 구매(인앱) | appFigures에서 가져옵니다. | 인앱 구매 및 구독 수입니다. |
| event (numeric) | 앱스토어 등급 | appFigures에서 가져옵니다. | 평균 appFigures 계산된 지표를 정의하는 데 사용됩니다. 직접 사용되지 않습니다. |
| event (numeric) | 앱스토어 등급 분류기 | appFigures에서 가져옵니다. | 평균 appFigures 계산된 지표를 정의하는 데 사용됩니다. 직접 사용되지 않습니다. |
| event (numeric) | 앱스토어 등급 | appFigures에서 가져옵니다. | 평균 appFigures 계산된 지표를 정의하는 데 사용됩니다. 직접 사용되지 않습니다. |
| event (numeric) | 앱스토어 등급 분류기 | appFigures에서 가져옵니다. | 평균 appFigures 계산된 지표를 정의하는 데 사용됩니다. 직접 사용되지 않습니다. |
| event (currency) | 앱스토어 매출(인앱) | appFigures에서 가져옵니다. | 인앱 매출액에서 스토어 비용을 제한 금액입니다. |
| event (currency) | 앱스토어 매출(일회성) | appFigures에서 가져옵니다. | 앱 구매로 발생한 총 매출에서 스토어 비용을 제한 금액입니다. |
| event (currency) | 앱스토어 로열티(인앱) | appFigures에서 가져옵니다. | 사용되지 않습니다 |
| event (currency) | 앱스토어 로열티(일회성) | appFigures에서 가져옵니다. | 사용되지 않습니다 |
