---
description: 회사는 Analytics를 사용하여 이메일 캠페인의 성공을 파악합니다.
keywords: Analytics 구현
seo-description: 회사는 Analytics를 사용하여 이메일 캠페인의 성공을 파악합니다.
seo-title: 외부 이메일 추적
solution: Analytics
title: 외부 이메일 추적
topic: 개발자 및 구현
uuid: FA 450 F 45-14 CF -4 D 0 D-A 87 C -14 A 946512 A 9 B
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 외부 이메일 추적

회사는 Analytics를 사용하여 이메일 캠페인의 성공을 파악합니다.

[!DNL Analytics]에서는 다음을 포함하여 몇 개의 주요 지표로 이메일 캠페인 분석 데이터를 보고할 수 있습니다.

| 지표 | 설명 |
|---|---|
| 클릭스루 | 이메일에서 랜딩 페이지까지 추적한 클릭스루 수를 표시합니다. |
| 구매 및/또는 성공 | 이메일에서 비롯된 구매 수를 표시합니다. |
| 주문 | 이메일의 결과로 받은 주문의 수를 표시합니다. |
| 산출 | 이메일에서 생성된 방문당 달러 금액을 표시합니다. |
| 전환 | 이메일에서 생성된 리드, 등록 또는 기타 모든 성공 이벤트의 수를 표시합니다. |

위의 주요 지표를 캡처하려면 HTML 이메일 본문과 JavaScript 라이브러리를 수정해야 합니다.

## 구현 {#section_8A42A8F4A6CD4A1BAF4B9F99F709AF7A}

이메일 캠페인 분석 데이터를 제대로 표시하려면 따라야 되는 몇 가지 단계들이 있습니다. 이 단계들은 다음과 같이 설명됩니다.

1. 고유 추적 코드를 만듭니다.

   종종, 사용자들은 각각의 고유 캠페인에 대한 추적 권장 사항을 요청합니다. 이러한 권장 사항은 가장 효과적인 방법을 기반으로 하되, 전적으로 사용자에게 달려 있습니다. 각각의 사용자는 다릅니다. 각 사용자는 아래 예에서 보듯이 친근한 추적 코드를 생성하는 것이 좋습니다.

   * sc_cid=A1123A321 &gt; "A"는 제휴 캠페인에 대한 플래그
   * sc_cid=EM033007 &gt; "EM"은 이메일 캠페인에 대한 플래그
   * sc_cid=GG987123 &gt; "GG"는 Google을 의미하며, 유료 검색 캠페인임
   추적 코드 설정 및 사용에 대한 자세한 내용은 Adobe [!DNL Customer Care]에 문의하십시오.

1. 쿼리 문자열 매개 변수를 HTML 이메일 링크에 추가합니다.

   사용자 클릭스루와 그 이후의 성공 이벤트를 추적하려면, 쿼리 문자열 매개 변수를 HTML 이메일 내의 각 링크에 추가해야 합니다. 각 링크를 따로따로 추적하거나 모든 링크를 함께 추적하도록 선택할 수 있습니다. 각 링크에 고유한 추적 코드가 있거나, 모든 링크에 동일한 추적 코드가 있을 수 있습니다. 이메일 내에 있는, 웹 사이트가 연결된 다음의 가상 링크를 생각해 보십시오.

   ```js
   <a href="https://www.mycompany.com/index.asp">Visit our home page</a>
   ```

   다음 쿼리 문자열 매개 변수 ?sc_cid=112233B를 위의 링크에 추가해야 합니다.

   ```js
   <a href= "https://www.mycompany.com/index.asp?sc_cid=112233B">Visit our home page</a>
   ```

1. JavaScript 라이브러리를 업데이트합니다.

   JavaScript 파일 [!DNL s_code.js]에서 코드를 바꾸면, 이메일을 통해 얼마나 많은 사용자, 그리고 어떤 사용자가 클릭스루를 수행하고 그 후의 성공 이벤트에 참여했는지 알 수 있습니다. JavaScript 라이브러리를 업데이트하는 두 가지 단계가 있습니다.

   1. Customize [!DNL s_code.js] by calling [!UICONTROL getQueryParam].

      [!DNL s_code.js]   파일은 각 웹 페이지가 액세스할 수 있는 웹 서버에 이 파일을 보관해야 합니다. The *`doPlugins`* function within this file should be altered so it captures the query string parameters on the email links. 예:

      ```js
      /* Plugin Config */ 
      s.usePlugins=true 
      function s_doPlugins(s) { 
       /* Add calls to plugins here */ 
       // External Campaigns 
      s.campaign=s.getQueryParam('source') 
      } 
      s.doPlugins=s_doPlugins 
      ```

      변수에 복사해야 하는 각 쿼리 문자열 매개 변수에는 하나의 [!UICONTROL getQueryParam] 호출이 있어야 합니다. 위의 예에서, 쿼리 문자열 매개 변수 [!UICONTROL sc_cid]는 *`campaign`*.

      클릭스루를 캡처하는 데는 [!UICONTROL getQueryParam]에 대한 첫 번째 호출만 필요합니다. 이 함수를 구현하고 자신의 JavaScript 파일 버전에 [!DNL Customer Care]getQueryParam[!UICONTROL  플러그인이 들어 있는지 확인하려면 Adobe ]에 문의하십시오.

   1. 붙여넣을 코드 JavaScript 태그가 모든 랜딩 페이지에 있는지 확인하십시오. 이 붙여넣을 코드는 Part A에서 바뀐 [!DNL s_code.js] 버전을 참조해야 합니다.

      다음 사항은 JavaScript 라이브러리를 업데이트할 때 기억해야 하며, 다음과 같습니다.

      * 쿼리 문자 매개 변수 [!UICONTROL sc_cid]는 최종 랜딩 페이지의 URL에서 볼 수 있어야 하며, 그렇지 않은 경우 클릭스루 전환이 기록되지 않습니다.
      * [!UICONTROL sc_cid] 매개 변수는 쿼리 문자열 매개 변수의 예입니다. 모든 쿼리 문자열 매개 변수는 [!UICONTROL getQueryParam] 플러그인에서 사용하고 캡처할 수 있습니다. 쿼리 문자열 매개 변수가 캠페인 추적에 대해서만 사용되었는지 확인하십시오. 언제든지 매개 변수가 쿼리 문자열에 나타나면, 그 값은 *`campaign`*.

1. [!UICONTROL SAINT]를 사용하여 캠페인 추적 코드를 분류합니다.

   [!UICONTROL SAINT 캠페인 관리 도구]는 추적 코드를 사용자에게 친근한 이름으로 변환하는 데 사용할 수 있으며, 각 이메일 캠페인의 성공을 요약하는 데도 사용할 수 있습니다. 다음 5단계는 이메일 캠페인을 설정할 때 필요한 프로세스에 대한 개요를 설명합니다.

1. 이메일 캠페인별로 경로 지정을 봅니다(선택 사항).

   이메일 캠페인에 의한 경로 지정 분석은 다른 캠페인에 의한 경로 지정과 유사하게 수행할 수 있습니다. 다음 단계들에 설명된 것처럼, 변수를 사용하여 캠페인별 경로 지정을 표시할 수 있습니다.

   1. [!DNL Customer Care]사용자 지정 인사이트[!UICONTROL  변수(prop)에 대한 경로 지정을 사용하는 방법에 대한 자세한 내용은 Adobe ]에 문의하십시오.

   1. 모든 페이지에서, 페이지 이름을 지정된 [!DNL s.prop]로 복사하십시오.
   1. 이메일 랜딩 페이지에서, 이메일 캠페인의 이름을 prop에 추가합니다. 결과는 아래와 같이 표시됩니다.

      ```js
      s.prop1="Home Page : 123456"
      ```

      경로 지정 기능이 [!UICONTROL 사용자 지정 인사이트] 변수에 대해 활성화되면, [!UICONTROL 경로] 보고서([!UICONTROL 다음 페이지 흐름]이나 [!UICONTROL 폴아웃] 등)를 사용하여 랜딩 페이지에서 방문자 이동을 볼 수 있습니다.

