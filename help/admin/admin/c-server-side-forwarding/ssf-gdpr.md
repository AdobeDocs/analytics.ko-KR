---
description: EU 쿠키 준수 규정에서 촉발된 서버 측 전달에 대한 개선 사항을 설명합니다.
title: GDPR/ePrivacy 준수 및 서버 측 전달
feature: Server-Side Forwarding
exl-id: 54e43a16-8f15-4ee8-9aa2-579af30be2c9
source-git-commit: ee56267979979f8e03b1c6a0d849ccf994599024
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 80%

---

# GDPR/ePrivacy 준수 및 서버 측 전달

이 섹션에서는 [EU 쿠키 준수 규정](https://wikis.ec.europa.eu/display/WEBGUIDE/04.+쿠키+및+유사+기술)2017년 9월 30일부터 시행되었습니다.

서버 측 전달은 Adobe Analytics의 데이터를 Audience Manager와 같은 다른 [!DNL Experience Cloud Solutions]과 실시간으로 공유하는 데 사용됩니다. 이 기능이 활성화되어 있을 때 서버 측 전달을 사용하면 Analytics에서 데이터를 다른 Experience Cloud 솔루션에 푸시하고 데이터 수집 프로세스 중에 해당 솔루션으로 데이터를 Analytics에 푸시할 수 있습니다.

이전에는 서버 측 전달에서 동의와 사전 동의 이벤트/히트 간을 구분할 수 없었습니다. 2018년 11월 1일부터, 데이터 컨트롤러(Adobe Analytics 고객)로서 데이터 사전 동의를 Adobe Analytics로 제한하여 AAM으로 전달되지 않도록 하는 옵션이 제공됩니다. 새 구현 컨텍스트 변수를 사용하여 동의를 받지 못한 히트에 플래그를 지정할 수 있습니다. 변수를 설정하면 동의를 받을 때까지 이러한 히트가 AAM에 전송되지 않습니다.

이 새 컨텍스트 변수 `cm.ssf=1`이 히트에 있으면 이 히트에 플래그가 지정되고 서버 측에서 AAM으로 전달되지 않습니다. 반대로 이 문자열이 히트에 표시되지 않으면 히트가 AAM에 전달됩니다.

서버 측 전달은 양방향입니다. 즉, 히트에 적용되어 이 히트가 AAM에 전달되면 대상 Analytics가 AAM에서 이 히트에 대한 세그먼트 정보를 수신하여 다시 Analytics으로 전송합니다. 따라서 서버 측이 Analytics에서 AAM으로 전달하지 않은 히트에는 AAM의 세그먼트 ID 목록이 추가되지 않습니다. 그러므로 AAM에서 세그먼트 ID 정보를 가져오지 않은 트래픽/히트의 서브세트가 있게 됩니다.

## 구현 세부 정보 {#section_FFA8B66085BF469FAB5365C944FE38F7}

구현 방법에 따라 다음 단계를 수행하십시오.

| 구현 방법 | 단계 |
|--- |--- |
| Adobe Experience Platform의 태그 | Adobe Analytics 확장이 설치되어 있다고 가정할 경우 규칙의 작업 구성 내에서 다음 컨텍스트 데이터 변수 정의를 사용자 지정 코드 편집기에 추가합니다. <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' ` <br/>참고: contextdata 변수를 정의하고, 고객이 대상 마케팅에 동의하지 않은 경우 1로 설정합니다. 대상 마케팅에 동의한 고객에 대해서는 `contextdata` 변수를 *0*&#x200B;으로 설정합니다. |
| AppMeasurement | 컨텍스트 데이터 변수 정의를 AppMeasurement.js 파일에 추가합니다.  <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' ` <br/>참고: contextdata 변수를 정의하고, 고객이 대상 마케팅에 동의하지 않은 경우 1로 설정합니다. 대상 마케팅에 동의한 고객에 대해서는 contextdata 변수를 0으로 설정합니다. |

## 보고(선택 사항) {#section_6AD4028EC11C4DABA2A34469DDC99E89}

Adobe Analytics를 사용하여 동의한 트래픽 수와 그 결과 서버 측에 전달된 트래픽 수 및 동의하지 않은 트래픽 수와 그 결과 AAM에 전달되지 않은 트래픽 수를 보고할 수 있습니다.

이러한 유형의 보고를 구성하려면 처리 규칙을 통해 사용자 정의 트래픽 변수(prop)에 새 컨텍스트 변수를 매핑합니다. 이렇게 하려면 다음을 수행하십시오.

1. 위에 표시된 대로 &quot;cm.ssf&quot; 변수를 구현합니다.
1. [prop를 활성화합니다.](/help/admin/admin/c-traffic-variables/traffic-var.md)
1. 처리 규칙을 사용하여 컨텍스트 변수를 prop에 매핑합니다.

   1. **[!UICONTROL Analytics]** > **[!UICONTROL 관리]** > **[!UICONTROL 보고서 세트]**&#x200B;로 이동한 후 보고서 세트를 선택합니다.
   1. **[!UICONTROL 보고서 세트 편집]** > **[!UICONTROL 일반]** > **[!UICONTROL 처리 규칙]**&#x200B;을 클릭합니다 .
   1. **[!UICONTROL 규칙 추가]**&#x200B;를 클릭합니다.
   1. **[!UICONTROL 항상 실행]**&#x200B;에서 활성화한 prop 값을 컨텍스트 변수 &quot;cm.ssf(컨텍스트 데이터)&quot;로 덮어씁니다.
   1. **[!UICONTROL 저장을 클릭합니다]**.
