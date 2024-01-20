---
description: 마케팅 채널 관리자에서 마케팅 채널을 추가하거나 활성화합니다. 마케팅 채널이 없는 보고서 세트의 경우, 자동 설정을 사용하여 해당 규칙과 함께 여러 채널을 만들 수 있습니다. 사전 정의된 채널을 사용자 요구에 맞게 편집하거나 자체 채널을 만들 수 있습니다(최대 25개).
subtopic: Marketing channels
title: 마케팅 채널 관리
feature: Marketing Channels
exl-id: a768a4c2-f922-4d96-a9fb-78a1dfac04d8
source-git-commit: d173a6c6c9751a86f4218ec842da17da14f8485b
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 94%

---

# 마케팅 채널 관리

>[!NOTE]
>
> 마케팅 채널에 대한 일반 정보는 [마케팅 채널 시작하기](/help/components/c-marketing-channels/c-getting-started-mchannel.md)를 참조하십시오.
>
> 기여도 분석 및 Customer Journey Analytics에 대한 마케팅 채널의 효과를 극대화하기 위해 다음을 게시했습니다 [수정된 모범 사례](/help/components/c-marketing-channels/mchannel-best-practices.md).

**[!UICONTROL 분석]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]** > **[!UICONTROL 편집 설정]** > **[!UICONTROL 마케팅 채널]** > **[!UICONTROL 마케팅 채널 관리자]**.

마케팅 채널 관리자에서 마케팅 채널을 추가하거나 활성화합니다. 마케팅 채널이 없는 보고서 세트의 경우, 자동 설정을 사용하여 해당 규칙과 함께 여러 채널을 만들 수 있습니다. 사전 정의된 채널을 사용자 요구에 맞게 편집하거나 자체 채널을 만들 수 있습니다(최대 25개).

[!UICONTROL 마케팅 채널] 페이지에 채널을 추가하는 작업은 [마케팅 채널 처리 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md) 페이지에서 규칙을 만드는 작업과는 별개로 수행됩니다. 규칙을 만들 때 채널과 규칙을 연관시킵니다.

다음은 채널을 만드는 방법에 대한 지침입니다.

* 모든 채널 목록을 만드는 식으로 미리 계획을 해서 모든 방문자 히트가 정확한 채널로 분류되도록 하십시오.
* [내부](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md) 히트에 대한 채널을 포함시키십시오.
* 유료 채널 후와 유기 채널 전에 배치되는 모든 “다른 캠페인” 채널을 포함하십시오.


## 사전 요구 사항 {#prereqs}

* 마케팅 채널 차원에 대한 액세스 권한을 설정합니다.

  [마케팅 채널 권한](/help/components/c-marketing-channels/c-channel-report-access.md)을 참조하십시오.

## 마케팅 채널 추가 {#add-mktg-channels}

마케팅 채널 관리자에서 마케팅 채널을 추가합니다.

>[!NOTE]
>
>채널은 삭제할 수 없습니다. 채널을 사용하지 않으려면 비활성화하거나 이름을 바꾼 후 나중에 사용하도록 예약해 두십시오.

1. **[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]**&#x200B;를 클릭합니다.
1. [!UICONTROL 보고서 세트 관리자 페이지에서 보고서 세트를 선택합니다.]

   여러 개의 보고서 세트를 선택할 경우, 템플릿에서 선택한 보고서 세트로 설정을 복사하는 템플릿을 선택합니다.

   다음을 참조하십시오 [여러 보고서 세트에 템플릿 보고서 세트 설정 적용](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

1. **[!UICONTROL 편집 설정]** > **[!UICONTROL 마케팅 채널]** > **[!UICONTROL 마케팅 채널 관리자]**&#x200B;를 클릭합니다.

   보고서 세트에 정의된 채널이 없으면 [자동 설정](/help/components/c-marketing-channels/c-getting-started-mchannel.md) 페이지가 표시됩니다.

1. [!UICONTROL 마케팅 채널 관리자] 페이지에서 **[!UICONTROL 채널 추가]**&#x200B;를 클릭합니다.

   25개의 채널이 정의된 경우에는 이 옵션을 사용할 수 없습니다.

1. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
1. 채널에 대한 규칙을 구성하려면 **[!UICONTROL 마케팅 채널 처리 규칙]**&#x200B;을 클릭합니다.

   [마케팅 채널 처리 규칙 만들기](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md)를 참조하십시오.

## 채널 설정 적용 {#mktg-channel-mgr}

[!UICONTROL 마케팅 채널 관리자] 페이지에는 각 채널에 적용할 수 있는 다양한 설정이 있습니다.

| 필드 | 정의 |
|--- |--- |
| 활성화됨 | 이 마케팅 채널을 활성 또는 비활성화합니다. |
| 채널 이름 | 마케팅 채널에 대한 알기 쉬운 이름입니다. |
| 마지막 접촉 채널 무시 | 영구적인 기존의 마지막 접촉 채널을 선택한 채널로 대체할지 여부를 선택할 수 있습니다. 이 확인란을 선택하면 모든 채널 (직접 및 내부 포함)이 기존 마지막 접촉 채널을 덮어씁니다. 크레딧을 받은 자격이 없는 채널이 전환되는 문제가 발생할 수 있습니다. 예를 들어 이 옵션은 자연어 검색 채널을 통해 사용자를 이미 획득한 경우, 직접 채널이 전환 크레딧을 받지 못하도록 할 수 있습니다. |
| 채널 분류 | 이 값을 기준으로 채널을 분류할 수 있습니다. [마케팅 채널 분류](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/classifications-mchannel.md)를 만들 때 가능한 채널 분류 (하위 채널)를 추가할 수 있습니다. |
| 유형 | 사용자를 사이트로 인도한 방식을 지정합니다. 온라인 또는 오프라인을 선택할 수 있습니다. 검색 엔진 또는 이메일 캠페인을 통해 방문한 방문자에 대해 온라인 채널을 사용합니다. 오프라인 채널은 신문 쿠폰이나 잡지 광고를 보고 사이트를 방문한 방문자에게 적용됩니다. 오프라인 채널에는 일반적으로 보고 데이터 소스를 통해 가져온 데이터가 포함됩니다. [데이터 소스](https://experienceleague.adobe.com/docs/analytics/import/data-sources/datasrc-home.html)를 참조하십시오. [오프라인 데이터 추가](/help/components/c-marketing-channels/c-getting-started-mchannel.md)를 참조하십시오. |

### 무시 권장 사항

직접 및 내부 채널이 다른 지속적인 마지막 터치 채널(또는 서로)에서 크레딧을 받을 수 없도록 직접 및 내부 채널에 대한 마지막 터치 무시 옵션을 선택 취소하는 것이 좋습니다.

![](assets/int-channel2.png)

## 채널 규칙 정의

보고서에 채널 및 채널 데이터를 표시하려면 먼저 데이터를 처리하는 기초 규칙과 채널을 만들어야 합니다. 또한 [방문자 참여 기간](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/visitor-engagement.md)이 지속되는 기간을 지정할 수도 있습니다.

Adobe는 [자동 설정](/help/components/c-marketing-channels/c-getting-started-mchannel.md) 중에 사전 정의된 여러 채널을 제공하는데 이 채널은 사용자의 요구 사항에 맞게 편집할 수 있습니다. 또한 이 설정을 수정하고 [마케팅 채널 처리 규칙](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md) 내에서 맞춤형 규칙을 정의할 수 있습니다.

>[!NOTE]
>
>Adobe에서는 테스트 목적의 템플릿으로 사용할 수 있도록 보고서 세트에서 보고서를 설정할 것을 권장합니다. 템플릿을 사용하여 하나 이상의 생산 보고서 세트에 전역으로 채널 및 규칙 세트를 적용할 수 있습니다.
>
>다음을 참조하십시오 [여러 보고서 세트에 템플릿 보고서 세트 설정 적용](/help/components/c-marketing-channels/c-getting-started-mchannel.md).
