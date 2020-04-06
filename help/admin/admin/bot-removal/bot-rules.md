---
description: 보트 규칙을 사용하면 알려진 스파이더 및 보트가 생성하는 트래픽을 보고서 세트에서 제거할 수 있습니다. 보트 트래픽을 제거하면 웹 사이트의 사용자 활동을 보다 정확하게 측정할 수 있습니다.
subtopic: Bot rules
title: 보트 규칙 개요
topic: Admin tools
uuid: 3cb9e29d-1c37-43de-b7ac-34441093a60e
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 보트 규칙 개요

보트 규칙을 사용하면 알려진 스파이더 및 보트에서 생성한 트래픽을 보고서 세트에서 제거할 수 있습니다. 보트 트래픽을 제거하면 웹 사이트의 사용자 활동을 보다 정확하게 측정할 수 있습니다.

보트 규칙이 정의되면 들어오는 모든 트래픽이 정의된 규칙과 비교됩니다. 이러한 규칙과 일치하는 트래픽은 보고서 세트에서 수집되지 않으며 트래픽 지표에 포함되지 않습니다.

보트 규칙을 업데이트하거나 업로드하려면 **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**&#x200B;으로 이동합니다. 올바른 보고서 세트를 선택한 다음 **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Bot Rules]**&#x200B;로 이동합니다.

일반적으로 보트 트래픽을 제거하면 트래픽 양과 전환 지표가 줄어듭니다. 많은 고객이 보트 트래픽을 제거하면 전환율이 증가하고 기타 유용성 지표가 증가한다는 사실을 알고 있습니다. 보트 트래픽을 제거하기 전에 이해 관계자와 연락하여 이러한 변경의 결과로 주요 성능 지표에 필요한 조정을 할 수 있는지 확인합니다. 가능하면 작은 보고서 세트에서 먼저 보트 트래픽을 제거하여 잠재적 영향을 추정하는 것이 좋습니다.

보트 트래픽 데이터는 개별 보관소에 저장되어 보트 및 보트 페이지 보고서에 표시됩니다. 보트 필터링을 활성화하는 다음 두 가지 옵션이 있습니다.

| 규칙 유형 | 설명 |
|--- |--- |
| 표준 IAB 보트 규칙 | Selecting [!UICONTROL Enable IAB Bot Filtering Rules] uses the [IAB&#39;s](https://www.iab.com) (International Advertising Bureau&#39;s) International Spiders &amp; Bots List to remove bot traffic. 대부분의 고객은 최소한 이 옵션을 선택합니다. |
| 사용자 지정 보트 규칙 | 사용자 에이전트, IP 주소 또는 IP 범위를 기반으로 하여 사용자 지정 보트 규칙을 정의하고 추가할 수 있습니다. |

## 표준 IAB 보트 규칙

확인란을 선택하여 표준 IAB 보트 규칙을 설정할 수 [!UICONTROL Enable IAB Bot Filtering Rules] 있습니다. 이 옵션을 선택하면 IAB(International Advertising Bureau)의 International Spiders &amp; Bots List에 있는 보트를 제거하여 보트 트래픽을 제거합니다. IAB는 이 목록을 매달 업데이트합니다.

![](assets/bot-iab-checkbox.png)

사용자는 보트 보고서를 사용하여 사용자의 사이트에 액세스한 보트 목록을 볼 수 있어도 Adobe에서는 세부 IAB 보트 목록을 고객에게 제공할 수 없습니다. IAB 목록에 보트를 제출하려면 [IAB](https://www.iab.com)를 방문하십시오.

## 사용자 지정 보트 규칙

>[!N참고] 사용자 인터페이스를 통해 500개의 규칙을 수동으로 정의할 수 있습니다. 이 한도에 도달하면 파일 가져오기 및 보트 규칙 내보내기 옵션을 통해 규칙을 일괄적으로 관리해야 합니다.

사용자 지정 보트 규칙을 사용하여 정의한 조건을 기준으로 트래픽을 필터링할 수 있습니다.

사용자 지정 보트 규칙은 다음 조건 유형을 사용하여 정의됩니다.

* 사용자 에이전트
* IP 주소
* IP 범위

단일 규칙에 대해 여러 조건을 정의할 수 있습니다. &quot;or&quot;를 사용하여 여러 조건을 일치시킵니다. 예를 들어 사용자 에이전트 및 IP 주소에 대한 값을 제공하는 경우 두 조건 중 하나가 충족되면 트래픽이 보트 트래픽으로 간주됩니다.

### 사용자 에이전트

A User Agent condition checks the user agent value to see if it **[!UICONTROL starts with]** or **[!UICONTROL contains]** the specified string. If **[!UICONTROL contains]** is selected, the substring is matched if it occurs anywhere in the user agent.

Optional values can be included in the **[!UICONTROL does not contain]** list to define values that the user agent must not contain for a successful match. 라인당 하나의 값을 포함하여 여러 값을 지정할 수 있습니다. 사용자 에이전트가 일치 문자열에 지정된 기준을 충족하지만 포함하지 않음 목록에 문자열을 포함하는 경우 일치로 간주되지 않습니다.

The **[!UICONTROL contains]** field is limited to 100 characters. 포함하지 않음 목록은 255자에서 각 새 줄의 구분 문자를 뺀 값으로 제한됩니다. (문자열 수 - 1과 같습니다. 4에 문자열이 *없으면* 3개의 구분 문자가 필요합니다. 모든 문자열 일치는 대/소문자를 구분하지 않습니다.

### IP 주소(와일드카드 일치 포함)

와일드카드(*)를 사용하여 동일한 블록의 IP 주소 또는 여러 주소와 일치합니다. 일치시킬 IP 주소의 숫자 값을 제공합니다. 와일드카드를 사용하여 일치시킬 모든 값에 대해 *로 대체합니다. 다음 목록에는 IP 주소 일치 문자열의 예가 포함되어 있습니다.

```
10.10.10.1
10.10.10.*
```

### IP 주소 범위

일치시킬 IP 주소의 시작 및 끝 범위를 제공합니다. 와일드카드를 사용하여 일치시킬 모든 값에 대해 *로 대체합니다.

### 사용자 지정 보트 규칙 정의

1. > **[!UICONTROL Analytics]** 로 **[!UICONTROL Admin]**&#x200B;이동하고 하나 이상의 보고서 세트를 선택하고 **[!UICONTROL General]** > **[!UICONTROL Bot Rules]**&#x200B;을 클릭합니다.
1. Click **[!UICONTROL Add Rule]** and define one or more match conditions.
1. 클릭 **[!UICONTROL Save]**. 변경은 30분 이내에 적용됩니다.

## 보트 규칙 업로드

보트 규칙을 벌크 가져오기 위해 규칙을 정의하는 CSV 파일을 업로드할 수 있습니다.

다음 열을 표시된 순서대로 포함한 CSV 파일을 만듭니다.

| 열 1 | 열 2 | 열 3 | 열 4 | 열 5 |
|--- |--- |---|---|---|
| 보트 이름 | IP 시작 | IP 끝 | 에이전트 일치 규칙<br>(다음을 포함하거나 다음으로 시작)</br> | 에이전트 제외<br>(255자 제한)</br> |

다음 세 가지 유형의 보트 규칙을 정의할 수 있습니다.

* 사용자 에이전트 포함 또는 다음으로 시작
* 단일 IP 주소 또는 와일드카드 일치
* IP 범위 일치

가져오기 파일의 각 행은 다음 보트 정의 중 하나만 포함할 수 있습니다.

* **사용자 에이전트 포함 또는 다음으로**&#x200B;시작:[에이전트 포함] 열에 일치시킬 단일 사용자 에이전트 문자열을 제공합니다. [에이전트 일치 규칙] 필드에 *포함* 또는 *다음으로* 시작을 배치하여 수행할 일치 유형을 지정합니다. 에이전트 제외 열에 에이전트가 포함하지 않는 한 개 이상의 파이프 구분(`|`) 문자열을 정의하는 선택적 값을 포함할 수 있습니다. 문자열 일치는 대/소문자를 구분하지 않습니다. IP 시작 열과 IP 끝 열은 모두 비어 있어야 합니다.

* **단일 IP 주소 또는 와일드카드 일치**: 단일 IP 주소(`10.10.10.1`) 또는 와일드카드 IP 주소(`10.10.*.*`)를 일치시키려면 IP 시작 열과 IP 끝 열에 모두 동일한 값을 배치합니다. 일치 규칙, 에이전트 포함 및 에이전트 제외는 비어 있어야 합니다.

* **IP 범위 일치**:IP 시작 및 IP 끝 열을 사용하여 IP 주소 범위를 정의합니다. 와일드카드를 사용하여 IP 범위를 일치시킬 수 있습니다(예: `10.10.10.*` ~ `10.10.20.*`). 일치 규칙, 에이전트 포함 및 에이전트 제외는 비어 있어야 합니다.

### OR로 결합된 다중 규칙

OR로 결합된 규칙 조합을 사용하여 보트를 일치시키려면(예: 사용자 에이전트 또는 IP 주소) 보트 이름 필드에 결합할 모든 규칙에 대해 동일한 이름을 제공합니다. AND 일치는 지원되지 않습니다.

### 업로드 파일로 모든 규칙 덮어쓰기

Select the **[!UICONTROL Overwrite existing rules]** checkbox to delete all existing rules and replace them with the rules defined in the upload file.

### 규칙 내보내기

The **[!UICONTROL Export Uploaded Bot File]** button exports all rules defined in the UI in a CSV format.


## 보트 규칙이 데이터 수집에 미치는 영향 {#section_F01A3130E7A04A9993371CF26F6586F2}

보트 규칙은 모든 Analytics 데이터에 적용됩니다. 보트 규칙으로 제거된 데이터는 보트 및 보트 페이지 보고서에서만 볼 수 있습니다.

VISTA 규칙은 보트 규칙 다음에 적용됩니다([ 처리 순서](/help/admin/admin/c-processing-rules/c-processing-rules-configuration/processing-rule-order.md) 참조).

**히트 방문 처리:** 방문에서 100개 이상의 히트가 발생하는 경우, 보고 기능은 방문 시간이 방문의 히트 수보다 적은지 또는 같은지 결정합니다. 이러한 상황에서 길고 강도 높은 방문 처리 비용으로 인해 보고는 새 방문으로 다시 시작됩니다. 일반적으로 히트 방문은 보트 공격으로 인해 발생하며 일반적인 방문자 탐색으로 간주되지 않습니다.

>[!NOTE] *`bots`*&#x200B;로 표시된 히트는 [서버 호출](/help/admin/c-server-call-usage/overage-overview.md)로 청구됩니다.

## IP 난독화가 보트 필터링에 미치는 영향 {#section_92E60B95BE8940D983F28C79E0CD6B12}

IAB 보트 목록은 사용자 에이전트만 기반으로 하므로 해당 목록을 기반으로 한 필터링은 IP 난독화 설정의 영향을 받지 않습니다. IAB가 아닌 보트 필터링(사용자 지정 규칙)의 경우 IP가 필터링 기준의 일부일 수 있습니다. IP를 사용하여 보트를 필터링하는 경우, 보트 필터링은 해당 설정이 활성화된 경우 마지막 octet가 제거된 후 전체 IP를 삭제하거나 일부 고유 ID로 교체하는 등 다른 IP 난독화 옵션 전에 발생합니다.

IP 난독화가 활성화되면 IP 주소가 난독화되기 전에 IP 제외가 발생하므로 고객은 IP 난독화를 활성화할 때 아무 것도 변경할 필요가 없습니다.

마지막 8진수가 제거되면 IP 필터링 전에 수행됩니다. 따라서 마지막 8진수는 0으로 대체되며, IP 제외 규칙은 IP 주소가 끝에 0으로 일치되도록 업데이트해야 합니다. 일치 *는 0과 일치해야 합니다.
