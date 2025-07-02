---
description: 알림을 세부적으로 제어하고 예외 항목 탐지와 통합할 수 있도록 경고를 사용하는 방법을 이해합니다.
title: 경고 개요
feature: Alerts
exl-id: 1b23211e-7632-4b33-a27d-c58b3bbbbab1
source-git-commit: ff38740116ac6f12033ebdc17cffa3250a30f3f7
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 93%

---

# 경고 개요

Adobe Analytics의 경고 기능을 사용하면 변경된 백분율이나 특정 데이터 포인트에 따라 알림을 받을 수 있습니다.

Adobe Analytics 패키지를 기반으로 예외 항목 임계값에 따라 경고를 트리거하도록 설정할 수도 있습니다. 이러한 경고(“지능형 경고”라고도 함)는 [예외 항목 탐지](/help/analyze/analysis-workspace/c-anomaly-detection/anomaly-detection.md) 기능과 통합하여 필요 시 트리거되는 세부적인 컨트롤을 제공합니다.

경고를 사용하면 다음 작업을 수행할 수 있습니다.

* 경고가 트리거되는 빈도를 미리 봅니다.
* 자동 생성된 Analysis Workspace 프로젝트에 대한 링크가 있는 이메일 또는 SMS로 경고를 보냅니다.
* 하나의 경고에서 여러 지표를 캡처하는 “스택” 경고를 생성합니다.
* 예외 항목(90%, 95%, 99%, 99.75%, 99.9% 임계값, % 변경, 위/아래)를 기반으로 경고를 구축합니다(Select, Prime 또는 Ultimate 패키지가 있는 Adobe Analytics 고객만 사용 가능).

다음 비디오 튜토리얼에서 경고 대한 기본 개요를 제공합니다. [경고](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/data-science/intelligent-alerts.html?lang=ko)&#x200B;(5:34)

## 경고 예외 항목 살펴보기

>[!NOTE]
>
>예외 항목 탐지가 있는 경고 사용(_지능형 경고_)은 Adobe Analytics Prime 또는 Ultimate 패키지를 보유한 조직에서만 사용할 수 있습니다.

경고에서 예외 항목 탐지를 사용하는 경우 교육 기간은 경고에 대해 선택한 세부기간에 따라 달라집니다.

* 월별 세부기간: 15개월 + 지난해와 동일한 범위
* 주별 세부기간: 15주 + 지난해와 동일한 범위
* 일별 세부기간: 35일 + 지난해와 동일한 범위
* 시간 세부기간: 336시간

자세한 내용은 [예외 항목 탐지에서 사용되는 통계 기법](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md)을 참조하십시오.

## 경고 만들기

Adobe Analytics에서 경고를 만드는 방법에 대한 자세한 내용은 [경고 만들기](/help/components/c-alerts/alert-builder.md)를 참조하십시오.

>[!IMPORTANT]
>
>경고를 생성하는 타임스탬프가 지정된 데이터를 사용하면 경고가 잘못 표시될 수 있습니다. 경고에는 타임스탬프가 지정되지 않은 데이터를 사용하는 것이 좋습니다.

## 경고 관리

경고 관리자에서 기존 경고를 관리할 수 있습니다. 경고에 대한 태그 지정, 이름 변경, 삭제 등 다양한 관리 작업을 수행할 수 있습니다.

Adobe Analytics에서 기존 경고를 관리하는 방법에 대한 자세한 내용은 [경고 관리](/help/components/c-alerts/alert-manager.md)를 참조하십시오.
