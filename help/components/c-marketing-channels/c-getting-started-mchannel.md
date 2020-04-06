---
title: 마케팅 채널 시작하기
description: 마케팅 채널 워크플로우, 자동 설정 및 템플릿 보고서 세트 설정을 여러 보고서 세트에 적용하는 방법에 대해 알아봅니다.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 마케팅 채널 시작하기

마케팅 채널은 일반적으로 방문자가 사이트에 도착하는 방법에 대한 통찰력을 제공하는 데 사용됩니다. 추적할 채널과 추적 방법에 따라 마케팅 채널 처리 규칙을 사용자 지정할 수 있습니다.

마케팅 채널은 표준 변환 지표의 구성 요소인 첫 번째 및 마지막 접촉 지표를 중심으로 진행됩니다.

## 마케팅 채널 워크플로우

![](assets/step1_icon.png) 비즈니스 요구 사항을 기반으로 각 채널 정의.

사용하는 채널을 정의하는 것은 마케팅 채널의 가장 중요한 구성 요소 중 하나입니다. 채널을 정의하려면 조직의 여러 개인 간에 협업이 필요할 수 있습니다. 고려해야 할 몇 가지 질문이 있습니다.

* 유료 검색을 사용하고 있습니까?
* 이메일 캠페인을 사용하고 있습니까? 개별적으로 추적하려는 여러 이메일 캠페인을 사용하고 있습니까?
* 사이트로 트래픽을 보내는 산하 조직이 있습니까? 개별적으로 추적하려는 산하 조직이 있습니까?
* 별도로 추적하는 데 유리한 외부 캠페인이 있습니까?
* 모든 소셜 네트워킹 사이트를 집계하시겠습니까? 아니면 개별적으로 추적하려는 사이트가 있습니까?
* 추적하려는 전환에 영향을 줄 수 있는 다른 채널이 있습니까?

권장 채널 목록은 FAQ 및 [예에서 확인할 수 있습니다](/help/components/c-marketing-channels/c-faq.md). 채널을 만들 때 더 쉽게 활성화 및 정의할 수 있도록 사용할 채널 목록을 만듭니다.

![](assets/step2_icon.png) 페이지에 마케팅 채널을 [!UICONTROL Marketing Channel Manager] 추가합니다.

After defining what channels to track, you enable them in **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.

중요한 전제 조건 및 개념 정보가 필요하면 [채널과 규칙](/help/components/c-marketing-channels/c-channels.md)을 참조하십시오.

절차에 대해서는 [마케팅 채널 추가](/help/components/c-marketing-channels/c-channels.md)를 참조하십시오.

>[!NOTE]
>
>마케팅 채널이 이전에 구성된 적이 없다면 [자동 설정](/help/components/c-marketing-channels/c-getting-started-mchannel.md)이 표시됩니다. 이 설정은 사용자 지정할 수 있는 미리 구성된 여러 채널을 제공합니다. 이러한 규칙을 템플릿으로 사용하는 것이 좋습니다. 하지만 이미 솔리드 채널 정의가 있는 경우 자동 설정을 건너뛸 수 있습니다.

![](assets/step3_icon.png) 페이지에서 각 채널의 규칙을 구성하거나 세분화할 수 [!UICONTROL Marketing Channel Processing Rules] 있습니다.

페이지에서 채널을 만든 후 채널이 데이터를 검색하고 보고할 수 있도록 규칙을 구성합니다. [!UICONTROL Marketing Channel Manager]

See [Marketing Channel Processing Rules](/help/components/c-marketing-channels/c-rules.md).

자동 설정에서 채널이 생성된 경우 해당 채널의 규칙이 정의됩니다. 필요에 맞게 수정할 수 있습니다.

## 마케팅 채널에 대한 자동 설정 {#run-auto-setup}

마케팅 채널 보고서에는 쉽게 시작할 수 있도록 1회 설정 페이지가 함께 제공됩니다. 추적에 사용할 수 있는 여러 마케팅 채널을 제공합니다. 채널과 규칙을 만드는 것이 편하다면 이 설정을 건너뛸 수 있습니다. 그러나 마법사가 자동으로 채널을 만들도록 허용하는 것이 좋습니다. 자동 설정을 사용하면 규칙이 구성되는 방식을 확인하거나 직접 편집할 수 있습니다. 언제든지 사전 정의된 채널을 비활성화하거나 삭제할 수 있습니다.

마케팅 채널을 자동 설정하는 방법

1. Click **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. 에서 [!UICONTROL Report Suite Manager]보고서 세트를 선택합니다.
1. Click **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]**.

   ![단계 결과](assets/wizard.png)

   >[!NOTE]
   >
   >The [!UICONTROL Marketing Channels: Auto Setup] page displays automatically when you access channel configuration applications in Admin Tools. [마케팅 채널 관리자](/help/components/c-marketing-channels/c-channels.md)를 참조하십시오. 보고서 세트에 하나 이상의 마케팅 채널이 포함된 경우 이 페이지는 표시되지 않습니다. 마케팅 채널을 포함하지 않는 다른 보고서 세트를 선택하지 않으면 이 페이지에 다시 액세스할 수 없습니다.

1. 만들려는 채널을 선택해야 합니다.

   이 옵션을 선택하면 **[!UICONTROL Email]**&#x200B;필수 **[!UICONTROL Display]**&#x200B;필드가 **[!UICONTROL Affiliate]** 되고

1. 클릭 **[!UICONTROL Save]**.

## 여러 보고서 세트에 템플릿 보고서 세트 설정 적용

마케팅 채널 구성을 테스트하는 템플릿으로 마스터 보고서 세트를 사용하는 방법. 시간을 절약하기 위해 이 템플릿을 대량 업데이트에서 하나 이상의 프로덕션 보고서 세트에 적용할 수 있습니다. 채널 및 규칙 세트에 대해 이 작업을 별도로 수행합니다.

>[!NOTE] 규칙 세트를 적용하려면 먼저 템플릿으로부터 채널을 적용하십시오. 이 절차를 수행할 때 채널은 모든 보고서 세트에 대해 동일해야 합니다.

1. 선택된 보고서 세트에 대해 마케팅 채널 보고서가 활성화되어 있어야 합니다. 계정 관리자가 이 단계를 수행합니다.
1. Click **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. On the **[!UICONTROL Report Suite Manager]** page, select the template report suite, as well as one or more target report suites.
1. Click **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]**.
1. 페이지에서 **[!UICONTROL Select Master Report Suites]** 템플릿 보고서 세트를 선택합니다.
1. 클릭 **[!UICONTROL Save All]**.
1. 템플릿으로부터 여러 보고서 세트에 규칙 적용:
   1. 페이지로 [!UICONTROL Report Suite Manager] 돌아갑니다.
   1. 템플릿 보고서 세트와 하나 이상의 대상 보고서 세트를 선택합니다.
   1. Click **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Processing Rules]**.
   1. 클릭 **[!UICONTROL Save]**. 이 단계에서 저장 단추가 비활성화되어 있으면 규칙 중 하나를 확장하여 활성화하십시오.

