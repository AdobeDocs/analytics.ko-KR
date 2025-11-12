---
description: Analysis Workspace에서 경고를 만드는 방법을 알아봅니다.
title: 경고 만들기
feature: Alerts
exl-id: 82e51357-4a32-4db1-bc56-95a72dbaa1be
source-git-commit: ca84a5f807545d7196e2e0e90d3209c32d3fd789
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 94%

---

# 경고 만들기 {#create-alerts}

<!-- markdownlint-disable MD034 -->

>[!CONTEXTUALHELP]
>id="components_alerts_timegranularity"
>title="시간 세부 기간"
>abstract="시간 세부 기간이란 경고를 확인하는 빈도를 의미합니다."

<!-- markdownlint-enable MD034 -->

>[!NOTE]
>
>예외 항목 탐지가 있는 경고 사용(_지능형 경고_)은 Adobe Analytics Prime 또는 Ultimate 패키지를 보유한 조직에서만 사용할 수 있습니다.

Adobe Analytics의 경고 기능을 사용하면 변경된 백분율이나 특정 데이터 포인트에 따라 알림을 받을 수 있습니다. Adobe Analytics 패키지를 기반으로 예외 항목 임계값에 따라 경고를 트리거하도록 설정할 수도 있습니다. 서버 호출 사용 경고는 Analytics 관리자에게만 제공되는 다른 종류의 경고입니다. 이러한 경고는 서버 호출 소비 및 약정 데이터의 초과 위험 또는 발생을 알려 줍니다. 자세한 내용은 [서버 호출 사용 경고](/help/admin/tools/server-call-usage/scu-alerts.md)를 참조하십시오.

경고에 대한 자세한 개요 정보는 [경고 개요](alerts-overview.md)를 참조하십시오.

경고 만드는 방법:

1. 다음 방법 중 하나를 사용하여 경고를 생성합니다.

   * Analysis Workspace에서 프로젝트를 연 다음 **[!UICONTROL 구성 요소]** > **[!UICONTROL 경고 만들기]**&#x200B;를 선택합니다.
   * Analysis Workspace에서 프로젝트를 열고 다음 단축키를 사용합니다. ***Cmd + Shift + A***(macOS) 또는 ***Ctrl + Shift + A***(Windows).
   * Analysis Workspace에서 프로젝트를 열고 자유 형식 테이블에서 하나 이상의 라인 항목을 선택한 다음 마우스 오른쪽 버튼을 클릭하고 **[!UICONTROL 선택 항목에서 경고 만들기]**&#x200B;를 선택합니다. 이 액션을 통해 즉시 [경고 빌더](alert-builder.md)가 사전에 채워져서 올바른 지표 및 필터를 사용한 경고가 만들어집니다.
   * [경고 관리자에서](/help/components/alerts/alert-manager.md#create-alerts) 경고를 만듭니다.

   경고 빌더를 표시합니다. 이 인터페이스는 Analytics에서 세그먼트 또는 계산된 지표를 빌드하는 인터페이스와 유사합니다.



## 경고 빌더

경고 빌더 인터페이스는 Customer Journey Analytics에 세그먼트 또는 계산된 지표를 만든 인터페이스와 유사합니다.

![경고 빌더 인터페이스](assets/alert-builder.png)

경고 빌더에서 경고에 대한 다음 세부 정보를 지정합니다.

| 요소 | 설명 |
|---------|----------|
| **[!UICONTROL 제목]** | 경고의 이름을 지정합니다. 경고 이름에는 보고서 이름 또는 지표 임계값이 포함될 수 있습니다. |
| **[!UICONTROL 설명 (선택 사항)]** | 경고의 설명을 작성합니다. |
| **[!UICONTROL 시간 세부 기간]** | 지표를 확인할 주기(일별, 주별 또는 월별)를 선택합니다.<p> |
| **[!UICONTROL 수신자]** | 경고를 전송할 대상을 지정합니다. 경고는 Analytics 사용자, Analytics 그룹, 원시 이메일 주소 또는 전화번호에 보낼 수 있습니다.<p><b>중요</b>: 전화번호 앞에는 `+`와 [국가 코드](https://countrycode.org/)가 있어야 합니다.</p><p>사용자가 받는 이메일의 예:</p><p>![경고 이메일](assets/alerts-email.PNG)</p> |
| **[!UICONTROL 만료 날짜]** | 경고가 만료되기 원하는 날짜와 시간을 설정합니다. |
| **[!UICONTROL 지연]** | 데이터가 완료되어 Customer Journey Analytics에 보고되는 데 필요한 시간은 조직마다 다르며, 일반적으로 데이터 이벤트 시간 이후 3~9시간 정도 소요됩니다. 경고가 정확하려면 지정된 이벤트 범위에 대한 이벤트 데이터가 완료되어야 하므로 Adobe는 더 이상 지정된 이벤트 범위에 대한 이벤트 데이터를 수신하지 않습니다.<p>이러한 수집 시간 지연을 고려하여 경고가 전송되기까지 기본적으로 9시간이 지연됩니다.</p><p>기본 지연 시간인 9시간을 0~24시간 사이의 값으로 조정할 수 있습니다. 그러나 지연 시간을 9시간 이하로 줄이면 불완전한 데이터를 보고하게 되어 부정확한 경고 정보가 제공될 수 있습니다.</p><p>지연 시간을 줄일 때 다음 사항을 고려해야 합니다.</p><ul><li>**데이터 가용성 및 데이터 완전성 이해**: 모든 배치 데이터는 3~9시간 후에만 Experience Platform 데이터 세트에 수집됩니다. 경고가 정확하려면 데이터 수집이 완료되어야 하며, 모든 배치 데이터가 데이터 세트에 포함되어 있어야 합니다.</li><li>**데이터 세트에서 데이터가 완료되고 사용 가능해지는 데 걸리는 시간 결정**: 데이터 수집 시간은 조직에 따라 다릅니다. 경고 게재를 위해 선택한 지연 시간이 Platform 데이터 세트에서 배치 데이터를 사용하는 데 걸리는 시간과 같거나 덜 빈번한지 확인합니다<!--add link? -->.</li><p>**팁:** 모든 배치 데이터가 완료되어 Platform 데이터 세트에 수집되는 데 필요한 시간은 조직 내 데이터 엔지니어에게 문의하는 것이 가장 정확한 방법입니다.</p><p>또는 조직 내 배치 게재가 Experience Platform 데이터 세트에서 제공되는 데 걸리는 시간을 대략적으로 파악할 수 있습니다. Analysis Workspace의 자유 형식 테이블에서 만듭니다.</p><ol><li>Analysis Workspace의 자유 형식 테이블에 [!UICONTROL **이벤트**] 지표와 [!UICONTROL **일**] 차원을 추가합니다.</li><li>[!UICONTROL **시간**] 차원을 사용하여 [!UICONTROL **일**] 차원을 분류합니다.<p>데이터가 없는 시간은 0으로 표시됩니다.</p></li></ol><li>**계산 오류 고려**: 기본 지연 시간을 줄이려면 데이터 수집 완료에 걸리는 시간보다 최소 한 시간 길게 지연을 설정해야 합니다. 예를 들어 데이터 수집이 완료되기까지 3시간 지연이 발생하면 지연 시간을 4시간으로 설정해야 합니다.</li> |
| **[!UICONTROL 다음의 경우에 경고 보내기]** | [!UICONTROL **지표 중 하나 이상의 트리거**]: 여기에 지표(계산된 지표 포함)를 끌어다 놓아 경고 트리거를 생성합니다.<p>경고에 뜬 모든 지표, 차원 또는 세그먼트 중 일부가 현재 선택된 데이터 보기와 호환하지 않을 경우 **“호환하지 않는 구성 요소”** 메시지가 표시됩니다.</p><p>경고가 설정되기 전에 지표가 초과해야 하는 임계값을 결정합니다. 이 값을 임계값으로 설정한 후 다음 조건 중 하나로 설정할 수 있습니다.</p><ul><li>예외 항목이 있음</li><li>예외 항목이 예상치를 초과합니다.</li><li>예외 항목이 예상한 것보다 적습니다.</li><li>다음보다 크거나 같음</li><li>다음보다 작거나 같음</li><li>변경 기준</li><li>90%, 95%, 99%, 99.75% 및 99.9%의 임계값을 설정할 수 있습니다.</li></ul><p>[!UICONTROL **이들 필터 모두 사용**]: 세그먼트나 차원을 끌어다 놓아 경고에 필터를 추가할 수 있습니다. 예를 들어 *모바일 디바이스만* 세그먼트를 추가한다는 것은 모바일 디바이스에 대해서만 규칙이 트리거됨을 의미합니다. AND 구문을 사용하여 추가 필터를 적용할 수 있습니다. 톱니바퀴 아이콘을 클릭하여 AND 또는 OR 규칙을 추가할 수 있습니다.</p><p>사용 사례 예제는 [경고 - 사용 사례](alerts-use-cases.md)를 참조하십시오.</p> |
| **[!UICONTROL 미리보기]** | 대화형 경고 미리보기에서는 경고가 과거의 경험을 기반으로 얼마나 자주 표시되는지를 근사적으로 보여 줍니다.<p>예를 들어 시간 세부 기간을 매일로 설정하는 경우, 미리보기에서는 경고가 지난 30 또는 31일 동안 특정 지표 x 배수에 대해 트리거됨을 알 수 있습니다.</p><p>너무 많은 경고가 트리거되면 [경고 관리](alert-manager.md)에서 임계값을 조정할 수 있습니다.</p><p>![](assets/alert-preview.png){width="50%"}</p> |

<!--

   ![](assets/alert-builder.png)

1. Specify the following options to configure the alert:

   | Option | Description |
   |---------|----------|
   | [!UICONTROL **Title**]  | Specify a name for the alert. The alert name might contain the name of the report or the metrics threshold. |
   | [!UICONTROL **Description (optional)**] | Specify a description for the alert. |
   | [!UICONTROL **Time granularity**] | Select how often you want the metric to be checked: Hourly, Daily, Weekly, or Monthly.<p><b>Note:</b> For report suites with a custom calendar, monthly granularity in the Alert Builder is not supported.<!--true?--</p |
   | [!UICONTROL **Recipients**] | Specify where the alert can be sent. An alert can be sent to an Analytics user, an Analytics group, a raw email address, or to a phone number.<p><b>Important:</b> The phone number must be preceded by `+` and a [country code](https://countrycode.org/).</p><p>The e-mail that a user would receive once an alert has been triggered looks similar to:</p><p>![](assets/alerts-email.PNG)</p> |
   | [!UICONTROL **Expiration date**] | Set the date and time when you want the alert to expire. |
   | [!UICONTROL **Send an alert when**] | [!UICONTROL **Any of these metrics trigger**]: Drag and drop metrics (including calculated metrics) here to create triggers for the alert.<p>An **"incompatible components"** message appears if not all the metrics, dimensions, or segments in the alert are compatible with the currently selected data view.</p><p>Determine the threshold that the metric must exceed before an alert is set. You can set this value to a threshold and then to one of the following conditions:</p><ul><li>anomaly exists</li><li>anomaly is above expected</li><li>anomaly is below expected</li><li>is above or equals</li><li>is below or equals</li><li>changes by</li><li>You can set a threshold of 90%, 95%, 99%, 99.75%, and 99.9%.</li></ul><p>[!UICONTROL **With all of these filters**]: Drag and drop segments or dimensions to add filters. For example, adding a *Mobile Devices Only* segment would mean that the rule triggers only for mobile devices. You can add additional filters by using an AND statement. You can add AND or OR rules by clicking the gear icon.</p><p>See [Alerts - use cases](/help/components/alerts/alerts-use-cases.md) for example.</p> |
   | [!UICONTROL **Preview**] | The interactive alert preview shows you how often, approximately, an alert will fire based on past experience.<p>For example, if you set the time granularity to daily, the preview can tell you that the alert would have been triggered for a certain metric x times during the last 30 or 31 days. The preview approximation window is established by the alert frequency setting. For daily alert frequencies, the preview window approximates the previous 30 days. For weekly alert frequencies, the preview window approximates the last 12 weeks. For monthly alert frequencies, the preview window approximates the previous 12 months.</p><p>If you find that too many alerts will be triggered, you can adjust the threshold in the [Alert Manager](/help/components/alerts/alert-manager.md).</p><p>![](assets/alert_preview.png)</p> |

1. Select [!UICONTROL **Save**].

-->