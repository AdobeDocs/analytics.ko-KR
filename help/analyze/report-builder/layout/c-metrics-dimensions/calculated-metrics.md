---
description: Report Builder 5.2는 Adobe Analytics Unified Calculated Metrics를 지원합니다. 가장 주목할 만한 혁신 사항은 모든 계산된 지표에는 전역 ID가 있으며 이것이 계산된 지표가 더 이상 하나의 보고서 세트로 제한되지 않음을 의미한다는 것입니다.
seo-description: Report Builder 5.2는 Adobe Analytics Unified Calculated Metrics를 지원합니다. 가장 주목할 만한 혁신 사항은 모든 계산된 지표에는 전역 ID가 있으며 이것이 계산된 지표가 더 이상 하나의 보고서 세트로 제한되지 않음을 의미한다는 것입니다.
seo-title: 계산된 지표
title: 계산된 지표
uuid: C 9814894-CDA 6-40 FF -8 EC 4-3 AB 2 C 1908 EBC
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 계산된 지표

Report Builder 5.2는 Adobe Analytics Unified Calculated Metrics를 지원합니다. 가장 주목할 만한 혁신 사항은 모든 계산된 지표에는 전역 ID가 있으며 이것이 계산된 지표가 더 이상 하나의 보고서 세트로 제한되지 않음을 의미한다는 것입니다.

>[!NOTE]
>
>기존 통합 문서는 기존 지표 ID가 있는 요청을 가리킬 수 있습니다. Report Builder 5.2 사용 시 이 기존 지표 ID들은 새로운 전역 ID로 변환됩니다. 이 통합 문서를 Report Builder v5.1 또는 그 이전 버전의 사용자와 공유하는 경우 해당 사용자는 계산된 지표를 볼 수 없게 됩니다.

새 Calculated Metric Builder 및 Manager로 계산된 지표를 생성 및 관리하는 방법에 대한 자세한 내용은 [계산된 지표](https://marketing.adobe.com/resources/help/en_US/analytics/calcmetrics) 안내서를 참조하십시오.

요청 마법사의 2단계에서는 계산된 지표를 필터링하고 적용할 수 있습니다.

## 계산된 지표 필터링 {#section_376E986D3E684999A7CDB08E53854159}

**필터 아이콘을 클릭하여** 계산된 지표를 필터링합니다. ![](assets/segment_filter.png)

라는 사용자 지정 코드에서 변수를 찾습니다. [고급 필터] 대화 상자는 표준 지표와 계산된 지표로 채워집니다.

사용 가능한 필터:

![](assets/advanced_filters_(2).png)

| 필터 이름 | 설명 |
|---|---|
| 태그 | 특정 태그가 있는 계산된 지표만 필터링할 수 있습니다. 태그 필터는 AND 연산자를 사용합니다. 두 태그를 선택하면 오른쪽 창에 **두** 태그가 모두 지정된 지표가 표시됩니다. |
| 보고서 세트 | *의 Calculated Metric Builder에서 "*&#x200B;보고서 세트 이름[!DNL Reports & Analytics]만" 필터를 적용한 다음 [!DNL Report Builder]에 고급 필터를 표시하면 고급 필터에 선택한 보고서 세트에 대한 계산된 지표만 표시됩니다. |
| 소유자 | 소유자별로 지표를 필터링할 수 있습니다. 소유자 필터는 OR 연산자를 사용합니다. 두 명의 소유자를 선택하면 오른쪽 창에 **둘 중 하나의** 소유자가 소유한 지표가 표시됩니다. |
| 기타 필터 &gt; 승인됨 | 공식적으로 승인된 모든 지표를 표시합니다. |
| 기타 필터 &gt; 즐겨찾기 | 즐겨찾기로 표시한 모든 지표를 표시합니다. |
| 기타 필터 &gt; 내 세그먼트 | 소유한 모든 지표를 표시합니다. |
| 기타 필터 &gt; 나와 공유 | 다른 사람이 사용자와 공유한 모든 지표를 표시합니다. |

## 계산된 지표 적용 {#section_DF5CF349460A45FDA4B6E6BB8B52F18E}

필터를 선택한 다음 **[!UICONTROL 적용]을 클릭하여 필터를 요청에 적용합니다.** 이제 선택된 필터가 보고서 레이아웃에 추가됩니다.

![](assets/filtering_for_metric.png)

