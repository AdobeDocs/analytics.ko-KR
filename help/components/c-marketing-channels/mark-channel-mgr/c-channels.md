---
description: 마케팅 채널 관리자에서 마케팅 채널을 추가하거나 활성화합니다. 마케팅 채널이 없는 보고서 세트의 경우, 자동 설정을 사용하여 해당 규칙과 함께 여러 채널을 만들 수 있습니다. 사전 정의된 채널을 사용자 요구에 맞게 편집하거나 자체 채널을 만들 수 있습니다(최대 25개).
subtopic: Marketing channels
title: 마케팅 채널 관리
topic: Reports and analytics
uuid: 9d367bb6-a17b-49b8-9cd5-24fac35ae982
translation-type: tm+mt
source-git-commit: dd58453a0459bc200a00badf34d06c259ce9fb59

---


# 마케팅 채널 관리

마케팅 채널 관리자에서 마케팅 채널을 추가하거나 활성화합니다. 마케팅 채널이 없는 보고서 세트의 경우, 자동 설정을 사용하여 해당 규칙과 함께 여러 채널을 만들 수 있습니다. 사전 정의된 채널을 사용자 요구에 맞게 편집하거나 자체 채널을 만들 수 있습니다(최대 25개).

다음은 채널을 만드는 방법에 대한 지침입니다.

* 모든 채널 목록을 만드는 식으로 미리 계획을 해서 모든 방문자 히트가 정확한 채널로 분류되도록 하십시오.
* 항상 [내부](/help/components/c-marketing-channels/mc-faq/c-faq.md) 히트 및 [직접](/help/components/c-marketing-channels/mc-faq/c-faq.md) 히트 카테고리에 대한 채널을 포함시키십시오.

Adding channels to the [!UICONTROL Marketing Channels] page is done independently of creating rules on the [Marketing Channel Processing Rules](/help/components/c-marketing-channels/mc-proc-rules/t-rules.md) page. 규칙을 만들 때 채널과 규칙을 연관시킵니다.

## 마케팅 채널 추가{#add-mktg-channels}를 참조하십시오 

마케팅 채널 관리자에서 마케팅 채널을 추가합니다.

> [!NOTE] 채널은 삭제할 수 없습니다. 채널을 사용하지 않으려면 비활성화하거나 이름을 바꾼 후 나중에 사용하도록 예약해 두십시오.

1. 클릭 **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. 페이지에서 보고서 세트를 [!UICONTROL Report Suite Manager] 선택합니다.

   여러 개의 보고서 세트를 선택할 경우, 템플릿에서 선택한 보고서 세트로 설정을 복사하는 템플릿을 선택합니다.

   자세한 내용은 [여러 보고서 세트에 템플릿 보고서 세트 설정 적용](/help/components/c-marketing-channels/getting-started/t-template.md).

1. 클릭 **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]**.

   보고서 세트에 정의된 채널이 없으면 [자동 설정](/help/components/c-marketing-channels/getting-started/c-channel-autosetup.md) 페이지가 표시됩니다.

1. 페이지에서 [!UICONTROL Marketing Channel Manager] 을 클릭합니다 **[!UICONTROL Add Channel]**.

   25개의 채널이 정의된 경우에는 이 옵션을 사용할 수 없습니다.

1. 확대/축소한 후에 **[!UICONTROL Save.]**
1. 채널에 대한 규칙을 구성하려면 을 클릭합니다 **[!UICONTROL Marketing Channel Processing Rules]**.

   [마케팅 채널 처리 규칙 만들기](/help/components/c-marketing-channels/mc-proc-rules/t-rules.md)를 참조하십시오.

## 마케팅 채널 관리자 - 인터페이스 정의 {#mktg-channel-mgr}

페이지의 필드 정의. [!UICONTROL Marketing Channel Manager]

| 필드 | 정의 |
|--- |--- |
| 활성화됨 | 이 마케팅 채널을 활성 또는 비활성화합니다. |
| 채널 이름 | 마케팅 채널에 대한 알기 쉬운 이름입니다. |
| 마지막 접촉 채널 무시 | 영구적인 기존의 마지막 접촉 채널을 선택한 채널로 대체할지 여부를 선택할 수 있습니다. 이 확인란을 선택하면 모든 채널(직접 및 내부 포함)이 기존 마지막 접촉 채널을 덮어씁니다. 크레딧을 받은 자격이 없는 채널이 전환되는 문제가 발생할 수 있습니다. 예를 들어 이 옵션은 자연어 검색 채널을 통해 사용자를 이미 획득한 경우, 직접 채널이 전환 크레딧을 받지 못하도록 할 수 있습니다. |
| 채널 분류 | 이 값을 기준으로 채널을 분류할 수 있습니다. You can add possible channel breakdowns (subchannels) when creating [marketing channel classifications](/help/components/c-marketing-channels/mc-classifications/classifictions-mchannel.md). |
| 유형 | 사용자를 사이트로 인도한 방식을 지정합니다. 온라인 또는 오프라인을 선택할 수 있습니다. 검색 엔진 또는 이메일 캠페인을 통해 방문한 방문자에 대해 온라인 채널을 사용합니다. 오프라인 채널은 신문 쿠폰이나 잡지 광고를 보고 사이트를 방문한 방문자에게 적용됩니다. 오프라인 채널에는 일반적으로 보고 데이터 소스를 통해 가져온 데이터가 포함됩니다. [ 데이터 소스](https://docs.adobe.com/content/help/en/analytics/import/data-sources/datasrc-home.html)를 참조하십시오. [오프라인 데이터 추가](/help/components/c-marketing-channels/getting-started/c-channel-autosetup.md)를 참조하십시오. |
| 색상 | 이 마케팅 채널과 연관된 색상입니다. 이 색상은 마케팅 채널 보고서의 채널을 나타냅니다. |