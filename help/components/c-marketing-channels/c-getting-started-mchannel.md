---
title: 마케팅 채널 시작
description: 마케팅 채널 워크플로, 자동 설정 및 템플릿 보고서 세트 설정을 여러 보고서 세트에 적용하는 방법에 대해 알아봅니다.
feature: Marketing Channels
exl-id: 35938bf9-89ab-434f-9dc2-7a65251412ef
source-git-commit: 2eff7656741bdba3d5d7d1f33e9261b59f8e6083
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 100%

---

# 마케팅 채널 시작

>[!NOTE]
>
>Attribution 및 Customer Journey Analytics에 대한 마케팅 채널의 효과를 극대화하기 위해 [수정된 모범 사례](/help/components/c-marketing-channels/mchannel-best-practices.md)를 게시했습니다.
>
>Analytics 관리자는 [마케팅 채널 관리](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-channels.md)에 설명된 대로 조직의 마케팅 채널을 관리할 수 있습니다.

마케팅 채널은 일반적으로 사이트에 방문자가 도착하는 방식에 대한 통찰력을 제공하는 데 사용됩니다. 추적할 채널과 추적 방법에 따라 마케팅 채널 처리 규칙을 사용자 정의할 수 있습니다.

마케팅 채널은 표준 전환 지표의 구성 요소인 첫 번째 및 마지막 접촉 지표를 중심으로 진행됩니다.

## 마케팅 채널 워크플로

![](assets/step1_icon.png) 비즈니스 요구 사항을 기반으로 각 채널 정의.

사용하는 채널을 정의하는 것은 마케팅 채널에서 가장 중요한 구성 요소 중 하나입니다. 채널을 정의하려면 조직 내에 있는 여러 사람 간의 협업이 필요할 수 있습니다. 고려해야 할 몇 가지 질문은 다음과 같습니다.

* 유료 검색을 사용합니까?
* 이메일 캠페인을 사용합니까? 개별적으로 추적하고 싶은 여러 개의 이메일 캠페인을 사용하고 있습니까?
* 사이트로 트래픽을 보내는 제휴가 있습니까? 개별적으로 추적하고 싶은 제휴가 있습니까?
* 개별적으로 추적하면 좋은 외부 캠페인이 있습니까?
* 모든 소셜 네트워킹 사이트를 집계하시겠습니까? 아니면 개별적으로 추적하고 싶은 사이트가 있습니까?
* 추적할 변환에 영향을 주는 다른 채널이 있습니까?

권장 채널 목록은 [FAQ 및 예제](/help/components/c-marketing-channels/c-faq.md)에서 확인할 수 있습니다. 채널을 만들 때 더 쉽게 활성화 및 정의할 수 있도록 사용할 채널 목록을 만듭니다.

![](assets/step2_icon.png) [!UICONTROL  마케팅 채널 관리자] 페이지에서 마케팅 채널을 추가합니다.

추적할 채널을 정의하고 나면 **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]**&#x200B;에서 활성화합니다.

중요한 전제 조건 및 개념 정보가 필요하면 [채널과 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-channels.md)을 참조하십시오.

절차에 대해서는 [마케팅 채널 추가](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-channels.md)를 참조하십시오.

>[!NOTE]
>
>마케팅 채널이 이전에 구성된 적이 없다면 [자동 설정](/help/components/c-marketing-channels/c-getting-started-mchannel.md)이 표시됩니다. 이 설정에서는 사용자 정의가 가능한 사전 구성된 채널 몇 가지를 제공합니다. Adobe에서는 이러한 규칙을 템플릿으로 사용할 것을 권장합니다. 그러나 이미 확고한 채널 정의가 있는 경우에는 자동 설정을 건너뛸 수 있습니다.

![](assets/step3_icon.png)[!UICONTROL  마케팅 채널 처리 규칙] 페이지에서 각 채널의 규칙을 구성하거나 세분화합니다.

[!UICONTROL 마케팅 채널 관리자] 페이지에서 채널을 만들고 나면 채널에서 데이터를 검색하고 보고할 수 있도록 규칙을 구성합니다.

[마케팅 채널 처리 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md)를 참조하십시오.

채널을 자동 설정에서 만드는 경우에는 채널의 규칙이 정의됩니다. 정의된 규칙을 필요에 맞게 수정할 수 있습니다.

## 마케팅 채널에 대한 자동 설정 {#run-auto-setup}

마케팅 채널 보고서에는 쉽게 시작할 수 있도록 1회 설정 페이지가 함께 제공됩니다. 이 보고서는 추적하는 데 사용할 수 있는 여러 가지 마케팅 채널을 제공합니다. 채널과 규칙을 만드는 데 익숙하다면 이 설정을 건너뛸 수 있습니다. 그러나 Adobe에서는 마법사가 사용자 대신 채널을 만들도록 허용할 것을 권장합니다. 자동 설정을 통해 규칙이 구성되는 방식을 보고 원하는 대로 편집할 수 있습니다. 사전 정의된 채널은 언제든지 비활성화하거나 삭제할 수 있습니다.

마케팅 채널을 자동 설정하는 방법

1. **[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]**&#x200B;를 클릭합니다.
1. [!UICONTROL 보고서 세트 관리자]에서 보고서 세트를 선택합니다.
1. **[!UICONTROL 편집 설정]** > **[!UICONTROL 마케팅 채널]** > **[!UICONTROL 마케팅 채널 관리자]**&#x200B;를 클릭합니다.

   ![단계 결과](assets/wizard.png)

   >[!NOTE]
   >
   >관리자 도구에서 채널 구성 애플리케이션에 액세스하면 자동으로 [!UICONTROL 마케팅 채널: 자동 설정] 페이지가 표시됩니다. [마케팅 채널 관리자](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-channels.md)를 참조하십시오. 보고서 세트에 하나 이상의 마케팅 채널이 포함된 경우에는 이 페이지가 표시되지 않습니다. 마케팅 채널을 포함하지 않는 다른 보고서 세트를 선택하지 않는 한 이 페이지에 다시 액세스할 수 없습니다.

1. 만들려는 채널을 선택해야 합니다.

   선택한 경우, **[!UICONTROL 이메일]**, **[!UICONTROL 표시]** 및 **[!UICONTROL 제휴]**&#x200B;는 필수 필드입니다.

1. **[!UICONTROL 저장을]** 클릭합니다.

## 여러 보고서 세트에 템플릿 보고서 세트 설정 적용

마케팅 채널 구성을 테스트하는 템플릿으로 마스터 보고서 세트를 사용하는 방법입니다 시간을 절약하기 위해, 이 템플릿을 대량 업데이트 시 하나 이상의 프로덕션 보고서 세트에 적용할 수 있습니다. 이 작업은 채널과 규칙 세트에 대해 별도로 수행합니다.

>[!NOTE]
>
>규칙 세트를 적용하려면 먼저 템플릿으로부터 채널을 적용하십시오. 이 절차를 수행할 때 채널은 모든 보고서 세트에 대해 동일해야 합니다.

1. **[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 보고서 세트 관리자]** 페이지에서 템플릿 보고서 세트와 하나 이상의 대상 보고서 세트를 선택합니다.
1. **[!UICONTROL 편집 설정]** > **[!UICONTROL 마케팅 채널]** > **[!UICONTROL 마케팅 채널 관리자]**&#x200B;를 클릭합니다.
1. **[!UICONTROL 마스터 보고서 세트 선택]** 페이지에서 템플릿 보고서 세트를 선택합니다.
1. **[!UICONTROL 모두 저장]**&#x200B;을 클릭합니다.
1. 템플릿으로부터 여러 보고서 세트에 규칙 적용:
   1. [!UICONTROL 보고서 세트 관리자] 페이지로 돌아갑니다.
   1. 템플릿 보고서 세트와 하나 이상의 대상 보고서 세트를 선택합니다.
   1. **[!UICONTROL 편집 설정]** > **[!UICONTROL 마케팅 채널]** > **[!UICONTROL 마케팅 채널 처리 규칙]**&#x200B;을 클릭합니다.
   1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다. 이 단계에서 저장 버튼이 비활성화되어 있으면 규칙 중 하나를 확장하여 활성화하십시오.
