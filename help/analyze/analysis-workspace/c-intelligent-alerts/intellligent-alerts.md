---
description: 새로운 인텔리전트 경고 시스템에서는 경고를 더욱 세밀하게 제어할 수 있으며 예외 항목 탐지 기능이 경고 시스템과 통합됩니다.
seo-description: 새로운 인텔리전트 경고 시스템에서는 경고를 더욱 세밀하게 제어할 수 있으며 예외 항목 탐지 기능이 경고 시스템과 통합됩니다.
seo-title: 지능형 경고 개요
title: 지능형 경고 개요
uuid: b9bf75ad-bb6f-49fe-8c55-355ea3c50a71
translation-type: tm+mt
source-git-commit: ca9f1ed00295b556250894ae4e7fa377ef8a593d

---


# 지능형 경고 개요

지능형 경고를 사용하면 경고를 보다 세밀하게 제어할 수 있으며 예외 항목 탐지를 경고 시스템과 통합할 수 있습니다.

[YouTube에 대한](https://www.youtube.com/watch?v=UVH9xr_2REA) 지능형 경고(5:34)

## 개요

Analysis Workspace의 새로운 경고 빌더와 경고 관리자는 Reports &amp; Analytics에 있는 기존의 경고 기능을 대체합니다. 지능형 경고를 사용하면 다음 작업을 수행할 수 있습니다.:

* 예외 항목을 기반으로 한 경고를 만듭니다(90%, 95%, 99%, 99.75%, 및 99.9% 임계값, % 변경, 초과/미만)
* 경고가 트리거되는 빈도를 미리 봅니다
* 자동 생성된 Analysis Workspace 프로젝트에 대한 링크가 있는 이메일 또는 SMS로 경고를 보냅니다
* 하나의 경고에서 여러 지표를 캡처하는 "누적된" 경고를 생성합니다

경고 빌더를 여는 방법에는 네 가지가 있습니다. 

* 경고 빌더로 직접 이동: 구성 **[!UICONTROL 요소]** &gt; **[!UICONTROL 경고]**
* 작업 공간에서 키보드 단축키 사용: `Ctrl + Shift + A` (Windows) 또는 `Cmd + Shift + A` (Mac)
* Selecting one or more freeform table line item/s, right-clicking and selecting **[!UICONTROL Create Alert from Selection]**. 그러면 경고 빌더가 열리고 테이블에서 적용된 적절한 지표와 필터가 미리 채워집니다. 필요한 경우 경고를 편집할 수 있습니다.

   ![선택 항목으로 경고 만들기](assets/create-alert-from-selection.png)

* From within a Reports &amp; Analytics report, by going to  **[!UICONTROL More]** &gt; **[!UICONTROL Add Alert]** . 이렇게 하면 경고 빌더가 열리고 보고서에서 적용된 적절한 지표와 필터가 미리 채워집니다. 필요한 경우 경고를 편집할 수 있습니다.

   ![경고 추가](assets/add-alert.png)

백분율 임계값은 표준 편차입니다. 예를 들어, 95% = 2 표준 편차와 99% = 3 표준 편차가 있습니다. 선택한 시간 단위에 따라 [다양한 모델](../virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md)을 사용하여 각 데이터 포인트가 기준(norm)에서 얼마나 떨어져 있는지(표준 편차 수) 계산합니다. 하한 임계값(예: 90%)을 설정하면 더 높은 임계값(99.75%)을 설정하는 경우보다 이상 예외 항목이 더 많이 발생합니다.

> [!IMPORTANT] 타임스탬프가 지정된 데이터를 사용하여 경고를 만들면 경고가 잘못 실행될 수 있습니다. Adobe에서는 지능형 경고에 타임스탬프가 지정되지 않은 데이터를 사용하는 것이 좋습니다.

## 예외 항목 경고 확인

경고에서 예외 항목 탐지를 사용하는 경우 교육 기간은 경고에 대해 선택한 세부기간에 따라 달라집니다.

* 월별 세부기간:15개월 + 작년에 동일한 범위
* 주별 세부기간:15주 + 작년 동일 범위
* 일별 세부기간:35일 + 작년 동일 범위
* 시간별 세부기간:336시간

See [Statistical techniques used in Anomaly Detection](../virtual-analyst/c-anomaly-detection/statistics-anomaly-detection.md) for more information.
