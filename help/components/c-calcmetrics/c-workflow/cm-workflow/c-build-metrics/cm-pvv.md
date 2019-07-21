---
description: 간단한 "방문당 페이지 보기 횟수" 지표를 만드는 방법을 표시합니다.
seo-description: 간단한 "방문당 페이지 보기 횟수" 지표를 만드는 방법을 표시합니다.
seo-title: 간단한 "방문당 페이지 보기 횟수" 지표 작성
title: 간단한 "방문당 페이지 보기 횟수" 지표 작성
uuid: 0730 E 51 C -1 F 8 F -473 B -8825-D 72911 F 2944 C
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 간단한 "방문당 페이지 보기 횟수" 지표 작성

간단한 "방문당 페이지 보기 횟수" 지표를 만드는 방법을 표시합니다.

UI 구성 요소에 대한 자세한 설명은 [지표 작성](../../../../../components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/cm-build-metrics.md#concept_5EC82A91EB9C44FC870326C85F9D0B18).

다음은 간단한 "방문당 페이지 보기 횟수" 지표를 만드는 방법입니다.

1. 계산된 지표 빌더로 이동합니다.
1. 지표의 이름을 "방문당 페이지 보기 횟수" 또는 이와 유사하게 지정합니다.
1. 사용자에게 친근한 **[!UICONTROL 설명]을 지정하여 용도를 알 수 있도록 합니다.**
1. Select the right **[!UICONTROL Format]**, in this case Decimal.
1. 보고서를 표시할 소수점 이하 자릿수를 결정합니다.
1. 지표 극성을 설정합니다. 이 지표의 경우, 증가 트렌드가 좋은(녹색) 것입니다.
1. **[!UICONTROL 태그]를 추가하여 지표를 정리합니다.**
1. 이 지표의 경우, 먼저 [페이지 보기 횟수]를 캔버스로 드래그한 다음 그 아래의 [방문 횟수]를 드래그합니다(파란색 선이 나타날 때까지 기다렸다가 놓음).
1. 나누기 연산자를 선택합니다. (나누기는 기본 연산자입니다.)
1. 이제 지표를 만들면 오른쪽 상단에서 해당 지표의 **[!UICONTROL 미리 보기]를 볼 수 있습니다.**
1. 제품 호환성은 지표가 [현재 데이터](https://marketing.adobe.com/resources/help/en_US/reference/data_latency.html)와 호환하는지, 완전히 처리된 데이터와만 호환하는지를 보여줍니다.
1. **[!UICONTROL 저장을 클릭합니다]**.
1. **[!UICONTROL 요약]공식은 지표 정의를 변경할 때마다 업데이트됩니다.**
1. You are now automatically taken to the [Calculated Metric Manager](../../../../../components/c-calcmetrics/c-workflow/cm-workflow/cm-manager.md#concept_BA6815CB06D842D5825766396B691653), which is similar to the Segment Manager. 지표를 공유, 승인, (재)태깅, 이름 변경 또는 삭제할 수 있도록 해줍니다.

