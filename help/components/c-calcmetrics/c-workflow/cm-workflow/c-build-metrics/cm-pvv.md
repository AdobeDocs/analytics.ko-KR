---
description: 간단한 "방문당 페이지 보기 수" 지표를 만드는 방법을 표시합니다.
title: 간단한 "방문자 수당 페이지 보기 수" 지표 작성
feature: Calculated Metrics
exl-id: 2d1c4677-b07c-4eca-97b7-e5e4594daee1
source-git-commit: 7722a2f01ff77dfec8ce110fd04fe977f6c627c6
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 56%

---

# “방문자 수당 페이지 조회수” 지표 작성

다음 정보는 간단한 &quot;방문자 수당 페이지 보기 수&quot; 지표를 만드는 방법을 설명합니다.

간단한 &quot;방문자 수당 페이지 보기 수&quot; 지표를 만들려면:

1. [지표 작성](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md)에 설명된 대로 지표 작성을 시작합니다.
1. 지표의 이름을 &quot;방문당 페이지 보기 수&quot; 또는 이와 유사하게 지정합니다.
1. 사용자에게 친근한 **[!UICONTROL 설명]**&#x200B;을 지정하여 용도를 알 수 있도록 합니다.
1. 올바른 **[!UICONTROL 형식]**&#x200B;을(를) 선택하십시오. 이 예제에서는 [!UICONTROL **십진수**]&#x200B;를 선택합니다.
1. 보고서를 표시할 소수점 이하 자리수를 결정합니다.
1. [!UICONTROL **증가 트렌드를**](으)로 표시 드롭다운 메뉴에서 [!UICONTROL **양호(녹색)**]&#x200B;을(를) 선택합니다.
1. **[!UICONTROL 태그]**&#x200B;를 추가하여 지표를 정리합니다.
1. 이 지표의 경우, 먼저 페이지 보기 수를 캔버스의 [!UICONTROL **정의**] 섹션으로 드래그한 다음 그 아래로 방문 수를 드래그합니다(파란색 선이 나타날 때까지 기다렸다가 놓음).
1. 나누기 연산자를 선택합니다. (나누기는 기본 연산자입니다.)
1. 이제 지표를 만들면 오른쪽 상단에서 해당 지표의 **[!UICONTROL 미리보기]**&#x200B;를 볼 수 있습니다.
1. 제품 호환성은 지표가 [현재 데이터](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/current-data.html?lang=ko-KR)와 호환하는지, 완전히 처리된 데이터와만 호환하는지를 보여 줍니다.
1. **[!UICONTROL 저장]**&#x200B;을 선택합니다.

   **[!UICONTROL 요약]** 공식은 지표 정의를 변경할 때마다 업데이트된다는 점을 참고하십시오.

1. (선택 사항) 지표를 공유, 승인, (재)태깅, 이름 변경 또는 삭제하려면 [계산된 지표 페이지](/help/components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md)(으)로 이동하십시오.
