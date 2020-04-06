---
description: 마케팅 채널 관리자에서 마케팅 채널을 추가하거나 활성화합니다. 마케팅 채널이 없는 보고서 세트의 경우, 자동 설정을 통해 여러 채널을 규칙과 함께 만들 수 있습니다. 필요에 맞게 사전 정의된 채널을 편집하거나 자체 채널을 만들 수 있습니다(최대 25개).
subtopic: Marketing channels
title: 마케팅 채널 관리
topic: Reports and analytics
uuid: 9d367bb6-a17b-49b8-9cd5-24fac35ae982
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# 마케팅 채널 관리

마케팅 채널 관리자에서 마케팅 채널을 추가하거나 활성화합니다. 마케팅 채널이 없는 보고서 세트의 경우, 자동 설정을 통해 여러 채널을 규칙과 함께 만들 수 있습니다. 필요에 맞게 사전 정의된 채널을 편집하거나 자체 채널을 만들 수 있습니다(최대 25개).

다음은 채널을 만들기 위한 지침입니다.

* 모든 채널 목록을 만들어 모든 방문자 히트가 올바른 채널로 분류되도록 미리 계획하십시오.
* 항상 내부 히트 및 [직접 히트 카테고리에](/help/components/c-marketing-channels/c-faq.md) 대한 채널을 [포함합니다](/help/components/c-marketing-channels/c-faq.md) .

페이지에 채널을 추가하는 [!UICONTROL Marketing Channels] 작업은 마케팅 채널 처리 규칙 [페이지에서 규칙을 만드는 것과는 별도로](/help/components/c-marketing-channels/c-rules.md) 수행됩니다. 규칙을 만들 때 채널과 규칙을 연결합니다.

## 마케팅 채널 추가{#add-mktg-channels}를 참조하십시오 

마케팅 채널 관리자에서 마케팅 채널을 추가합니다.

>[!NOTE] 채널은 삭제할 수 없습니다. 채널을 사용하지 않으려면 비활성화하거나 이름을 바꾼 후 나중에 사용하도록 예약해 두십시오.

1. Click **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. 페이지에서 보고서 세트를 [!UICONTROL Report Suite Manager] 선택합니다.

   여러 보고서 세트를 선택하는 경우 템플릿에서 선택한 보고서 세트로 설정을 복사하는 템플릿을 선택합니다.

   See [Apply template report suite settings to multiple report suites](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

1. Click **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]**.

   보고서 세트에 정의된 채널이 없으면 [자동 설정](/help/components/c-marketing-channels/c-getting-started-mchannel.md) 페이지가 표시됩니다.

1. 페이지에서 [!UICONTROL Marketing Channel Manager] 을 클릭합니다 **[!UICONTROL Add Channel]**.

   25개의 채널이 정의된 경우에는 이 옵션을 사용할 수 없습니다.

1. 확대/축소한 후에 **[!UICONTROL Save.]**
1. 채널에 대한 규칙을 구성하려면 을 클릭합니다 **[!UICONTROL Marketing Channel Processing Rules]**.

   [마케팅 채널 처리 규칙 만들기](/help/components/c-marketing-channels/c-rules.md)를 참조하십시오.

## 마케팅 채널 관리자 - 인터페이스 정의 {#mktg-channel-mgr}

페이지의 필드 정의. [!UICONTROL Marketing Channel Manager]

| 필드 | 정의 |
|--- |--- |
| 활성화됨 | 이 마케팅 채널을 활성화하거나 비활성화합니다. |
| 채널 이름 | 마케팅 채널의 친숙한 이름입니다. |
| 마지막 터치 채널 무시 | 기존 영구 마지막 접촉 채널을 선택한 채널로 재정의할지 여부를 선택할 수 있습니다. 이 확인란을 선택하면 모든 채널(직접 및 내부 포함)이 기존 마지막 접촉 채널을 덮어씁니다. 크레딧을 받을 자격이 없는 채널에 대한 전환이 발생합니다. 예를 들어, 이 옵션은 사용자가 이전에 자연어 검색 채널을 통해 획득한 경우 직접 채널이 전환에 대한 크레딧을 받지 않도록 할 수 있습니다. |
| 채널 분류 | 이 값으로 채널을 분류할 수 있습니다. 마케팅 채널 분류를 [](/help/components/c-marketing-channels/classifictions-mchannel.md)만들 때 가능한 채널 분류(하위 채널)를 추가할 수 있습니다. |
| 유형 | 사용자가 사이트를 방문하는 방법을 지정합니다. 온라인 또는 오프라인을 선택할 수 있습니다. 검색 엔진 또는 이메일 캠페인을 통해 방문하는 방문자에 대해 온라인 채널을 사용합니다. 오프라인 채널은 신문 쿠폰이나 잡지 광고를 통해 사이트를 찾은 방문자에게 적용됩니다. 오프라인 채널에는 일반적으로 보고 데이터 소스를 통해 가져온 데이터가 포함됩니다. [ 데이터 소스](https://docs.adobe.com/content/help/ko-KR/analytics/import/data-sources/datasrc-home.html)를 참조하십시오. [오프라인 데이터 추가](/help/components/c-marketing-channels/c-getting-started-mchannel.md)를 참조하십시오. |
| 색상 | 이 마케팅 채널과 연결된 색상입니다. 이 색상은 마케팅 채널 보고서의 채널을 나타냅니다. |

## 채널 정의

채널 및 채널 데이터를 보고서에 표시하려면 먼저 데이터를 처리하는 채널과 기본 규칙을 만듭니다. 관련 채널에 대한 비용 및 예산 금액을 만들고 방문자 참여 기간이 지속될 기간을 지정할 수도 있습니다. 보고서 구성 작업은 관리자 도구에서 수행합니다.

채널을 방문 컨테이너로 간주합니다. 규칙은 적절한 컨테이너에 방문을 할당합니다.

![](assets/buckets_2.png)

Adobe는 [자동 설정](/help/components/c-marketing-channels/c-getting-started-mchannel.md) 중에 사용자의 요구 사항에 맞게 편집할 수 있는 미리 정의된 여러 채널을 제공합니다.

>[!NOTE]
>
>Adobe에서는 테스트 목적의 템플릿으로 사용할 수 있도록 보고서 세트에서 보고서를 설정할 것을 권장합니다. 템플릿을 사용하여 하나 이상의 프로덕션 보고서 세트에 전체적으로 채널 및 규칙 세트를 적용할 수 있습니다.
>
>See [Apply Template Report Suite Settings to Multiple Report Suites](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

### 전제 조건 {#prereqs}

필요한 경우 고객 지원팀에 연락하여 이러한 전제 조건에 대한 도움을 받으십시오.

* In the Administration Console (General Account Settings), enable the **[!UICONTROL Conversion Level]** (e-commerce) option for the report suite.

   자세한 내용은 Analytics 도움말의 [일반 계정 설정](https://docs.adobe.com/content/help/ko-KR/analytics/admin/admin-tools/general-acct-settings-admin.html)을 참조하십시오.

* 마케팅 채널 차원에 대한 액세스를 설정합니다.

   See [Marketing Channels permissions](/help/components/c-marketing-channels/c-channel-report-access.md).

* Ensure that your account manager has enabled **[!UICONTROL Channel Reports]** for your report suite.

### 중요한 처리 정보 {#important-proc-rules}

* 시스템은 사용자가 지정한 순서대로 규칙을 처리하고 규칙이 충족되면 시스템이 나머지 규칙 처리를 중지합니다.
* 규칙은 VISTA가 설정한 변수에 액세스할 수 있지만 VISTA가 삭제한 데이터에 액세스할 수 없습니다.
* 채널은 전환 지표만 저장합니다. 트래픽 지표를 사용할 수 없습니다.
* 두 마케팅 채널은 동일한 이벤트(구매 또는 클릭 등)에 대한 크레딧을 받지 않습니다. 이러한 방식으로 마케팅 채널은 eVar와 다릅니다(두 개의 eVar가 동일한 이벤트에 대한 크레딧을 받을 수 있는 경우).
* 보고서는 한 번에 최대 25개의 채널을 처리할 수 있습니다.

