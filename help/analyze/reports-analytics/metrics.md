---
description: 지표는 보고서의 기반으로, 데이터 관계를 보고 이해하는 데 도움이 되며 웹 사이트에 대한 다양한 데이터 세트를 동시에 비교할 수 있도록 지원합니다. 지표는 보기 수, 클릭스루 횟수, 다시 로드 횟수, 평균 체류 시간, 판매량, 주문 수, 매출액 등과 같은 방문자 활동에 대한 수량 정보입니다.
title: 지표
topic: Reports and analytics
uuid: ae2021eb-8b26-4a98-b7a0-ce36bca46753
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 지표

지표는 보고서의 기반으로, 데이터 관계를 보고 이해하는 데 도움이 되며 웹 사이트에 대한 다양한 데이터 세트를 동시에 비교할 수 있도록 지원합니다. 지표는 보기 수, 클릭스루 횟수, 다시 로드 횟수, 평균 체류 시간, 판매량, 주문 수, 매출액 등과 같은 방문자 활동에 대한 수량 정보입니다.

## 지표

지표는 보고서의 기반으로, 데이터 관계를 보고 이해하는 데 도움이 되며 웹 사이트에 대한 다양한 데이터 세트를 동시에 비교할 수 있도록 지원합니다. 지표는 보기 수, 클릭스루 횟수, 다시 로드 횟수, 평균 체류 시간, 판매량, 주문 수, 매출액 등과 같은 방문자 활동에 대한 수량 정보입니다.

지표와 관련 데이터는 보고서 열에 표시됩니다. 트래픽 지표는 방문자의 볼륨에 대한 데이터를 보여줍니다. 전환 지표는 구매, 다운로드 또는 기타 사용자가 웹 사이트에서 취하려고 하는 모든 동작과 같은 성공 이벤트에 대한 데이터를 보여줍니다. 

[계산된 지표](/help/components/c-calcmetrics/cm-overview.md)는 지표를 결합하여 만들어집니다.

자세한 내용은 [지표 개요](/help/components/c-variables/c-metrics/metricslist.md)를 참조하십시오.

## 기본 보고서 지표 선택

보고서 수준에서 기본 지표를 선택하는 방법을 설명하는 단계입니다.

<!-- 

t_metrics_set_default.xml

 -->

1. 보고서 실행.
1. 기본 지표로 저장할 지표를 추가합니다.
1. 드롭다운 **[!UICONTROL Add Metrics]** 목록을 클릭한 다음 **[!UICONTROL Set as Default]**&#x200B;선택합니다.

   선택한 지표가 이 보고서의 기본값으로 저장됩니다. 다음 정보가 기본 지표에 적용됩니다.

* 기본 지표는 모든 사용자 계정에서 적용되지만 보고서 및 보고서 세트별로 적용됩니다. 예를 들어 같은 보고서 세트의 특정 보고서를 보는 모든 사용자는 이전 절차를 사용하는 지표 집합을 표시합니다.
* 보고서 간에 이동하는 경우 최근에 본 보고서에 표시된 지표가 지속됩니다. To display default metrics in that new report, click the [!UICONTROL Add Metrics] drop-down list, then click [!UICONTROL Show Defaults].

* Clicking [!UICONTROL Clear Defaults] removes the default metrics for that report and reverts them to the original default metrics for that report ( [!UICONTROL Page Views] for props, and whatever you have set in Admin Tools for eVars).

