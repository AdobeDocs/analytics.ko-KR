---
description: 보트 규칙을 사용하여 알려진 스파이더 및 보트가 생성하는 트래픽을 보고서 세트에서 제거할 수 있습니다. 보트 트래픽을 제거하면 웹 사이트에서 사용자 활동을 더 정확하게 측정할 수 있습니다.
seo-description: 보트 규칙을 사용하여 알려진 스파이더 및 보트가 생성하는 트래픽을 보고서 세트에서 제거할 수 있습니다. 보트 트래픽을 제거하면 웹 사이트에서 사용자 활동을 더 정확하게 측정할 수 있습니다.
seo-title: 보트 규칙
solution: Analytics
subtopic: 보트 규칙
title: 보트 규칙
topic: 관리 도구
uuid: 3 CB 9 E 29 D -1 C 37-43 DE-B 7 AC -34441093 A 60 E
translation-type: tm+mt
source-git-commit: 92ac6c03013bd68326e4136a5d512171fc831689

---


# 보트 규칙

보트 규칙을 사용하면 알려진 스파이더 및 보트가 생성하는 보고서 세트에서 트래픽을 제거할 수 있습니다. 보트 트래픽을 제거하면 웹 사이트에서 사용자 활동을 더 정확하게 측정할 수 있습니다.

보트 규칙이 정의된 후, 모든 들어오는 트래픽이 정의된 규칙과 비교됩니다. 이러한 규칙과 일치하는 트래픽은 보고서 세트에서 수집되지 않고 트래픽 지표에 포함되지 않습니다.

To update or upload bot rules, navigate to **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]**. Select the correct Report Suite, and then go to **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL General]** &gt; **[!UICONTROL Bot Rules]**.

일반적으로 보트 트래픽을 제거하면 트래픽 양과 전환 지표가 줄어듭니다. 대부분의 고객이 보트 트래픽을 제거하면 전환율이 증가하고 기타 유용성 지표도 증가함을 확인할 수 있습니다. 보트 트래픽을 제거하기 전에 이해 당사자들과 소통하여 이러한 변경의 결과로 핵심 성능 지표(KPI)에 필요한 조정을 할 수 있음을 확인하십시오. 가능하면 작은 보고서 세트에서 먼저 보트 트래픽을 제거하여 잠재적 영향을 추정하는 것이 좋습니다.

>[!NOTE] 보고서 세트당 500개 이하의 보트 규칙을 정의하는 것이 좋습니다. 사용자 인터페이스를 통해 500개의 규칙을 수동으로 정의할 수 있습니다. 이 한도에 도달하면 [파일 가져오기](../../../admin/admin/bot-rules/t-upload-bot-rules.md#task_95868D8564564E6A996163335C119806) 및 [보트 규칙 내보내기] 옵션을 통해 규칙을 일괄적으로 관리해야 합니다.

보트 트래픽 데이터는 개별 보관소에 저장되어 [!UICONTROL  보트] 및 [!UICONTROL 보트 페이지] 보고서에 표시됩니다.

| 규칙 유형 | 설명 |
|--- |--- |
| IAB | [!UICONTROL IAB 포함을 선택하면] IAB (International Advertising Bureau's International Advertising Bureau's International Spiders &amp; Bots List) 를 사용하여 보트 트래픽을 제거합니다. 이 목록은 IAB에서 매월 업데이트합니다. <br>보트를 IAB 목록에 제출하려면 [IAB](https://www.iab.net/sites/spiders/form.php)를 방문하십시오. <br>사용자가 보트 보고서를 사용하여 사용자의 사이트에 액세스한 보트 목록을 볼 수 있더라도, Adobe는 세부 IAB 보트 목록을 고객에게 제공할 수 없습니다. |
| 사용자 지정 보트 규칙 | 자세한 내용은  [사용자 지정 보트 규칙 만들기](../../../admin/admin/bot-rules/t-create-bot-rules.md). |

## 보트 규칙이 데이터 수집에 미치는 영향 {#section_F01A3130E7A04A9993371CF26F6586F2}

보트 규칙이 모든 분석 데이터에 적용됩니다. 보트 규칙으로 제거된 데이터는 보트 및 보트 페이지 보고서에서만 볼 수 있습니다.

VISTA rules are applied after Bot Rules (see [Processing Order](../../../admin/admin/c-processing-rules/c-processing-rules-configuration/processing-rule-order.md#concept_8A6BBEA7F50C40C8A8D8755D4F579B1E)).

**하이 히트 방문 처리:** 한 번의 방문에 100개 이상 히트가 발생하는 경우, 보고는 방문 시간(초)이 해당 방문의 히트 수와 같은지 또는 미만인지 파악합니다. 이런 상황에서 길고 집중적인 방문을 처리하는 비용 때문에, 보고는 새 방문으로 다시 시작합니다. 일반적으로 하이 히트 방문은 보트 공격으로 인해 발생하며 일반적인 방문 검색으로 간주되지 않습니다.

>[!NOTE]
>
>표시된 히트는 *`bots`* 서버 호출로 [청구됩니다](https://docs.adobe.com/content/help/en/analytics/admin/server-call-usage/overage-overview.html).

## 보트 필터링에 대한 IP 난독화의 영향 {#section_92E60B95BE8940D983F28C79E0CD6B12}

IAB 보트 목록은 오로지 사용자 에이전트를 기반으로 하므로, 해당 목록을 기반으로 한 필터링은 IP 난독화 설정의 영향을 받지 않습니다. 비-IAB 보트 필터링(사용자 지정 규칙)의 경우, IP는 필터링 기준의 일부일 수 있습니다. IP를 사용하여 보트를 필터링하는 경우, 해당 설정이 활성화되어 있으면 보트 필터링은 마지막 옥텟이 제거된 후, 하지만 전체 IP를 삭제하거나 일부 고유 ID로 대체하는 등의 다른 IP 난독화 옵션 전에 발생합니다.

IP 난독화가 활성화되어 있으면 IP 주소가 난독화되기 전에 IP 제외가 발생하므로 고객은 IP 난독화를 활성화할 때 아무것도 변경할 필요가 없습니다.

마지막 옥텟이 제거되면 IP 필터링 전에 변경이 수행됩니다. 따라서 마지막 옥텟은 0으로 대체되고, IP 제외 규칙은 끝에 0이 있는 IP 주소와 일치하도록 업데이트해야 합니다. 일치 *는 0과 일치해야 합니다.
