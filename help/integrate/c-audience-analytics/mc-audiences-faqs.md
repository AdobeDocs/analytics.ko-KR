---
description: Audience Analytics을 구현할 때 나올 수 있는 질문에 대한 답변입니다.
seo-description: Audience Analytics을 구현할 때 나올 수 있는 질문에 대한 답변입니다.
seo-title: FAQ
solution: Experience Cloud
title: FAQ
uuid: 9dfc8f19-f9b2-4c2e-bff9-3d91cfe01bca
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# FAQ

Audience Analytics을 구현할 때 나올 수 있는 질문에 대한 답변입니다.

## 법적 FAQ {#section_B51CFC961C0B45A2BE5F4A4404620764}

<table id="table_22037CCB516C4231BF5820004FBB351A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <b>Q: 내 Analytics 데이터에 PII(개인식별정보)가 있는지 어떻게 알 수 있습니까? 알 수 있다면, 어떻게 해야 합니까?</b> </td> 
   <td colname="col2"> 
    <ul id="ul_71E0ECD5981D4B65BCDA065BE07A43AA"> 
     <li id="li_F8FF61A4D7B54BA39DAA6F28DB51D749">prop 또는 eVar에 이메일/주소/등이 있는 경우 수집 중에 데이터 해싱을 고려하십시오. </li> 
     <li id="li_57A8B4C7BB784FFCBC1DC363B35D9FF7">해당 국가에서 IP 주소 PII로 고려하는 경우 <a href="https://marketing.adobe.com/resources/help/en_US/reference/exclude_IP.html" format="html" scope="external">IP 난독화</a>를 켭니다 . </li> 
     <li id="li_C7AA02B831AE47A59E783623126A7789">Analytics 관리자에게 사용자가 수집 중인 것을 확인하라고 말합니다. </li> 
     <li id="li_F6AAE868141E486AB8CAB291BD8EDB71">법률 부서에 그들이 PII에 대해 고려하는 것을 확인하라고 말합니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Q: 보고서 세트에서 온사이트 개인화를 수행하는지 아니면 오프사이트/온사이트 타깃팅을 수행하는지 어떻게 알 수 있습니까?</b> </td> 
   <td colname="col2"> 
    <ul id="ul_F0984CEF80DB4B589716BC55549E32B8"> 
     <li id="li_9BC3819784A9408F846D60FF0F20AAF9">이러한 사항은 Adobe Audience Manager에 Adobe Analytics 데이터 보내기에 적용되지 않습니다. </li> 
     <li id="li_050A1BF9978E436895B5C7E33A82527D">스스로에게 질문하기: MCA 차원과 Analytics 공유 세그먼트를 다시 Experience Cloud와 공유하시겠습니까? </li> 
     <li id="li_C52D969681B94F4AAA18FDEB21EC5B49">이러한 목적에 사용되는 BI(비즈니스 인텔리전스) 시스템으로 데이터 피드 등을 통해 내보내시겠습니까? </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 관련 FAQ {#section_6BDF746BA6464359A6A89A64EB025D12}

<table id="table_15B44592161240BDA79F3B020EA9CC9D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Q: Audience Manager에서 Analytics 대상을 만들려면 어떻게 합니까?</b> </p> </td> 
   <td colname="col2"> AAM <a href="https://marketing.adobe.com/resources/help/en_US/aam/create-analytics-destination.html" format="html" scope="external"> 에서 분석 대상 구성을 참조하십시오 </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: Analytics 대상을 만들고 저장한 후 선택한 보고서 세트에 데이터가 나타날 때까지 얼마나 걸립니까?</b> </p> </td> 
   <td colname="col2"> <p>새 데이터로 보고서 세트를 채우는 데 몇 시간이 걸릴 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: 새로운 Analytics 대상을 만들었지만 사용할 수있는 세그먼트의 대상 매핑 섹션에는 표시되지 않습니다. 해당 대상이 이동한 위치 또는 찾는 방법은 무엇입니까?</b> </p> </td> 
   <td colname="col2"> <p><span class="uicontrol">세그먼트 매핑</span>에서 <span class="uicontrol">자동으로 모든 현재 및 향후 세그먼트 매핑</span> 옵션을 선택하면 세그먼트의 대상 매핑 섹션에서 Analytics 대상이 사라집니다 . </p> <p><img placement="break" align="left"  src="assets/auto-mapping.png" id="image_670ED5A306784FCBA8A0B336AC1F0FC6" width="300px" /> </p> <p>이를 방지하려면 자동 옵션 대신 <span class="uicontrol">수동으로 세그먼트 매핑</span>을 선택하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Q:이렇게 하면 Analytics에서 AAM의 모든 정보가 제공됩니까?</b> </p> </td> 
   <td colname="col2"> <p>아니요, Audience Manager 대상 지원 중 또는 후에 그리고 세그먼트 자격 조건 중/후에 사이트를 방문한 사람과 관련된 데이터만 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Q: 이 경우 세그먼트별 지정 가능한 대상을 제게 제공합니까?</b> </p> </td> 
   <td colname="col2"> <p>실제로 그렇지 않습니다. 세그먼트 자격 조건 중 또는 후에 사이트로 돌아온 해당 세그먼트의 방문자 수를 알려줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Q: 기존 쿠키 대상과 Analytics에서 어떻게 다릅니까?</b> </p> </td> 
   <td colname="col2"> <p>세그먼트는 동일한 히트에서 실시간으로 자격을 부여받고 반환됩니다. </p> <p>친숙한 이름이 자동으로 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: 일부 보고서 세트에 개인 데이터가 있고 일부 데이터 세트에는 없는 경우 어떻게 합니까?</b> </p> </td> 
   <td colname="col2"> <p>팁: 두 개의 대상을 만들어, 한 대상에는 개인 데이터 보고서 세트를 추가하고 다른 대상에는 비개인 데이터 보고서 세트를 추가합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Analytics 관련 FAQ {#section_67BFB1B1E48D4113A38B075C020931BA}

<table id="table_19AEAE0A3575423CB4F5F164DB5626D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Q: 이 통합이 Analytics의 차원 또는 세그먼트로 나타납니까?</b> </p> </td> 
   <td colname="col2"> <p>차원: 대상 ID 및 대상 이름에서 보냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: 이러한 차원을 Analytics의 어디에서 사용할 수 있습니까?</b> </p> </td> 
   <td colname="col2"> <p>어디서나 사용할 수 있습니다. 이러한 차원은 Analytics에 수집된 다른 차원과 마찬가지로 취급됩니다. 두 가지 예외가 있습니다. 지금은 데이터가 Data Workbench 또는 Livestream에 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: Analytics에 데이터가 전달되지 않는 이유는 무엇입니까?</b> </p> </td> 
   <td colname="col2"> <p>데이터 소스와 대상 간의 AAM 개인정보 컨트롤이 충돌할 가능성이 큽니다.에서 보냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: 모든 세그먼트를 보내도록 선택했지만 일부 세그먼트가 Analytics에 표시되지 않는 이유는 무엇입니까?</b> </p> </td> 
   <td colname="col2"> 
    <ul id="ul_B8938FD08C6F4F2387EDADDEF8089319"> 
     <li id="li_50A9BDF612304062913370F16BC882EF">대상 및 세그먼트의 데이터 소스에 있는 AAM 데이터 내보내기 컨트롤이 충돌하여 특정 세그먼트가 전송되지 않을 수 있습니다. </li> 
     <li id="li_AF5D6F883D6F4D3192E0BF23CF12ADEA">세그먼트에서 타사 데이터 트레이트를 사용하는 경우 해당 세그먼트를 개인 데이터가 포함된 대상(보고서 세트)에 공유할 수 없습니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q:내 Analytics 보고서에 "대상자 제한에 도달함"이 표시되는 이유는 무엇입니까? (참고:이 값은 데이터 웨어하우스에서 대상 ID = -1 및 "::max_audiences_exceeded::"로 표시됩니다.)</b> </p> </td> 
   <td colname="col2"> <p>기본적으로 AAM에 대한 Audience Analytics 통합은 방문자가 대상인 모든 세그먼트를 히트별로 Analytics에 보냅니다. 방문자가 한 번의 히트에서 150개 이상의 AAM 세그먼트에 속하면 <b>가장 최근에 자격을 갖춘 150개의 세그먼트</b>가 Analytics로 전송되고 나머지 목록은 잘립니다. </p> <p>세그먼트 목록이 잘렸음을 나타내는 추가 플래그가 Analytics에 전송되고, 대상 이름 차원에 "대상 제한에 도달했습니다."로 표시되고 대상 ID 차원에 "-1"로 표시됩니다. </p> <p>방문자가 특정 히트에서 150개 이상의 세그먼트에 대해 자격을 얻는 것은 거의 불가능하지만, 가끔 발생할 수 있습니다. 보고서에 "대상 제한에 도달했습니다."가 표시되면 다음 두 가지 옵션을 사용할 수 있습니다. </p> 
    <ul id="ul_8E290B2E32DC49738F6FD00CB0CE2BBB"> 
     <li id="li_12F498981EA949B5BCBD40ECC954C339"><b>옵션 1</b>: 통합을 기본 상태로 계속 작업하면서 특정 방문자에 대해 가장 최근에 자격을 얻은 150개의 세그먼트를 전송합니다. </li> 
     <li id="li_CA4D5747AA4A4452929097807B604959"><b>옵션 2</b>: AAM에서 통합을 위해 비즈니스에 가장 중요한 150개의 세그먼트를 선택합니다. 그러면 AAM이 그러한 150개의 세그먼트에 대해서만 방문자를 확인합니다. 이 방법의 단점은 모든 방문자에 대해 그러한 150개의 세그먼트만 수신한다는 것입니다. 반면에 옵션 1 방법은 통합의 히트별 특성으로 인해 세그먼트를 무제한으로 전달할 수 있습니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: 이 통합을 위해 추가 서버 호출에 대한 비용이 Analytics에 청구됩니까?</b> </p> </td> 
   <td colname="col2"> <p>아니요. AAM 대상은 Analytics의 히트 서버측에 통합됩니다. 이 경우 Analytics에 대한 추가 서버 호출이 발생하지 않습니다(기본 또는 보조). </p> </td> 
  </tr> 
 </tbody> 
</table>

## SSF(서버측 전달) FAQ {#section_ADDE84ABCA0D4906B6235E92D185E0C6}

<table id="table_B7067B70FF85498896801F58D716202F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Q: 이전 SSF를 구현한 경우 Analytics 관리자로 이동하여 보고서 세트 SSF를 켜야 합니까?</b> </p> </td> 
   <td colname="col2"> <p>예. AAM 대상 설정에서 SSF가 켜져 있는 보고서 세트만 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: Analytics 관리자의 SSF에 대한 특정 보고서 세트를 켤 수 없는 이유는 무엇입니까?</b> </p> </td> 
   <td colname="col2"> <p>Experience Cloud 조직에 매핑된 세트만 활성화할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

이 항목에 대한 자세한 FAQ는 서버측 [전달 FAQ를 참조하십시오](/help/admin/admin/c-server-side-forwarding/ssf-faq.md).

## 일반 FAQ {#section_E55410BBFB624AAFB87ADCF7F036DDA3}

<table id="table_1F7C0C785F9C472286A96F8C25E8440B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Q: Audience Manager와 Analytics 간에 세그먼트 방문자 수가 다른 이유는 무엇입니까?</b> </p> </td> 
   <td colname="col2"> <p>자세한 내용은 <a href="../../integrate/c-audience-analytics/visitor-count-reconciliation.md#concept_03DD2B594C2B4D23907D5272DDFADFA0" format="dita" scope="local"> 방문자 수 차이 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: AAM의 "대상"과 Analytics의 "세그먼트"의 차이점은 무엇입니까?</b> </p> </td> 
   <td colname="col2"> <p>자세한 내용은 <a href="../../integrate/c-audience-analytics/aam-analytics-segments.md#concept_AB72F76AFAF14F82A5BB17809925813B" format="dita" scope="local"> Understand Segments in Analytics and Audience Manager </a>. </p> <p>AAM 대상이 전송되어 Analytics에서 사용할 "차원" 구성 요소로 공유됩니다. 세그먼트 빌더에서는 세그먼트로 표시되지 않지만, 세그먼트를 만들 수 있는 차원으로 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: 고객 특성과 AAM에서 통합된 고객 데이터의 차이점은 무엇입니까?</b> </p> </td> 
   <td colname="col2"> <p>고객 특성은 시간을 기반으로 하지 않으며, 소급하여 적용하고 진행합니다. AAM 통합 데이터는 시간을 기반으로 하며, 앞으로 진행됩니다. 또한 고객 특성은 Experience Cloud 방문자 ID에 대한 조회 테이블이지만, AAM 통합은 방문자의 각 히트에 결합된 데이터입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: 이전 베타 또는 컨설팅 플러그인 쿠키 대상 등, 이 문제에 대한 기존 접근 방법은 무엇입니까?</b> </p> </td> 
   <td colname="col2"> <p>새 통합을 구현하고 이전 대상을 제거하는 것이 좋습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

