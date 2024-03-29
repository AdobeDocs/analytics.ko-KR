---
description: 새로운 지능형 경고 시스템에서는 경고를 더욱 세밀하게 제어할 수 있으며 예외 항목 탐지 기능이 경고 시스템과 통합됩니다.
title: 지능형 경고 개요
feature: Alerts
role: User, Admin
exl-id: 49d47896-bf93-4960-b647-2765c935eb25
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 88%

---

# 지능형 경고 개요

지능형 경고는 경고를 더욱 세밀하게 제어할 수 있도록 해 주며 예외 항목 탐지 기능이 경고 시스템과 통합됩니다.

[지능형 경고](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/data-science/intelligent-alerts.html?lang=ko-KR)에 대한 비디오 튜토리얼 (5:34)

## 개요

지능형 경고를 사용하면 다음 작업을 수행할 수 있습니다.

* 예외 항목을 기반으로 한 경고를 만듭니다(90%, 95%, 99%, 99.75%, 및 99.9% 임계값, % 변경률, 초과/미만)
* 경고가 트리거되는 빈도를 미리 봅니다.
* 자동 생성된 Analysis Workspace 프로젝트에 대한 링크가 있는 이메일 또는 SMS로 경고를 보냅니다.
* 하나의 경고에서 여러 지표를 캡처하는 &quot;누적된&quot; 경고를 생성합니다.

경고 빌더로 이동하는 방법에는 세 가지가 있습니다.

| 메서드 | 세부 사항 |
| --- | --- |
| 경고 빌더로 직접 이동 | **[!UICONTROL 구성 요소]** > **[!UICONTROL 경고]** |
| 작업 영역에서 키보드 단축키 사용 | `Ctrl + Shift + A` (Windows) 또는 `Cmd + Shift + A` (Mac) |
| 하나 이상의 자유 형식 테이블 라인 항목 선택 | 마우스 오른쪽 버튼을 클릭하고 **[!UICONTROL 선택 항목으로 경고 만들기]**&#x200B;를 선택합니다. 이렇게 하면 [!UICONTROL 경고 빌더]가 열리고 테이블에서 적용된 적절한 지표와 필터가 미리 채워집니다. 그런 다음 필요할 경우 경고를 편집할 수 있습니다. ![선택 항목으로 경고 만들기](assets/create-alert-from-selection.png) |

퍼센트 임계값은 표준 편차입니다. 예를 들어 95% = 2 표준 편차와 99% = 3 표준 편차가 있습니다. 선택한 시간 세부기간에 따라 [다른 모델](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md) 는 각 데이터 포인트가 기준(norm)에서 얼마나 떨어져 있는지(표준 편차 수) 계산하는 데 사용됩니다. 낮은 임계값 (예: 90%)을 설정하면 높은 임계값 (99.75%)을 설정하는 경우보다 많은 예외 항목이 생깁니다.

>[!IMPORTANT]
>
>경고를 생성하는 타임스탬프가 지정된 데이터를 사용하면 경고가 잘못 표시될 수 있습니다. 지능형 경고에는 타임스탬프가 지정되지 않은 데이터를 사용하는 것이 좋습니다.

## 경고 예외 항목 살펴보기

경고에서 예외 항목 탐지를 사용하는 경우 교육 기간은 경고에 대해 선택한 세부기간에 따라 달라집니다.

* 월별 세부기간: 15개월 + 지난해와 동일한 범위
* 주별 세부기간: 15주 + 지난해와 동일한 범위
* 일별 세부기간: 35일 + 지난해와 동일한 범위
* 시간 세부기간: 336시간

자세한 내용은 [예외 항목 탐지에서 사용되는 통계 기법](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md)을 참조하십시오.
