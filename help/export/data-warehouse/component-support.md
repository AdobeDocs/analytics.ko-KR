---
title: Data Warehouse의 구성 요소 지원
description: Data Warehouse에서 사용할 수 있는 추가 차원 및 지표와 지원되지 않는 항목을 알아봅니다.
feature: Data Warehouse
exl-id: ce7411a4-a720-47b7-90d5-4d867eff4bae
source-git-commit: d929e97a9d9623a8255f16729177d812d59cec05
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 60%

---

# Data Warehouse의 구성 요소 지원

Data Warehouse 아키텍처의 고유한 처리를 통해 Adobe Analytics의 다른 기능에서 일반적으로 사용할 수 없는 일부 구성 요소를 사용할 수 있습니다. 고유한 아키텍처로 인해 일부 구성 요소는 보고서나 세그먼트에서 사용할 수 없습니다. 이 페이지에서 사용할 수 있는 것과 사용할 수 없는 것을 파악합니다.

## Data Warehouse에 고유한 구성 요소

Adobe Analytics에서 다른 기능을 사용할 때는 Data Warehouse에 사용할 수 있는 일부 차원과 지표를 사용할 수 없습니다.

### 전용 차원 지원

* **Experience Cloud ID**: ECID(Experience Cloud ID 서비스)를 사용하는 구현의 경우 연결된 두 개의 64비트 숫자로 구성된 128비트 숫자를 19자리로 채워줍니다.
* **페이지 URL**: 히트가 발생한 페이지 URL.
* **구매 ID**: purchaseID 변수를 사용하여 설정한 구매에 대한 고유 식별자입니다.
* **방문자 ID**: 방문자에 대한 고유 식별자를 제공합니다. 이 값은 데이터 피드에서 `visid_high` 및 `visid_low` 열의 연결된 값과 동일합니다. 자세한 내용은 데이터 피드 아래의 [데이터 열 참조](../analytics-data-feed/c-df-contents/datafeeds-reference.md)를 참조하십시오.

### 전용 지원 지표

* **방문 횟수**: Data Warehouse 컨텍스트에서 이 지표는 비영구 쿠키 방문 횟수를 제외합니다.
* **방문 횟수 - 모든 방문자 수**: Data Warehouse 컨텍스트에서 이 지표는 Adobe Analytics 내의 다른 도구에 있는 방문 횟수 지표와 더 가깝게 일치합니다.

## Data Warehouse에서 지원되지 않는 구성 요소

일부 차원 및 지표는 Data Warehouse에서 지원되지 않습니다.

>[!NOTE]
>
>차원 또는 지표가 Data Warehouse에서 지원되지 않는 경우 이러한 구성 요소를 사용하는 세그먼트도 지원되지 않습니다. 세그먼트를 만들거나 편집할 때 항상 제품 호환성을 확인하십시오.

### 차원이 지원되지 않음

* 오전/오후
* 다음을 포함한 일부 경로 지정 기반 차원:
   * 시작 페이지를 제외한 모든 시작 차원
   * 종료 페이지 및 종료 링크를 제외한 모든 종료 차원
   * 히트 깊이
   * 반환 주기
   * 이벤트까지 남은 시간
   * 페이지 체류 시간 - 버킷 지정됨
   * 방문당 체류 시간 - 그룹화됨
* 모든 검색 페이지 등급
* 계층 변수
* 히트 유형
* 페이지를 찾을 수 없음(차원으로 사용 가능, 세그멘테이션을 지원하지 않음)
* 유료 검색
* 단일 페이지 방문 횟수
* 옵트아웃 이유 추적
* 미국 주

### 지표가 지원되지 않음

* 다음을 포함한 일부 경로 지정 기반 지표:
   * 바운스 수
   * 항목
   * 종료
   * 다시 로드
   * 단일 액세스
   * 체류 시간 지표
* 기여도 지표([기여도 지표 작성](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/participation-metric.md)에 설명되어 있음)

### 다른 방식으로 지원되는 Dimension

다음 시간 기반 차원이 지원됩니다. 단, 이들 차원을 사용할 때 날짜 출력은 표준이 아닙니다. 구체적으로 해당 연도는 1900년까지 상쇄되며, 월은 0을 기준으로 한다.

* 년
* 분기
* 월
* 주
* 일
* 시간
* 분

## Data Warehouse에서 차원으로서의 세그먼트

Data Warehouse에서 세그먼트를 차원으로 사용하면 보고서는 `"0"` 또는 `"1"`가 포함된 열을 반환합니다.

* **`"0"`**: 차원 항목이 세그먼트의 기준을 충족하지 않았습니다.
* **`"1"`**: 차원 항목이 세그먼트의 기준을 충족했습니다.
