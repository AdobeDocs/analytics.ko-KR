---
description: 'null'
seo-description: 'null'
seo-title: 경고 빌더
title: 경고 빌더
uuid: 86 d 00 a 33-dc 99-4 dc 3-a 732-0 b 895 ba 487 bc
translation-type: tm+mt
source-git-commit: 8b2feced9fd503395d06dc12c8e5d7985ca89161

---


# 경고 빌더

>[!IMPORTANT]
>
>Intelligent Alerts are available to Adobe [!DNL Analytics] Prime and Adobe [!DNL Analytics] Ultimate customers only.

다음 네 가지 방법 중 하나로 경고 빌더에 액세스합니다.

* Analysis Workspace에서 다음의 바로 가기 사용:

   `ctrl (or cmd) + shift + a`
* **[!UICONTROL 작업 영역]** &gt; **[!UICONTROL 구성 요소]** &gt; **[!UICONTROL 새 경고로 이동합니다]**.
* 하나 이상의 자유 형식 테이블 라인 항목을 선택하고, 마우스 오른쪽 단추로 클릭한 다음, **[!UICONTROL 선택 항목으로 경고 만들기 선택]**.
* From within a [!UICONTROL Reports &amp; Analytics] report, by going to **[!UICONTROL More]** &gt; **[!UICONTROL Add Alert]**.

The Alert Builder interface is familiar to those who have built segments or calculated metrics in [!DNL Analytics]:

![](assets/alert_builder.png)

**경고 이름**

경고 이름을 지정합니다. 경고 이름에는 보고서 또는 지표 임계값 이름이 포함될 수 있습니다.

**시간 세부기간**

지표를 확인할 시기(시간별, 일별, 주별 또는 월별)를 지정합니다.

>[!NOTE]
>
>사용자 지정 달력이 있는 보고서 세트의 경우, 경고 빌더에서 월별 세부기간을 지원하지 않습니다.

**수신자**

경고를 전송할 대상을 지정합니다. An alert can be sent to an [!DNL Analytics] user, an [!DNL Analytics] group, a raw email address, or to a phone number.

>[!IMPORTANT]
>
>The phone number must be preceded by a "+" and a [country code](https://countrycode.org/).

**만료 날짜**

경고의 만료 날짜를 설정합니다. 

**다음의 경우에 경고 보내기...**

*... 다음 지표 중 하나 이상의 트리거*

* 트리거를 추가하는 지표를 캔버스에 드래그하여 놓습니다. 

   Note that an **"incompatible components”** message will appear if not all the components (metrics/dimensions/segments) in the alert are compatible with the currently selected report suite.

* 경고를 설정하기 전에 지표가 초과되는 임계값을 결정합니다. 이 값을 임계값으로 설정한 후 다음 조건 중 하나로 설정할 수 있습니다. 

   * 예외 항목이 있음
   * 예외 항목이 예상 이상임
   * 예외 항목이 예상 미만임
   * 예외 항목 초과
   * 위 또는 같음
   * 아래 또는 같음
   * 변경

* "예외 항목 초과"는 기존(정적) 임계값을 초과하는 새로운 조건입니다. 트리거를 동적으로 정의하는 예외 항목 탐지 알고리즘을 가져옵니다. 90%, 95%, 99%, 99.75% 및 99.9%의 임계값을 설정할 수 있습니다.
* 시간 세분기간은 99.75% 임계값으로 설정되고 일별 세분기간은 99%로 설정됩니다.
* 계산된 지표를 사용할 수도 있습니다.

*... 다음 필터 사용*

세그먼트 또는 차원을 드래그하여 놓아 필터를 추가합니다. 예를 들어, "모바일 장치만" 세그먼트를 추가한다는 것은 모바일 장치에 대해서만 규칙이 트리거됨을 의미합니다. 

추가 필터를 적용하려면 AND 구문을 사용합니다.

**규칙 추가**

톱니바퀴 아이콘을 클릭하여 AND 또는 OR 규칙을 추가할 수 있습니다.

## 경고 미리 보기 {#section_10D75BA7B77E4C5FAF58A719C082E070}

대화형 경고 미리 보기에서는 경고가 과거의 경험을 기반으로 얼마나 자주 표시되는지를 근사적으로 보여 줍니다.

예를 들어, 시간 세부기간을 매일로 설정하는 경우, 미리 보기에서는 경고가 지난 30 또는 31일 동안 특정 지표 x 배수에 대해 트리거됨을 알 수 있습니다.

너무 많은 경고가 트리거될 것 같으면 [경고 관리자](/help/components/c-alerts/alert-manager.md)에서 임계값을 조정할 수 있습니다.

![](assets/alert_preview.png)
