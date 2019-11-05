---
description: Adobe Analytics 구현을 구현하기 위한 최초 고객 환경에 대해 알아보십시오.
keywords: 시작하기
seo-description: Adobe Analytics 구현을 구현하기 위한 최초 고객 환경에 대해 알아보십시오.
seo-title: 간소화된 구현 모달
solution: Analytics
subtopic: Analysis Workspace
title: 간소화된 구현 모달
topic: Reports and Analytics
uuid: 6fad2c1f-476c-4985-90df-7c222e751ddc
translation-type: tm+mt
source-git-commit: 57fe1f6d613b9f54a5191ac8684d36bccfebf4e5

---


# 간소화된 구현 모달

Adobe Analytics 구현을 구현하기 위한 최초 고객 환경에 대해 알아보십시오.

<!-- 

<p>https://activation.adobedtm.com/index.php?redirected=1 </p>

 -->

새 사용자는 이 *`Getting Started with Adobe Analytics`* 설정 모달을 사용하여 첫 번째 [!DNL Analytics] 보고서 세트(데이터 저장소)를 신속하게 만들 수 있습니다. 그런 다음 [!DNL Dynamic Tag Management]를 사용하여 [!DNL Analytics] 코드를 배포할 수 있습니다.

[!DNL Dynamic Tag Management]를 사용하면 사이트를 매번 변경할 필요 없이 Adobe Analytics 구현을 관리할 수 있습니다. 모바일 앱을 구현하는 경우 앱에서 중요한 데이터 수집을 시작하는 데 필요한 SDK를 받을 수 있습니다.

이 절차에서 다음을 수행할 수 있습니다.

* 첫 번째  [보고서 세트](https://marketing.adobe.com/resources/help/en_US/analytics/getting-started/report-suites.html)를 빠르게 만듭니다.
* 배포 [!DNL Analytics] 및 ID [서비스](https://marketing.adobe.com/resources/help/en_US/mcvid/).

* 기본 페이지 수준 데이터에서 보고서를 실행합니다.

> [!NOTE] 시작하기 전에 Adobe Experience Cloud에서 Analytics가 [활성화되어 있는지](https://marketing.adobe.com/resources/help/en_US/mcloud/core_services.html) 확인합니다(솔루션 제공 프로세스). Enterprise Dashboard에서 Analytics에 로그인하라는 이메일 초대를 받으면 사전 요구 사항을 완료한 것입니다.

**간단한 구현 양식을 실행하려면**

1. Log in to the [!DNL Adobe Experience Cloud] ( [experiencecloud.adobe.com](https://experiencecloud.adobe.com)).

   [!DNL Analytics]에 액세스하면 시스템이 사용자에게 보고서 세트가 있는지 판단합니다. 없는 경우 [!UICONTROL Adobe Analytics 시작하기] 페이지가 표시됩니다.

   ![](assets/analytics-implementation-rs-wizard.png)

   또는 **[!UICONTROL 도움말]** &gt; **[!UICONTROL Adobe Analysis에 오신 것을 환영합니다.]**&#x200B;를 클릭하여 [!DNL Analytics]에서 이 설정을 실행할 수 있습니다.

1. 비즈니스에 대한 다음 기본 정보를 제공합니다. 

   <table id="table_1741878A1B284CB78D297D531DC703D6"> 
     <thead> 
      <tr> 
       <th colname="col1" class="entry"> 요소 </th> 
       <th colname="col2" class="entry"> 설명 </th> 
      </tr> 
     </thead>
     <tbody> 
      <tr> 
       <td colname="col1"> <p>속성 유형 </p> </td> 
       <td colname="col2"> <p>웹, 모바일 또는 두 가지 모두에 대한 구현입니까? </p> </td> 
      </tr> 
      <tr> 
       <td colname="col1"> <p>업종 </p> </td> 
       <td colname="col2"> <p>회사가 수익을 얻는 방식을 지정합니다(제품, 고객 서비스, 리드, 브랜드 인지도, 광고). </p> </td> 
      </tr> 
      <tr> 
       <td colname="col1"> <p>데이터 레이어 </p> </td> 
       <td colname="col2"> <p>(권장) 정보를 저장하는 데 사용된 JavaScript 배열. Dynamic Tag Management를 사용하여 자동 설정을 수행하는 경우 데이터 레이어를 사용하게 됩니다. </p> <p>데이터 계층에 대한 블로그에 대해서는 <a href="https://blogs.adobe.com/digitalmarketing/analytics/data-layers-buzzword-best-practice/">데이터 계층: 유행어부터 우수 사례까지 </a>를 참조하십시오. </p> </td> 
      </tr> 
      <tr> 
       <td colname="col1"> <p>데이터 저장소(보고서 세트) </p> </td> 
       <td colname="col2"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/analytics/getting-started/report-suites.html">보고서 세트</a>는 일반적으로 한 속성(사이트 또는 앱)이나 브랜드에 해당하는 개별 데이터 세트입니다. 각 보고서 세트에는 고유한 보고서와 지표 세트가 있습니다. </p> </td> 
      </tr> 
      <tr> 
       <td colname="col1"> <p>시간대 </p> </td> 
       <td colname="col2"> <p>현지 표준 시간대. (자동으로 감지됨) </p> </td> 
      </tr> 
      <tr> 
       <td colname="col1"> <p>예상 페이지 보기 수 </p> </td> 
       <td colname="col2"> <p>사이트가 일별로 받는 대략적인 페이지 보기 수. </p> </td> 
      </tr> 
      <tr> 
       <td colname="col1"> <p>기본 통화 </p> </td> 
       <td colname="col2"> <p>거래하는 통화. </p> </td> 
      </tr> 
     </tbody> 
    </table>

1. **[!UICONTROL 다음]**&#x200B;을 클릭합니다.

   시스템에서 보고서 세트를 만듭니다.

1. 배포를 시작하려면 **[!UICONTROL 다음]**&#x200B;을 클릭하고 다음 옵션 중 하나를 클릭합니다.

   <table id="table_71C7F7B9677346CD8D5130519D32464B"> 
     <thead> 
      <tr> 
       <th colname="col1" class="entry"> 요소 </th> 
       <th colname="col2" class="entry"> 설명 </th> 
      </tr> 
     </thead>
     <tbody> 
      <tr> 
       <td colname="col1"> <p>배포 </p> </td> 
       <td colname="col2"> <p> Analytics에 로그인하고 배포할 수 있는 <span class="keyword">Dynamic Tag Management</span>를 시작합니다. 이 절차는 <span class="filepath">AppMeasurement.js</span> 파일과 ID 서비스(<span class="filepath"> VisitorAPI.js</span>)를 자동으로 구현합니다. </p> <p> <p>중요: 새 브라우저 탭에 Dynamic Tag Management를 통해 <span class="keyword">Adobe Analytics</span> 배포를 안내하는 도움말 페이지가 표시됩니다. </p> </p> </td> 
      </tr> 
      <tr> 
       <td colname="col1"> <p>다운로드 </p> </td> 
       <td colname="col2"> <p> 설치 파일 <span class="filepath">INSTALL-ME &lt;report suite name&gt;.js</span>를 다운로드합니다. 이 옵션은 <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/js_implementation.html">JavaScript 구현</a>을 이해하는 고급 사용자용입니다. </p> <p> <p>중요: 코드 다운로드는 <span class="keyword">Analytics</span> 배포를 구성하지 않습니다. 이 배포는 사이트의 페이지에서 또는 Adobe 컨설팅 서비스를 통해 수행하는 수동 배포입니다. </p> </p> </td> 
      </tr> 
     </tbody> 
    </table>

1. 보고서 실행.

   Analytics 도구를 배포한 후 Reports &amp; Analytics에서 보고서를 실행하여 데이터가 사이트에 도달하는지 확인할 수 있습니다. (Analytics 인터페이스에 대한 자세한 내용은  [로그인 및 탐색](https://marketing.adobe.com/resources/help/en_US/analytics/getting-started/analytics-navigation.html)을 참조하십시오.)

   예를 들면 **[!UICONTROL 사이트 지표]** &gt; **[!UICONTROL 실시간]**&#x200B;을 사용하여 즉시 데이터를 볼 수 있습니다.

   >[!NOTE]
   >
   >[!UICONTROL 실시간] 보고서를 실행하려면 몇 가지 구성이 필요합니다. [실시간 보고서 구성](https://marketing.adobe.com/resources/help/en_US/reference/t_realtime_admin.html)을 참조하십시오.

**예제 실시간 보고서**

![](assets/real-time-report.png)
