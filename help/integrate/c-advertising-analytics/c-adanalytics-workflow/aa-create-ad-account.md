---
title: Advertising Analytics에서 광고 계정을 설정하는 방법
description: 이 문서에서는 새 광고 계정을 만들고 여러 계정을 여러 보고서 세트에 매핑하는 방법에 대해 설명합니다.
feature: Advertising Analytics
exl-id: f593c714-e85f-4000-85b2-6294cad81e25
source-git-commit: cf0f528f1ccb0346786c017b4d0d48dd5ab6dfc2
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 25%

---

# 광고 계정 설정

Adobe Analytics 관리자는 새 광고 계정을 만들고 여러 계정을 여러 보고서 세트에 매핑 (일대일, 일대다, 다대다)할 수 있습니다.

또한 관리자는 광고 계정을 설정할 [관리자가 아닌 사용자에게 액세스 권한을 부여](/help/integrate/c-advertising-analytics/overview.md#section_FCC58EB635954A32990D4E67B52B4369)할 수 있습니다.

<!--
![](assets/aa_accounts.png)
-->

1. Adobe Analytics에서 **[!UICONTROL 관리]** > **[!UICONTROL 광고 계정]**&#x200B;으로 이동합니다.
1. (처음 사용 시에만 해당) 최종 사용자 라이선스 계약서 약관에 동의합니다.
1. **[!UICONTROL + 추가]**&#x200B;를 선택합니다.
1. [!UICONTROL 새 검색 엔진 설정] 대화 상자가 표시됩니다.

   ![](assets/aa-new-se-account.png)

1. 다음 지침에 따라 **[!UICONTROL 검색 엔진 설정]**&#x200B;을 입력하십시오.

   | 설정 | 설명 |
   | --- | --- |
   | **[!UICONTROL Type]** | 두 가지 옵션이 있습니다. **[!UICONTROL Google Adwords]** 및 **[!UICONTROL Bing Ads]**.  참고: Yahoo Gemini는 2019년 3월 31일에 Microsoft Bing에 합병되었습니다. 따라서 Yahoo Gemini 광고 계정 옵션은 더 이상 사용할 수 없습니다. |
   | 계정 이름 | 이 계정 이름을 사용자에게 맞는 이름으로 설정하도록 선택할 수 있습니다.  계정 이름 은 UI에 표시되는 계정의 친숙한 이름입니다. |
   | OAuth 토큰 | **참고**: OAuth는 액세스 위임에 대한 개방형 표준으로, 일반적으로 웹 사이트 또는 응용 프로그램에 웹 사이트에 있는 정보에 액세스할 권한을 부여하는 방법으로 사용되지만 암호를 제공하지 않습니다. 사용자는 서드파티 URL(efrontier.com)로 라우팅됩니다. Adobe은 Adobe Media Optimizer를 사용하여 세 개의 검색 엔진 모두에 대한 OAuth 인증 프로세스를 진행합니다. Internet Explorer 11(또는 이전 버전)을 사용하는 경우 세 개의 검색 엔진에 대한 Oauth 토큰을 검색할 수 없습니다. 대신 다른 웹 브라우저를 사용하십시오.<p>OAuth2 인증 프로세스를 시작하려면 **[!UICONTROL 검색 토큰]**&#x200B;을 선택하십시오. 자격 증명을 사용하여 Google/Bing 검색 계정에 로그인하라는 메시지가 표시됩니다. 선택한 항목에 따라 프로세스가 약간 다릅니다. <ul><li>Google Adwords: Google 계정 ID를 제공합니다</li><li>Microsoft Bing: Bing 계정 ID 및 Bing 고객 ID를 제공합니다.</li></ul>이러한 ID에 대한 자세한 내용은 [계정 ID 찾기](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-locate-account-id.md)를 참조하세요. 성공적으로 로그인되면 **[!UICONTROL OAuth 토큰]** 필드에 **[!UICONTROL 검색됨]**&#x200B;이 표시됩니다. |

1. **[!UICONTROL 추적]** 섹션에서 Adobe Analytics 구현을 사용하여 데이터를 추적하는 방법에 대한 정보를 제공합니다. 추적은 검색 엔진 데이터를 사용하여 Adobe Analytics 데이터를 적절하게 늘리는 데 필요한 단계입니다.
다음 지침에 따라 **[!UICONTROL 추적 설정]**&#x200B;을 입력합니다.

   | 설정 | 설명 |
   | --- | --- |
   | 유형 | <ul><li>**자동**: Advertising Cloud 엔진은 추적 매개 변수가 의 추적 템플릿/대상 URL에 추가되는 방법을 결정합니다. [!UICONTROL 자동 유형 추적]은(는) 가장 간단한 방법이지만 최상의 통합 데이터 집합을 만들지 못할 수 있습니다.<br>**중요:** [!UICONTROL 자동 유형 추적]을 사용하여 검색 엔진 계정을 구성하려면 다음 작업을 수행해야 합니다.<ul><li>`s_kwcid` 매개 변수 및 값이 추가되는 계정의 계정 추적 템플릿 또는 랜딩 페이지 URL에 추가됩니다. 매개 변수와 값은 URL 끝에 삽입됩니다. 웹 서버에서 URL 끝에 특정 `key=value` 쌍이 필요한 경우 추가 작업이 필요할 수 있습니다. 또는 URL에서 새 `key=value` 쌍을 지원하는 업데이트가 필요합니다. **참고**: 이 매개 변수를 [콘텐츠 보안 정책](https://experienceleague.adobe.com/ko/docs/id-service/using/reference/csp)에 추가해야 하는지에 대해 자세히 알아보세요.</li><li>또한 `s_kwcid` 값의 일부로 랜딩 URL에 키워드를 삽입할 수 있습니다. 키워드에 특수 문자 또는 기호가 포함되어 있는 경우 웹 서버에서 해당 문자를 지원할 수 있는지 확인하십시오. 일반적인 특수 문자의 예로는 `+`이(가) 있으며, 이 문자는 &quot;Broad Match Modified&quot; 키워드에 사용됩니다.</li></ul></li><li>**수동**: 추적 매개 변수가 검색 엔진의 추적 템플릿/대상 URL에 추가되는 방식을 관리할 수 있습니다. [각 검색 엔진에 대한 이러한 수동 추적 예를 참조하십시오](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-manual-vs-automatic-tracking.md).</li></ul> |

1. **[!UICONTROL 저장]**&#x200B;을 선택합니다.
1. 면책조항에 주의 사항 목록이 표시됩니다. 이 계약서를 읽고 이해했는지 확인합니다. 확인란을 선택한 다음 **[!UICONTROL 확인]**&#x200B;을 선택합니다.

   이제 새로 작성한 계정이 나열된 광고 계정 [관리 UI](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-manage-ad-accounts.md)로 이동합니다.

>[!NOTE]
>
>검색 엔진 데이터가 Analytics 보고서에 채우기를 시작할 때까지 최소 24시간 대기해야 합니다.
