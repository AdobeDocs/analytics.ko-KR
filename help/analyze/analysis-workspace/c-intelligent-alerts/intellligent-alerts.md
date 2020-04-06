---
description: 새로운 지능형 경고 시스템에서는 경고를 더욱 세밀하게 제어할 수 있으며 예외 항목 탐지 기능이 경고 시스템과 통합됩니다.
title: 지능형 경고 개요
uuid: b9bf75ad-bb6f-49fe-8c55-355ea3c50a71
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 지능형 경고 개요

지능형 경고는 경고를 더욱 세밀하게 제어할 수 있도록 해주며 예외 항목 탐지 기능이 경고 시스템과 통합됩니다.

[지능형 경고 - YouTube](https://www.youtube.com/watch?v=UVH9xr_2REA)(5:34)

## 개요

분석 작업 공간의 새로운 경고 빌더 및 경고 관리자는 보고 및 분석의 기존 경고 기능을 대체합니다. 지능형 경고를 사용하면 다음 작업을 수행할 수 있습니다.

* 예외 항목을 기반으로 한 경고를 만듭니다(90%, 95%, 99%, 99.75%, 및 99.9% 임계값, % 변경률, 초과/미만)
* 경고가 트리거되는 빈도를 미리 봅니다.
* 자동 생성된 Analysis Workspace 프로젝트에 대한 링크가 있는 이메일 또는 SMS로 경고를 보냅니다.
* 하나의 경고에서 여러 지표를 캡처하는 &quot;누적된&quot; 경고를 생성합니다.

경고 빌더를 여는 방법에는 네 가지가 있습니다. 

* 경고 빌더로 직접 이동: **[!UICONTROL Components]** > **[!UICONTROL Alerts]**
* Workspace에서 키보드 단축키 사용: `Ctrl + Shift + A` (Windows) 또는 `Cmd + Shift + A` (Mac)
* Selecting one or more freeform table line item/s, right-clicking and selecting **[!UICONTROL Create Alert from Selection]**. 이렇게 하면 경고 빌더가 열리고 테이블에서 적용된 적절한 지표와 필터가 미리 채워집니다. 그런 다음 필요할 경우 경고를 편집할 수 있습니다.

   ![선택 항목으로 경고 만들기](assets/create-alert-from-selection.png)

* 보고 및 분석 보고서 내에서 > **[!UICONTROL More]** 로 이동합니다 **[!UICONTROL Add Alert]** . 이렇게 하면 경고 빌더가 열리고 보고서에서 적용된 적절한 지표와 필터가 미리 채워집니다. 그런 다음 필요할 경우 경고를 편집할 수 있습니다.

   ![경고 추가](assets/add-alert.png)

퍼센트 임계값은 표준 편차입니다. 예를 들어 95% = 2 표준 편차 및 99% = 3 표준 편차. 선택한 시간 세부기간에 따라 [서로 다른 모델을](../virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md) 사용하여 각 데이터 포인트가 기본값에서 얼마나 멀리(표준 편차 수)되는지 계산합니다. 낮은 임계값(예: 90%)을 설정하면 높은 임계값(99.75%)을 설정하는 경우보다 많은 예외 항목이 생깁니다.

>[!IMPORTANT] 경고를 생성하는 타임스탬프가 지정된 데이터를 사용하면 경고가 잘못 표시될 수 있습니다. 지능형 경고에는 타임스탬프가 지정되지 않은 데이터를 사용하는 것이 좋습니다.

## 경고 예외 항목 살펴보기

경고에서 예외 항목 탐지를 사용하는 경우 교육 기간은 경고에 대해 선택한 세부기간에 따라 달라집니다.

* 월별 세부기간: 15개월 + 지난해와 동일한 범위
* 주별 세부기간: 15주 + 지난해와 동일한 범위
* 일별 세부기간: 35일 + 지난해와 동일한 범위
* 시간 세부기간: 336시간

자세한 내용은 [예외 항목 탐지에서 사용되는 통계 기법](../virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md)을 참조하십시오.
