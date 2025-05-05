---
title: 계산된 지표 합계
description: Analysis Workspace의 계산된 지표 합계에 대해 알아봅니다
feature: Calculated Metrics
exl-id: 3e4429de-3e0c-49a5-b32c-3a4d24a29816
source-git-commit: be5a73347d417c8dc6667d4059e7d46ef5f0f5cd
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 89%

---

# Analysis Workspace의 계산된 지표 합계

Analysis Workspace에서 데이터를 볼 때 대부분의 경우 계산된 지표 합계가 표시됩니다. 보고서의 행이 혼합 형식 (예: 십진수와 통화)인 경우와 같이 일부 경우에는 합계를 제공할 수 없습니다.

합계는 표시될 때 종종 서버 측에서 계산되는데, 이것은 합계가 방문 횟수나 방문자 수와 같은 지표에 대한 중복 제거를 수행함을 의미합니다. 특정 상황에서 계산된 지표는 테이블의 행들을 합하여 클라이언트 측에서 생성되는데, 이것은 이 합계가 방문 횟수 또는 방문자 수와 같은 지표에 대한 중복 제거를 수행하지 않음을 의미합니다.  이 문제는 다음 상황에서 발생합니다.

* 자유 형식 테이블에 [정적 행](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md)을 사용하고 **[!UICONTROL 현재 행의 합계로 표시]** 옵션 (기본값)을 선택한 경우
* [도넛 시각화](/help/analyze/analysis-workspace/visualizations/donut.md)에서 숫자가 최대 100%까지 추가되도록 하는 경우

Analysis Workspace의 합계에 대한 자세한 내용은 [Workspace 합계](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.html?lang=ko#static-row-total)를 참조하십시오.
