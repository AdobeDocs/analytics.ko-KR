---
description: 경고 사용방법 이해하기는 알림을 세밀하게 제어하고 예외 항목 탐지와 통합할 수 있도록 해 줍니다.
title: 경고 개요
feature: Alerts
exl-id: 1b23211e-7632-4b33-a27d-c58b3bbbbab1
source-git-commit: f02b660b551f5291443b8f7c5c51179a06b22eb9
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 54%

---

# 경고 개요

Adobe Analytics의 경고 기능을 사용하면 변경된 백분율이나 특정 데이터 포인트에 따라 알림을 받을 수 있습니다.

Adobe Analytics 패키지를 기반으로 예외 항목 임계값에 따라 경고를 트리거하도록 설정할 수도 있습니다. 이러한 경고(*지능형 경고*&#x200B;라고도 함)는 [예외 항목 탐지](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md)와 통합되는 세분화된 제어를 제공하여 가장 필요할 때 트리거합니다.

경고를 사용하면 다음 작업을 수행할 수 있습니다.

* 경고가 트리거되는 빈도를 미리 봅니다.
* 자동 생성된 Analysis Workspace 프로젝트에 대한 링크가 있는 이메일 또는 SMS로 경고를 보냅니다.
* 하나의 경고에서 여러 지표를 캡처하는 *누적된* 경고를 만듭니다.
* 다음 기준에 따라 경고 작성:
   * 존재하는 지표의 예외 항목이 예상 임계값 초과 또는 미만입니다.

     [예외 항목 탐지](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md)는 이전 데이터를 사용하여 예상 값과 상한 및 하한을 빌드합니다. 실제 지표 값이 임계값으로 정의된 상한 또는 하한 미만이면 이 이벤트는 임계값 신뢰 수준에서 예외 항목으로 간주되고 경고를 트리거합니다. 높은 임계값(예: 99% 또는 99.9%)은 더 넓은 대역을 의미하므로 더 극단적인 예외 항목으로 인해 발생하는 경고 수가 줄어듭니다. 낮은 임계값(예: 90%)은 더 좁은 대역을 의미하며, 이로 인해 덜 극단적인 예외로 인해 더 많은 경고가 발생합니다.
   * 특정 비율에 따른 지표 변경.
   * 특정 값 이상, 미만 또는 동일한 지표. (Select, Prime 또는 Ultimate 패키지를 사용하는 Adobe Analytics 고객만 사용 가능)

이 [비디오 튜토리얼](https://experienceleague.adobe.com/ko/docs/analytics-learn/tutorials/data-science/intelligent-alerts)에서는 경고에 대한 기본 개요를 제공합니다.


## 경고 예외 항목 살펴보기

>[!NOTE]
>
>예외 항목 탐지가 있는 경고 사용(_지능형 경고_)은 Adobe Analytics Prime 또는 Ultimate 패키지를 보유한 조직에서만 사용할 수 있습니다.

경고에서 예외 항목 탐지를 사용하는 경우 교육 기간은 경고에 대해 선택한 세부 기간에 따라 달라집니다.

* 월별 세부 기간: 15개월 + 지난해와 동일한 범위
* 주별 세부 기간: 15주 + 지난해와 동일한 범위
* 일별 세부 기간: 35일 + 지난해와 동일한 범위
* 시간 세부 기간: 336시간

자세한 내용은 [예외 항목 탐지에서 사용되는 통계 기법](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md)을 참조하십시오.

## 경고 만들기

Adobe Analytics에서 경고를 만드는 방법에 대한 자세한 내용은 [경고 만들기](/help/components/alerts/alert-builder.md)를 참조하십시오.

>[!IMPORTANT]
>
>경고를 생성하는 타임스탬프가 지정된 데이터를 사용하면 경고가 잘못 표시될 수 있습니다. 경고에는 타임스탬프가 지정되지 않은 데이터를 사용하는 것이 좋습니다.

## 경고 관리

경고 관리자에서 기존 경고를 관리할 수 있습니다. 경고에 대한 태그 지정, 이름 변경, 삭제 등 다양한 관리 작업을 수행할 수 있습니다.

Adobe Analytics에서 기존 경고를 관리하는 방법에 대한 자세한 내용은 [경고 관리](/help/components/alerts/alert-manager.md)를 참조하십시오.
