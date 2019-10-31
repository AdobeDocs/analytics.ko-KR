---
description: Analysis Workspace 내에서 데이터 예외 항목을 컨텍스트에 따라 보고 분석할 수 있습니다.
seo-description: Analysis Workspace 내에서 데이터 예외 항목을 컨텍스트에 따라 보고 분석할 수 있습니다.
seo-title: 예외 항목 탐지 개요
title: 예외 항목 탐지 개요
uuid: 991fde08-198c-4410-9606-d5a4f3dd8339
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# 예외 항목 탐지 개요

분석 작업 공간 내에서 데이터 예외 항목을 상황에 따라 보고 분석할 수 있습니다.

[YouTube의 예외 항목](https://www.youtube.com/watch?v=krXyQCjXoeU&index=63&list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS) 탐지(4:53)

[YouTube 기여도](https://www.youtube.com/watch?v=MbpeJIADtGk&index=64&list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS) 분석(3:20)

> [!IMPORTANT] 예외 항목 탐지는 분석 작업 공간에서만 사용할 수 있습니다. Adobe Analytics Select 및 Foundation 고객은 작업 공간에서 "일별 세부기간" 예외 항목 감지에 액세스할 수 있습니다. 자세한 내용은 [예외 항목 탐지 및 기여도 분석 권한](../contribution-analysis/ca-tokens.md)을 참조하십시오.

예외 항목 탐지는 이전 데이터에 관해 주어진 지표가 변경되는 방법을 결정하는 통계적 방법을 제공합니다.

예외 항목 탐지 기능을 사용하면 "노이즈"에서 "진짜 신호"를 구분한 다음, 이러한 신호 또는 이상 현상에 기여한 잠재적 요인을 식별하는 데 도움이 됩니다. 다시 말해, 통계적 변동이 문제가 되는지 여부를 식별하게 해줍니다. 그러면 진짜 예외 현상의 근본 원인을 식별할 수 있습니다. 또한 신뢰할 수 있는 지표(KPI) 예측이 가능합니다.

조사할 수 있는 이상 현상의 예에는 다음 내용이 포함됩니다.

* 평균 주문 가격의 급격한 하락
* 매출액이 낮은 주문의 급등
* 평가판 등록 급등 또는 하락
* 랜딩 페이지 보기 수의 하락
* 비디오 버퍼 이벤트의 스파이크
* 낮은 비디오 비트율의 스파이크

Analysis Workspace에서 예외 항목 탐지 및 [기여도 분석](https://marketing.adobe.com/resources/help/en_US/analytics/contribution/ca_main.html) 기능은 모두 핵심 워크플로우입니다. 매일 발생하는 임의의 예외 항목에 대해 [기여도 분석]을 실행하고 Analysis Workspace 프로젝트에 그 결과를 포함할 수 있습니다.

Analysis Workspace의 예외 항목 탐지 알고리즘에 포함된 기능은 다음과 같습니다.

* 기존의 일별 세부 기간 이외에 시간별, 주별 및 월별 세부 기간 지원.
* 계절적 영향(예: "블랙 프라이데이") 및 휴일 인식.
