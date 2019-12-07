---
description: 방문자 히트가 채널에 지정된 기준을 충족하는지 여부를 결정하는 마케팅 채널 처리 규칙을 만듭니다.
subtopic: Marketing channels
title: 마케팅 채널 처리 규칙 만들기
topic: Reports and analytics
uuid: 0e47634f-3c69-46db-8af4-8d0b3d15f7a8
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 마케팅 채널 처리 규칙 만들기

방문자 히트가 채널에 지정된 기준을 충족하는지 여부를 결정하는 마케팅 채널 처리 규칙을 만듭니다.

이 절차에서는 이메일 규칙을 하나의 예로 사용합니다. 이 예에서는 마케팅 채널 관리자 페이지의 채널 목록에 이메일 채널을 추가했다고 가정합니다.

1. **[!UICONTROL Analytics]** &gt; **[!UICONTROL 관리자]** &gt; **[!UICONTROL 보고서 세트]**&#x200B;를 클릭합니다.
1. 보고서 세트 선택.

   보고서 세트에 정의된 채널이 없으면 [!UICONTROL 마케팅 채널: 자동 설정] 페이지가 표시됩니다.

   자세한 내용은 [자동 설정 실행](/help/components/c-marketing-channels/c-channel-autosetup.md).

1. **[!UICONTROL 편집 설정]** &gt; **[!UICONTROL 마케팅 채널]** &gt; **[!UICONTROL 마케팅 채널 처리 규칙]**&#x200B;을 클릭합니다.

   ![단계 결과](assets/marketing_channel_rules.png)

1. **새 규칙 세트 추가** 메뉴에서 **[!UICONTROL 이메일을 선택합니다]**.

   여기에서 채널을 선택하는 것이 아니라, 필요한 몇 가지 매개 변수로 규칙을 채우는 템플릿을 선택하는 것입니다.

   ![단계 결과](assets/example_email.png)

   부울 로직(if / then 문)을 사용하여 규칙을 구성합니다. 예를 들어 이메일 채널 규칙에서, 다음 문에서 강조된 설정 또는 정보를 제공합니다.

   `"If **[!UICONTROL All]** or **[!UICONTROL Any]** of the following are true:  **[!UICONTROL Query String Parameter]** *<value>* **[!UICONTROL exists]**...`

   `"Then identify the channel as **[!UICONTROL Email]**...`

   `"Then set the channel's value to **[!UICONTROL Query String Parameter]** *<value>*."`

   이 예에서 *`<value>`*&#x200B;는 이메일 캠페인에 사용하는 쿼리 문자열 매개 변수입니다(예:*`eml`*).
1. 규칙 만들기를 계속하려면 **[!UICONTROL 규칙 추가]**&#x200B;를 클릭합니다.
1. 규칙의 우선 순위를 정하려면 규칙을 드래그하여 원하는 위치에 놓습니다.
1. **[!UICONTROL 저장을 클릭합니다.]**

>[!MORELIKETHIS]
>
>* [FAQ 및 예제](/help/components/c-marketing-channels/c-faq.md)를 참조하십시오

