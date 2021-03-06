---
description: 간단한 "방문당 페이지 보기 수" 지표를 만드는 방법을 표시합니다.
title: 간단한 "방문자 수당 페이지 보기 수" 지표 작성
feature: Calculated Metrics
exl-id: 2d1c4677-b07c-4eca-97b7-e5e4594daee1
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: ht
source-wordcount: '249'
ht-degree: 100%

---

# 간단한 &quot;방문자 수당 페이지 보기 수&quot; 지표 작성

간단한 &quot;방문당 페이지 보기 횟수&quot; 지표를 만드는 방법을 표시합니다.

UI 구성 요소에 대한 자세한 설명은 [지표 작성](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md).

다음은 간단한 &quot;방문당 페이지 보기 수&quot; 지표를 만드는 방법입니다.

1. 계산된 지표 빌더로 이동합니다.
1. 지표의 이름을 &quot;방문당 페이지 보기 수&quot; 또는 이와 유사하게 지정합니다.
1. 사용자에게 친근한 **[!UICONTROL 설명]**&#x200B;을 지정하여 용도를 알 수 있도록 합니다.
1. 올바른 **[!UICONTROL 공식]**&#x200B;을 선택합니다. 이 경우에는 십진수입니다.
1. 보고서를 표시할 소수점 이하 자리수를 결정합니다.
1. 지표 극성을 설정합니다. 이 지표의 경우, 증가 트렌드가 좋은 (녹색) 것입니다.
1. **[!UICONTROL 태그]**&#x200B;를 추가하여 지표를 정리합니다.
1. 이 지표의 경우, 먼저 페이지 보기 수를 캔버스로 드래그한 다음 그 아래의 방문 수를 드래그합니다(파란색 선이 표시될 때까지 기다렸다가 놓음).
1. 나누기 연산자를 선택합니다. (나누기는 기본 연산자입니다.)
1. 이제 지표를 만들면 오른쪽 상단에서 해당 지표의 **[!UICONTROL 미리보기]**&#x200B;를 볼 수 있습니다.
1. 제품 호환성은 지표가 [현재 데이터](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/current-data.html?lang=ko-KR)와 호환하는지, 완전히 처리된 데이터와만 호환하는지를 보여 줍니다.
1. **[!UICONTROL 저장을 클릭합니다]**.
1. **[!UICONTROL 요약]** 공식은 지표 정의를 변경할 때마다 업데이트됩니다.
1. 이제 세그먼트 관리자와 유사한 [계산된 지표 관리자](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md)가 자동으로 표시됩니다. 지표를 공유, 승인, (재)태깅, 이름 변경 또는 삭제할 수 있도록 해 줍니다.
