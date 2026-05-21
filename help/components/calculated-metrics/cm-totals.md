---
title: 계산된 지표 합계
description: Analysis Workspace의 계산된 지표 합계에 대해 알아봅니다
feature: Calculated Metrics
exl-id: 3e4429de-3e0c-49a5-b32c-3a4d24a29816
TQID: https://experienceleague.adobe.com/3UJF1Hl3nLqjYAiQuvcE4Jpq26MaTgeba5BmnVfvEps
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: c153fd90-23e1-4614-81d3-3cc7571227f7
subfeature_v2: id: b0a1f9d5-5795-42a3-a6d0-bd0e2748fd06id: dcae653e-62c6-4cc8-84e6-ee110b848296id: e318d41c-1d01-4c1e-9b18-1f61d435ceeeid: ef60b66e-5984-4336-ba72-6d978b1b6f87id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: ff16e07c7a2b75e9c6cc09e8255a7ea7e4c6f0c8
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 94%

---

# 계산된 지표 합계

Analysis Workspace에서 데이터를 볼 때 대부분의 경우 계산된 지표 합계가 표시됩니다. 보고서의 행이 혼합 형식 (예: 십진수와 통화)인 경우와 같이 일부 경우에는 합계를 제공할 수 없습니다.

합계는 표시될 때 종종 서버 측에서 계산되는데, 이것은 합계가 방문 횟수나 방문자 수와 같은 지표에 대한 중복 제거를 수행함을 의미합니다. 특정 상황에서 계산된 지표는 테이블의 행들을 합하여 클라이언트 측에서 생성되는데, 이것은 이 합계가 방문 횟수 또는 방문자 수와 같은 지표에 대한 중복 제거를 수행하지 않음을 의미합니다. 이 문제는 다음 상황에서 발생합니다.

* 자유 형식 테이블에 [정적 행](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md)을 사용하고 **[!UICONTROL 현재 행의 합계로 표시]** 옵션 (기본값)을 선택한 경우
* [도넛 시각화](/help/analyze/analysis-workspace/visualizations/donut.md)에서 숫자가 최대 100%까지 추가되도록 하는 경우

Analysis Workspace의 합계에 대한 자세한 내용은 [Workspace 합계](/help/analyze/analysis-workspace/visualizations/freeform-table/workspace-totals.md#static-row-total)를 참조하십시오.
