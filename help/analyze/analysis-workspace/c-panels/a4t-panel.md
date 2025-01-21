---
description: A4T (Analytics for Target) 패널을 사용하면 Analysis Workspace에서 Adobe Target 활동 및 경험을 분석할 수 있습니다.
title: A4T (Analytics for Target) 패널
feature: Panels
role: User, Admin
exl-id: 36bca104-37b8-43c6-b8d0-b607a9a333cc
source-git-commit: 2aaa8c0d13755b40ec701ca6342ab773103a0422
workflow-type: tm+mt
source-wordcount: '1132'
ht-degree: 43%

---

# Analytics for Target 패널 {#analyze-for-target-panel}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_a4t_button"
>title="Target용 Analytics"
>abstract="Analysis Workspace에서 타겟 활동 및 경험을 분석합니다."

<!-- markdownlint-enable MD034 -->

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="workspace_a4t_panel"
>title="Analytics for Target 패널"
>abstract="Analysis Workspace에서 타겟 활동 및 경험을 분석합니다.<br/><br>**매개 변수&#x200B;**<br/>**Target 활동**: 분석되는 Target 활동입니다.<br/>**제어 경험**: 선택한 Target 활동에 대한 제어 경험입니다.<br/>**지표 정규화**: 방문자, 방문 또는 노출 횟수. 이 지표 (계산 방법이라고도 함)는 상승도 계산의 분모가 됩니다. 이는 신뢰도 계산이 적용되기 전에 데이터가 종합되는 방식에도 영향을 줍니다.<br/>**성공 지표**: Target 활동을 분석할 최대 3개의 표준(계산되지 않은) 성공 지표입니다."

<!-- markdownlint-enable MD034 -->

>[!BEGINSHADEBOX]

_이 문서에서는_ ![AdobeAnalytics](/help/assets/icons/AdobeAnalytics.svg) _**Adobe Analytics**&#x200B;의 Analytics for Target 패널에 대한 문서를 제공합니다._<br/>_다양한 사용자 경험, 마케팅 또는 메시징의 변화를 비교하는 방법에 대한 자세한 내용은 [실험 패널](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/panels/a4t-panel)을 참조하세요_ ![CustomerJourneyAnalytics](/help/assets/icons/CustomerJourneyAnalytics.svg) _**Customer Journey Analytics**._

>[!ENDSHADEBOX]

Analytics for Target 패널을 사용하면 Analysis Workspace에서 Adobe Target 활동 및 경험을 분석할 수 있습니다. 또한 패널을 통해 최대 3개의 성공 지표에 대한 상승도 및 신뢰도를 확인할 수 있습니다. Analytics for Target 패널에 액세스하려면 Analytics for Target 구성 요소가 활성화된 보고서 세트로 이동합니다. 그런 다음 맨 왼쪽에 있는 패널 아이콘을 선택하고 Analytics for Target 패널을 Analysis Workspace 프로젝트로 드래그합니다.

+++다음은 Analytics for Target 패널에 대한 짧은 비디오 개요입니다.

>[!VIDEO](https://video.tv.adobe.com/v/37247/?quality=12)

+++

## 사용

**[!UICONTROL Analytics for Target]** 패널을 사용하려면:

1. **[!UICONTROL Analytics for Target]** 패널을 만듭니다. 패널을 만드는 방법에 대한 자세한 내용은 [패널 만들기](panels.md#create-a-panel)를 참조하십시오.

1. 패널의 [입력](#panel-input)을 지정합니다.

1. 패널의 [출력](#panel-output)을 확인합니다.

### 패널 입력 {#panel-nput}

다음 입력 설정을 사용하여 Analytics for Target 패널을 구성할 수 있습니다.

![A4T 패널 입력](assets/a4t-panel-input.png)

| 설정 | 설명 |
|---|---|
| **[!UICONTROL 타겟 활동]** | 대상 활동 목록에서 을 선택합니다. 이 목록은 최소 1개의 히트가 있는 최근 6개월 활동 수로 채워집니다. 목록에 활동이 없으면 6개월 이상일 수 있습니다. 이는 여전히 왼쪽 레일에서 추가할 수 있으며, 최대 18개월 동안의 전환 기간이 있습니다. |
| **[!UICONTROL 환경 제어]** | 제어 경험을 선택합니다. |
| **[!UICONTROL 지표 정규화]** | 방문자 수, 방문 횟수 또는 노출 횟수를 선택합니다. 대부분의 분석 사용 사례에는 [!UICONTROL 방문자]가 권장됩니다. 이 지표 (계산 방법이라고도 함)는 상승도 계산의 분모가 됩니다. 이는 신뢰도 계산이 적용되기 전에 데이터가 종합되는 방식에도 영향을 줍니다. |
| **[!UICONTROL 성공 지표]** | 드롭다운 메뉴에서 최대 3개의 표준(계산되지 않은) 성공 이벤트를 선택하거나 구성 요소 레일의 지표에서 지표를 드래그하여 놓습니다. 각 지표에는 렌더링된 패널에 전용 테이블과 시각화가 있습니다. |

패널을 빌드하려면 **[!UICONTROL 빌드]**&#x200B;를 선택하십시오.

### 패널 출력 {#panel-output}

Analytics for Target 패널은 Adobe Target 활동 및 경험의 성과를 더 잘 이해할 수 있도록 풍부한 데이터 및 시각화를 반환합니다. 패널 맨 위에는 선택한 패널 설정을 알려 주는 요약 줄이 제공됩니다. 선택한 각 성공 지표에 대해 전환율 트렌드를 보여 주는 하나의 [자유 형식 테이블](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table.md) 및 하나의 [선](/help/analyze/analysis-workspace/visualizations/line.md) 시각화가 표시됩니다.

![렌더링됨](assets/a4t-panel-output.png)

각 자유 형식 테이블에는 다음 지표 열이 표시됩니다.

| 지표 | 설명 |
|---|---|
| **[!UICONTROL 지표 정규화]** | 입력 패널에서 선택한 표준화 지표(고유 방문자 수, 방문 횟수 또는 활동 노출 횟수)입니다. |
| **[!UICONTROL 성공 지표]** | 입력 패널에서 선택한 성공 지표. |
| **[!UICONTROL 전환율]** | 성공 지표 / 표준화 지표입니다. |
| **[!UICONTROL 상승도]** | 통제 경험을 기준으로 각 경험의 전환율을 비교합니다. 참고: 상승도는 Target 경험에 대해 *잠긴 지표*&#x200B;입니다. 분류하거나 다른 차원과 함께 사용할 수 없습니다. |
| **[!UICONTROL 상승도(하한)]** | 이 값은 95% 신뢰 구간에서 변형 경험을 통해 제어할 수 있는 최악의 상승도를 나타냅니다.<br>자세한 내용은 [통계 계산](https://experienceleague.adobe.com/en/docs/target/using/reports/statistical-methodology/statistical-calculations) 및 [Complete Confidence Calculator](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx) Excel 파일을 참조하십시오. |
| **[!UICONTROL 상승도(중간)]** | 이 값은 95% 신뢰 구간에서 변형 경험을 통해 제어할 수 있는 중간 상승도를 나타냅니다. <br>자세한 내용은 [통계 계산](https://experienceleague.adobe.com/en/docs/target/using/reports/statistical-methodology/statistical-calculations) 및 [Complete Confidence Calculator](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx) Excel 파일을 참조하십시오. |
| **[!UICONTROL 상승도(상한)]** | 이 값은 95% 신뢰 구간에서 변형 경험을 통해 제어할 수 있는 최상의 상승도를 나타냅니다.<br>자세한 내용은 [통계 계산](https://experienceleague.adobe.com/en/docs/target/using/reports/statistical-methodology/statistical-calculations) 및 [Complete Confidence Calculator](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx) Excel 파일을 참조하십시오. |
| **[!UICONTROL 신뢰도]** | 학생 T-테스트에서는 다시 테스트를 실행하면 결과가 복제될 가능성을 나타내는 신뢰 수준을 계산합니다. 고정 조건부 서식 범위 (75%/85%/95%)가 지표에 적용되었습니다. 열 설정에서 필요한 경우 이 형식을 사용자 지정할 수 있습니다. 참고: 신뢰도는 Target 경험에 대해 &quot;잠긴 지표&quot;입니다. 분류하거나 다른 차원과 함께 사용할 수 없습니다.<br>자세한 내용은 [통계 계산](https://experienceleague.adobe.com/en/docs/target/using/reports/statistical-methodology/statistical-calculations) 및 [Complete Confidence Calculator](https://experienceleague.adobe.com/docs/target/assets/complete_confidence_calculator.xlsx) Excel 파일을 참조하십시오. |

Analysis Workspace의 모든 패널과 마찬가지로 Adobe Target 활동을 분석하는 데 도움이 되는 추가 테이블 및 [시각화](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations)를 추가하여 분석을 계속할 수 있습니다. 패널 수준 또는 자유형 테이블 내에서 세그먼트를 적용할 수도 있습니다. 자유형 테이블 내에 추가하는 경우 상승도 및 신뢰도 계산을 유지하기 위해 전체 테이블에 오버레이해야 합니다. 현재 열 수준 세그먼트는 지원되지 않습니다.

![편집](/help/assets/icons/Edit.svg)을 사용하여 패널을 다시 구성하고 다시 빌드합니다.

## FAQ {#FAQ}

| 질문 | 답변 |
|---|---|
| Analytics for Target에서 지원되는 활동 유형은 무엇입니까? | 지원되는 활동 유형에 대해 [자세히](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-activity-setup) 알아보십시오. |
| 상승도 및 신뢰도 계산에서 계산된 지표가 지원됩니까? | 아니요. 상승도 및 신뢰도에서 계산된 지표가 지원되지 않는 이유에 대해 [자세히](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-lift-and-confidence) 알아보십시오. 그러나 계산된 지표는 이러한 지표 외부의 Analytics for Target 보고에서 사용할 수 있습니다. |
| Target과 Analytics 간에 고유 방문자가 다른 이유는 무엇입니까? | 제품 간 고유 방문자 차이에 대해 [자세히 알아보기](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports). |
| 내 분석에서 특정 Target 활동에 대해 히트 세그먼트를 적용하면 반환된 관련 없는 경험이 표시되는 이유가 무엇입니까? | 타겟 분석 차원은 목록 변수입니다. 이는 한 번에 많은 활동(및 경험)을 포함할 수 있음을 의미합니다. [자세히 알아보기](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports) |
| 신뢰도 지표는 예외적인 주문을 고려합니까? 또는 여러 오퍼에 대해 Bonferroni 수정을 적용합니까? | 아니요. Analytics이 신뢰도를 계산하는 방법에 대해 [자세히](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/a4t-faq/a4t-faq-lift-and-confidence) 알아보십시오. |
| 상승도와 신뢰도 지표를 다른 차원이나 분류와 함께 사용할 수 있습니까? | 상승도와 신뢰도는 계산할 제어 및 변형을 필요로 하므로 타겟 경험 차원에 대해 &quot;잠긴 지표&quot;입니다. 따라서 분류하거나 다른 차원과 사용할 수 없습니다. |
| 상승도와 신뢰도는 언제 다시 계산됩니까? | 패널을 빌드하거나, 패널 날짜 범위가 변경되거나, 세그먼트가 패널이나 테이블에 적용될 때마다 상승도와 신뢰도가 다시 계산됩니다. 자유 형식 테이블에 세그먼트 필터를 적용할 때 모든 열에 세그먼트를 적용해야 합니다. 그렇지 않으면 상승도 및 신뢰도가 올바르게 업데이트되지 않습니다. 열 수준 세그먼트는 지원되지 않습니다. |

Analytics for Target 보고에 대한 자세한 내용은 [Analytics for Target 보고](https://experienceleague.adobe.com/en/docs/target/using/integrate/a4t/reporting)를 참조하세요.
