---
description: 'null'
seo-description: 'null'
seo-title: GDPR/e개인 정보 보호 규정 준수 및 서버측 전달
title: GDPR/e개인 정보 보호 규정 준수 및 서버측 전달
uuid: 1b90c567-3321-4dbd-a699-38c04e809fa4
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# GDPR/e개인 정보 보호 규정 준수 및 서버측 전달

이 섹션에서는 2017년 9월 30일에 시행된 [EU 쿠키 준수 규정](https://ec.europa.eu/ipg/basics/legal/cookies/index_en.htm)에서 서버 측 전달에 대한 최근 개선된 내용을 설명합니다.

Server-side forwarding is used to share data from Adobe Analytics to other [!DNL Experience Cloud Solutions], such as Audience Manager, in real time. 이 기능이 활성화되어 있을 때 서버 측 전달을 사용하면 Analytics에서 데이터를 다른 Experience Cloud 솔루션에 푸시하고 데이터 수집 프로세스 중에 해당 솔루션으로 데이터를 Analytics에 푸시할 수 있습니다.

최근까지 서버 측 전달은 동의와 사전 동의 이벤트/히트를 설명할 방법이 없었습니다. 2018년 11월 1일부터, 데이터 컨트롤러(Adobe Analytics 고객)로서 데이터 사전 동의를 Adobe Analytics로 제한하여 AAM으로 전달되지 않도록 하는 옵션이 제공됩니다. 새 구현 컨텍스트 변수를 사용하여 동의를 받지 못한 히트에 플래그를 지정할 수 있습니다. 변수를 설정하면 동의를 받을 때까지 이러한 히트가 AAM에 전송되지 않습니다.

When this new context variable, `cm.ssf=1`, exists on a hit, this hit gets flagged and does not get server-side-forwarded to AAM. 반대로 이 문자열이 히트에 표시되지 않으면 히트가 AAM에 전달됩니다.

서버 측 전달은 양방향입니다. 즉, 히트에 적용되어 이 히트가 AAM에 전달되면 대상 Analytics가 AAM에서 이 히트에 대한 세그먼트 정보를 수신하여 다시 Analytics으로 전송합니다. 따라서 서버 측이 Analytics에서 AAM으로 전달하지 않은 히트에는 AAM의 세그먼트 ID 목록이 추가되지 않습니다. 그러므로 AAM에서 세그먼트 ID 정보를 가져오지 않은 트래픽/히트의 서브세트가 있게 됩니다.

## 구현 세부 정보 {#section_FFA8B66085BF469FAB5365C944FE38F7}

구현 방법에 따라 다음 단계를 수행하십시오.

| 구현 방법 | 단계 |
|--- |--- |
| Adobe Experience Platform Launch | Adobe Analytics 익스텐션이 설치되어 있다고 가정할 경우 규칙의 작업 구성 내에서 다음 컨텍스트 데이터 변수 정의를 사용자 지정 코드 편집기에 추가합니다.참고 <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' `<br/>사항: 컨텍스트 데이터 변수를 정의하고 고객이 타깃팅된 마케팅에 동의하지 않는 경우 1로 설정합니다. Set the `contextdata` variable to *0* for customers who consented to targeted marketing. |
| DTM | 사용자 정의 페이지 코드 편집기에 컨텍스트 데이터 변수 정의를 추가합니다. <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' ` <br/>참고: contextdata 변수를 정의하고, 고객이 대상 마케팅에 동의하지 않은 경우 1로 설정합니다. 대상 마케팅에 동의한 고객에 대해서는 contextdata 변수를 0으로 설정합니다. |
| AppMeasurement | 컨텍스트 데이터 변수 정의를 AppMeasurement.js 파일에 추가합니다.  <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' ` <br/>참고: contextdata 변수를 정의하고, 고객이 대상 마케팅에 동의하지 않은 경우 1로 설정합니다. 대상 마케팅에 동의한 고객에 대해서는 contextdata 변수를 0으로 설정합니다. |

## 보고(선택 사항) {#section_6AD4028EC11C4DABA2A34469DDC99E89}

Adobe Analytics를 사용하여 동의를 기반으로 한 트래픽 수와 그 결과 서버 측에서 전달된 트래픽 중 동의 기반이 되지 않은 트래픽과 AAM에 전달되지 않은 트래픽의 양을 보고할 수 있습니다.

이러한 유형의 보고를 구성하려면 처리 규칙을 통해 사용자 정의 트래픽 변수(prop)에 새 컨텍스트 변수를 매핑합니다. 이렇게 하려면 다음을 수행하십시오.

1. "cm.ssf" 변수를 구현합니다(위에 표시된 대로).
1. [prop를 활성화합니다.](/help/admin/admin/c-traffic-variables/traffic-var.md)
1. 처리 규칙을 사용하여 컨텍스트 변수를 prop에 매핑합니다.

   1. Go to  **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]** , then select a report suite.
   1. Click  **[!UICONTROL Edit Report Suite]** &gt; **[!UICONTROL General]** &gt; **[!UICONTROL Processing Rules]** .
   1. **[!UICONTROL 규칙 추가를 클릭합니다.]**
   1. Under **[!UICONTROL Always Execute]**, overwrite the value of the prop you had enabled with the context variable "cm.ssf(Context Data)".
   1. **[!UICONTROL 저장을 클릭합니다]**.

