---
description: 요약 숫자 및 변경 시각화를 사용하여 프로젝트의 중요 데이터 포인트를 표시할 수 있습니다.
title: 요약 번호 및 요약 변경 사항
uuid: 177c1b89-6d98-473d-8447-6b4cdc479565
feature: Visualizations
role: User, Admin
exl-id: d6a08201-ca3a-48ff-983a-3ec6b989deda
source-git-commit: c9299befa63868ce0450af9c63132738474e2371
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 93%

---

# 요약 숫자 및 변경 사항

>[!BEGINSHADEBOX]

_이 문서에서는_ ![AdobeAnalytics](/help/assets/icons/AdobeAnalytics.svg) _&#x200B;**Adobe Analytics**&#x200B;의 요약 번호 및 요약 변경 시각화를 설명합니다._<br/>_이 문서의 [&#128279;](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-workspace/visualizations/summary-number-change)CustomerJourneyAnalytics_ ![Customer Journey Analytics](/help/assets/icons/CustomerJourneyAnalytics.svg) 버전에 대한 _&#x200B;**요약 번호 및 요약 변경**&#x200B;을 참조하세요._

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [요약 숫자 및 요약 변경 시각화](https://video.tv.adobe.com/v/3416890/?quality=12&learn=on&captions=kor){target="_blank"}를 확인하십시오.

>[!ENDSHADEBOX]

## 요약 숫자 {#summary-number}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_summarynumber_button"
>title="요약 숫자"
>abstract="총계와 소계를 보여 주는 시각화를 만듭니다."

<!-- markdownlint-enable MD034 -->

프로젝트에서 중요한 큰 숫자를 강조 표시하려면 ![요약](/help/assets/icons/123.svg) **[!UICONTROL 요약 숫자]** 시각화를 사용하십시오. 이 시각화는 연관된 데이터 소스를 사용하여 다음과 같은 방식으로 작동합니다.

* 셀을 선택하지 않은 경우 열의 합계를 선택합니다.
* 단일 셀을 선택하면 해당 셀의 요약이 표시됩니다.
* 두 개 이상의 셀을 선택하면 선택한 첫 번째 셀이 표시됩니다.
* 열을 선택하면 열의 첫 번째 셀 값이 선택됩니다.

![요약 숫자 시각화](asses/../assets/summary-number.png)

시각화 설정의 일부로 특정 요약 숫자 옵션을 이용할 수 있습니다.

| 옵션 | 정의 |
|--- |--- |
| **[!UICONTROL 값 생략]** | 숫자 값을 지능적으로 축약하도록 **[!UICONTROL 값 생략]**&#x200B;을 선택합니다. 선택하면 숫자를 입력하여 축약 수를 정의합니다. 예:<br/><table><tr><td>**원래 값**</td><td>**축약 값**</td><td>**결과**</td></tr><tr><td>$12,011,141.25</td><td>선택되지 않음</td><td  align="right">$12,011,141.25</td></tr><tr><td>$12,011,141.25</td><td>선택된 경우, `0`으로 설정</td><td align="right">$12M</td></tr><tr><td>$12,011,141.25</td><td> 선택된 경우, `1`로 설정</td><td  align="right">$12.0M</td></tr><tr><td>$12,011,141.25</td><td>선택된 경우, `2`로 설정</td><td align="right">$12.01M</td></tr><tr><td>$12,011,141.25</td><td>선택된 경우, `3`으로 설정</td><td align="right">$12.011M</td></tr></table> |
| **[!UICONTROL 다음을 기준으로 값 요약]** | 선택한 데이터의 최대, 최소, 평균, 중간값 또는 합계를 표시하도록 선택합니다. |

## 요약 변경 {#summary-change}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_summarychange_button"
>title="요약 변경"
>abstract="두 숫자 사이의 델타(변경)를 보여 주는 시각화를 만듭니다."

<!-- markdownlint-enable MD034 -->


![MoveUpDown](/help/assets/icons/MoveUpDown.svg) **[!UICONTROL 요약 변경]** 시각화를 사용하여 두 숫자 간의 델타(변화량)를 표시합니다. <!-- This is applicable for AA, not CJA: The green and red color of the Summary Change can be controlled through [custom event polarity](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/success-events/success-event.html?lang=ko) or a calculated metric's [Show Upward Trend As](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html?lang=ko) option.-->

<!--
The green and red color of the Summary Change can be controlled through [custom event polarity](https://experienceleague.adobe.com/docs/analytics/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md) or a calculated metric's [Show Upward Trend As](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html?lang=ko) option.
-->

이 시각화는 다음과 같은 방식으로 동작합니다.

* 셀을 선택하지 않으면 열의 처음 두 셀 값을 비교합니다.
* 하나의 셀을 선택하면 셀 값을 자신과 비교하기 때문에 0을 표시합니다.
* 두 개의 셀을 선택하면 처음 선택한 셀을 분자로, 두 번째 셀을 분모로 취합니다.
* 세 개 이상의 셀을 선택하면 처음 두 개만 비교합니다.
* 셀 범위를 선택하면 범위에서 선택한 첫 번째 셀과 마지막 셀을 비교합니다.
* 열을 선택하면 첫 번째 값과 자신을 비교하여 0이 표시됩니다.


![두 숫자 사이의 델타를 보여 주는 요약 변경 시각화.](assets/summary-change.png)


시각화 설정의 일부로 특정 **[!UICONTROL 요약 변경 옵션]**&#x200B;을 이용할 수 있습니다.

| 옵션 | 정의 |
|--- |--- |
| **[!UICONTROL 백분율 변경 표시]** | 두 숫자 사이의 퍼센트 변화량을 표시합니다. |
| **[!UICONTROL 원시 차이 표시]** | 두 숫자 사이의 원시 차이를 표시합니다. 이 옵션을 사용하여 값들을 축약하고 소수점 이하 최대 3자리를 표시할 수도 있습니다. |
| **[!UICONTROL 값 생략]** | 변경된 값을 지능적으로 축약하도록 **[!UICONTROL 값 생략]**&#x200B;을 선택합니다. 선택하면 숫자를 입력하여 축약 수를 정의합니다. 예:<br/><table><tr><td>**원래 값**</td><td>**축약 값**</td><td>**결과**</td></tr><tr><td>$12,011,141.25</td><td>선택되지 않음</td><td  align="right">$12,011,141.25</td></tr><tr><td>$12,011,141.25</td><td>선택된 경우, `0`으로 설정</td><td align="right">$12M</td></tr><tr><td>$12,011,141.25</td><td> 선택된 경우, `1`로 설정</td><td  align="right">$12.0M</td></tr><tr><td>$12,011,141.25</td><td>선택된 경우, `2`로 설정</td><td align="right">$12.01M</td></tr><tr><td>$12,011,141.25</td><td>선택된 경우, `3`으로 설정</td><td align="right">$12.011M</td></tr></table> |

>[!MORELIKETHIS]
>
>[패널 내에 시각화 추가](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#add-visualizations-to-a-panel)
>&#x200B;>[시각화 설정](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#settings)
>&#x200B;>[시각화 컨텍스트 메뉴](/help/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.md#context-menu)
>
