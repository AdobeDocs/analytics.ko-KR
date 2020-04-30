---
description: 간단한 "방문당 페이지 보기 수" 지표를 만드는 방법을 표시합니다.
title: 간단한 "방문자 수당 페이지 보기 수" 지표 작성
uuid: 0730e51c-1f8f-473b-8825-d72911f2944c
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# 간단한 &quot;방문자 수당 페이지 보기 수&quot; 지표 작성

간단한 &quot;방문당 페이지 보기 횟수&quot; 지표를 만드는 방법을 표시합니다.

UI 구성 요소에 대한 자세한 설명은 [지표 작성](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md).

다음은 간단한 &quot;방문당 페이지 보기 수&quot; 지표를 만드는 방법입니다.

1. 계산된 지표 빌더로 이동합니다.
1. 지표의 이름을 &quot;방문당 페이지 보기 수&quot; 또는 이와 유사하게 지정합니다.
1. Give it a user-friendly **[!UICONTROL Description]** to show what it&#39;s used for.
1. Select the right **[!UICONTROL Format]**, in this case Decimal.
1. 보고서를 표시할 소수점 이하 자리수를 결정합니다.
1. 지표 극성을 설정합니다. 이 지표의 경우, 증가 트렌드가 좋은(녹색) 것입니다.
1. Add a **[!UICONTROL Tag]** to organize your metrics.
1. 이 지표의 경우, 먼저 페이지 보기 수를 캔버스로 드래그한 다음 그 아래의 방문 수를 드래그합니다(파란색 선이 나타날 때까지 기다렸다가 놓음).
1. 나누기 연산자를 선택합니다. (나누기는 기본 연산자입니다.)
1. You can now see a **[!UICONTROL Preview]** of that metric as you are building it, at the top right.
1. 제품 호환성은 지표가 [현재 데이터](https://docs.adobe.com/content/help/en/analytics/analyze/reports-analytics/current-data.html)와 호환하는지, 완전히 처리된 데이터와만 호환하는지를 보여줍니다.
1. 클릭 **[!UICONTROL Save]**.
1. Notice that the **[!UICONTROL Summary]** formula updates anytime you make a change to the metric definition.
1. 이제 세그먼트 관리자와 유사한 [계산된 지표 관리자](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md)가 자동으로 표시됩니다. 지표를 공유, 승인, (재)태깅, 이름 변경 또는 삭제할 수 있도록 해줍니다.

