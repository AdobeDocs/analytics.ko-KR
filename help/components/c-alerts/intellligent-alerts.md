---
description: 지능형 경고 시스템은 경고를 더욱 세밀하게 제어할 수 있으며 예외 항목 탐지 기능을 경고 시스템과 통합합니다.
title: 지능형 경고
feature: Alerts
exl-id: 1b23211e-7632-4b33-a27d-c58b3bbbbab1
source-git-commit: be5a73347d417c8dc6667d4059e7d46ef5f0f5cd
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 68%

---

# 지능형 경고

지능형 경고 시스템은 경고를 더욱 세밀하게 제어할 수 있으며 예외 항목 탐지 기능을 경고 시스템과 통합합니다.

다음은 비디오 개요입니다.

>[!VIDEO](https://video.tv.adobe.com/v/25446/?quality=12)

## 개요 {#section_6AC8CA81DEA94E99B0F192B60D0FDF03}

>[!IMPORTANT]
>
>지능형 경고는 Adobe [!DNL Analytics] Prime 및 Adobe [!DNL Analytics] Ultimate 고객만 사용할 수 있습니다.

지능형 경고를 사용하면 다음 작업을 수행할 수 있습니다.

* 예외 항목을 기반으로 한 경고를 만듭니다(90%, 95%, 99%, 99.75%, 및 99.9% 임계값, % 변경률, 초과/미만).
* 경고가 트리거되는 빈도를 미리 봅니다.
* 자동 생성된 Analysis Workspace 프로젝트에 대한 링크가 있는 이메일 또는 SMS로 경고를 보냅니다.
* 하나의 경고에서 여러 지표를 캡처하는 &quot;누적된&quot; 경고를 생성합니다.

경고 시스템의 구성 요소에는 경고 빌더, 경고 관리자, 경고 미리보기 및 경고 작성에 대한 더 나은 컨텍스트 내 액세스 기능이 포함됩니다. 이전 경고 시스템 사용자 인터페이스는 더 이상 사용할 수 없지만, 경고는 마이그레이션됩니다. 일부 이전 경고 기능은 [더 이상 사용할 수 없습니다](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/alerts.html?lang=ko-KR).

경고 빌더로 이동하는 방법에는 세 가지가 있습니다.

* Analysis Workspace에서 다음의 단축키 사용:

  `ctrl (or cmd) + shift + a`
* 경고 빌더로 이동: **[!UICONTROL 작업 영역]** > **[!UICONTROL 구성 요소]** > **[!UICONTROL 새 경고]**.
* 하나 이상의 자유 형식 테이블 라인 항목을 선택하고, 마우스 오른쪽 버튼으로 클릭한 다음, **[!UICONTROL 선택 항목으로 경고 만들기 선택]**. 이렇게 하면 경고 빌더가 열리고, 테이블에서 적용된 적절한 지표와 필터로 빌더가 사전에 채워집니다. 그런 다음 필요할 경우 경고를 편집할 수 있습니다.

  ![](assets/create-alert-from-selection.png)


## FAQ: 경고를 계산하고 트리거하는 방법 {#trigger}

% 임계값은 표준 편차입니다. 예를 들어 95% = 2 표준 편차와 99% = 3 표준 편차가 있습니다. 선택한 시간 세부기간에 따라 [다양한 모델](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md)을 사용하여 각 데이터 포인트가 기준(norm)에서 얼마나 떨어져 있는지(표준 편차 수) 계산합니다. 낮은 임계값(예: 90%)을 설정하면 높은 임계값(99%)을 설정하는 경우보다 많은 예외 항목이 생깁니다. 99.75% 및 99.99% 임계값은 많은 예외 항목을 트리거되지 않도록 시간 단위용으로 특별히 도입되었습니다.

+++ 경고의 예외 항목 탐지는 데이터 예외 항목을 결정하기 위해 얼마나 오래 전으로 이동합니까?

교육 기간은 선택한 세부기간에 따라 다릅니다. 자세한 내용은 <a href="/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md">예외 항목 탐지</a>에서 사용되는 통계 기법을 참조하십시오. 다음은 요약입니다.

* 월 단위 = 15개월 + 지난 해와 동일한 범위
* 주 단위 = 15주 + 지난 해와 동일한 범위
* 일 단위 = 35일 + 지난 해와 동일한 범위
* 시간 단위 = 336시간

+++

+++ 비헤이비어의 급감이나 비헤이비어의 급증에 대해서만 알림을 받으려면 예외 항목 기능을 사용할 수 있습니까, 아니면 절대값을 사용해야 합니까?

절대값을 사용하면 급등은 물론 급등에 대한 경고를 계속 트리거할 수 있습니다. 하락 또는 급등에 대해서만 경고를 분리할 수 없습니다.

+++

+++ 그날의 특정 시간 동안 (예: 업무 시간과 비업무 시간)만 트리거하도록 경고를 구성할 수 있습니까?

현재는 할 수 없습니다.

+++

+++ 점선을 구성하는 &quot;예상값&quot; 테이블이나 그러한 값에 대한 일종의 출력을 얻을 수 있습니까?

Workspace에서는 사용할 수 없지만 Report Builder에서는 사용할 수 있습니다. Report Builder의 예외 항목 탐지에서 [이 비디오](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/exporting/report-builder/anomaly-detection-in-report-builder.html?lang=ko-KR)를 참조하세요.

Report Builder는 보다 덜 복잡한 예외 항목 탐지 방법을 사용한다는 점을 기억하십시오. 고정된 30일 교육 기간, 고정된 95% 간격을 사용합니다.

+++
