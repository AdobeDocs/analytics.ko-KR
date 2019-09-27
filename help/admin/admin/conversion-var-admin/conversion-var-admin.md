---
description: 사용자 지정 인사이트 전환 변수(또는 eVar)는 사이트에서 선택된 웹 페이지의 Adobe 코드에 삽입됩니다. eVar의 기본 목적은 사용자 지정 마케팅 보고서의 전환 성공 지표를 세그먼트화하는 것입니다. eVar는 방문 기준이며 쿠키와 유사한 기능을 수행할 수 있습니다. eVar 변수로 전달된 값은 사전 결정된 기간 동안 사용자를 따릅니다.
keywords: eVar
seo-description: 사용자 지정 인사이트 전환 변수(또는 eVar)는 사이트에서 선택된 웹 페이지의 Adobe 코드에 삽입됩니다. eVar의 기본 목적은 사용자 지정 마케팅 보고서의 전환 성공 지표를 세그먼트화하는 것입니다. eVar는 방문 기준이며 쿠키와 유사한 기능을 수행할 수 있습니다. eVar 변수로 전달된 값은 사전 결정된 기간 동안 사용자를 따릅니다.
seo-title: 전환 변수(eVar)
solution: Analytics
title: 전환 변수(eVar)
topic: 관리 도구
uuid: 1eed0cb1-0735-4142-be21-43f264216b50
translation-type: tm+mt
source-git-commit: 3c5cc9275c9978caf57e4e29704e23405ac24b65

---


# 전환 변수(eVar)

사용자 지정 인사이트 전환 변수(또는 eVar)는 사이트에서 선택된 웹 페이지의 Adobe 코드에 삽입됩니다. eVar의 기본 목적은 사용자 지정 마케팅 보고서의 전환 성공 지표를 세그먼트화하는 것입니다. eVar는 방문 기준이며 쿠키와 유사한 기능을 수행할 수 있습니다. eVar 변수로 전달된 값은 사전 결정된 기간 동안 사용자를 따릅니다.

eVar이 방문자에 대한 값으로 설정될 때 Adobe는 값이 만료될 때까지 해당 값을 자동으로 기억합니다. eVar 값이 활성일 때 방문자가 발견하는 성공 이벤트는 eVar 값으로 카운트됩니다.

eVar는 다음과 같은 원인과 결과를 측정하는 데 가장 적절하게 사용됩니다.

* 매출액에 영향을 준 내부 캠페인
* 등록에 결정적인 영향을 준 배너 광고
* 주문을 하기 전에 내부 검색을 사용한 횟수

트래픽 측정 또는 경로 지정을 원하는 경우 트래픽 변수 사용이 권장됩니다.

>[!NOTE]
>
>Only a single value can be stored in an eVar in an image request. eVar 값에 여러 값을 사용할 수 있는 경우 [목록 변수(list vars)](https://marketing.adobe.com/resources/help/en_US/sc/implement/listN.html)를 구현하는 것이 좋습니다.

## 전환 변수 - 설명 {#section_7C317BB0287A4B8EB0A1A4ECC40627BF}

Descriptions of fields used when [editing conversion variables](../../../admin/admin/conversion-var-admin/t-conversion-variables-admin.md#task_051920D9B3E24A00A28F32EEBBB0EF97).

<table id="table_E48D50926E6B492183300CA58A886927"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>요소 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> 이름 </span> </p> </td> 
   <td colname="col2"> <p>전환 변수의 친숙한 이름. 이 이름은 eVar가 일반 보고에서 참조되는 방식이며 왼쪽 메뉴에서 보고서의 이름이 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol">유형</span> </p> <p>(eVar만) </p> </td> 
   <td colname="col2"> <p>변수 값 유형은 다음과 같습니다. </p> <p> <b></b> Text String: Captures text values used on your site. </span> 이것은 eVar의 가장 흔한 유형으로, 기본 설정입니다. 이것은 다른 변수와 유사하게 작동하며, 변수 내 값은 정적 텍스트 문자열입니다. 이것은 내부 캠페인 또는 내부 검색 키워드와 같은 것을 추적할 경우 권장되는 설정입니다. </p> <p> <b></b> 카운터</span>:성공 이벤트 전에 작업이 발생하는 횟수를 카운트합니다. 예를 들어 eVar를 사용하여 사이트에서 내부 검색을 추적하는 경우 이 값을 <span class="uicontrol">텍스트 문자열</span>로 설정하면 검색어 사용을 추적할 수 있습니다. 사용된 검색어에 관계없이 검색 횟수를 카운트하려면 이 값을 <span class="uicontrol">카운터</span>로 설정합니다. 예를 들어 카운터 eVar를 사용하여 어떤 사람이 구매를 하기 전에 내부 검색을 사용한 횟수를 추적할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> 할당 </span> </p> </td> 
   <td colname="col2"> <p>변수가 이벤트 이전에 여러 개의 값을 받을 경우 Analytics가 성공 이벤트에 대한 크레딧을 할당하는 방법을 결정합니다. 지원되는 값은 다음과 같습니다. </p> <p> <b>최근</b>:마지막 eVar 값은 해당 eVar가 만료될 때까지 성공 이벤트에 대한 크레딧을 항상 받습니다. </p> <p> <b>Original Value</b>: The first eVar always receives credit for success events until that eVar expires. </p> <p> <b> Linear</b>:Allocates success events equally across all eVar values. 선형 할당은 단일 방문 내에만 값을 정확하게 분배하므로 선형 할당은 방문의 eVar 만료와 함께 사용합니다. </p> <p>참고: 할당을 선형으로 또는 반대로 전환하면 내역 데이터가 표시되지 않습니다. 보고 인터페이스에서 할당 유형을 혼합하면 보고서에 데이터가 잘못 명시될 수 있습니다. 예를 들어 선형 할당은 다양한 eVar 값으로 매출액을 나눌 수 있습니다. 다시 가장 최근 할당으로 변경하면 해당 매출액의 100%가 가장 최근의 단일 값과 연결됩니다. 이러한 연결로 인해 사용자들은 잘못된 결론을 내릴 수 있습니다. </p> <p>보고 시 혼란의 가능성을 피하기 위해 Analytics는 인터페이스에서 내역 데이터를 사용할 수 없게 합니다. 내역 데이터에 액세스하기 위해 간단히 eVar 할당 설정을 변경해서는 안 되지만, 지정된 eVar를 다시 초기 할당 설정으로 변경하기로 결정하면 이 데이터를 볼 수 있습니다. 이미 기록 중인 데이터에 대해 새 할당 설정을 원할 때는 이미 상당한 양의 내역 데이터가 누적된 eVar의 할당 설정을 변경하는 것보다, 새 eVar를 사용하는 것이 좋습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> 다음 날짜 이후에 만료</span> </p> </td> 
   <td colname="col2"> <p>eVar 값이 만료된 후 기간 또는 이벤트를 지정합니다(더 이상 성공 이벤트에 대한 크레딧을 받지 않음). 성공 이벤트가 eVar 만료 후 발생하는 경우 값이 해당 이벤트에 대한 크레딧을 받지 않습니다(eVar가 활성화되지 않았음). </p> <p>이벤트를 만료 값으로 선택하면 이 이벤트가 발생하는 경우에만 해당 변수가 만료됩니다. 해당 이벤트가 발생하지 않으면 해당 변수가 만료되지 않습니다. </p> <p>사용 가능한 만료 옵션은 다음 네 가지 기본 범주로 분류될 수 있습니다. </p> 
    <ul id="ul_810A37C9B6624F429F2FB45C18F7B43F"> 
     <li id="li_654D9D9044EC4E61AA7ABA372DBF8A93"><b>페이지 뷰 또는 방문 수준에서.</b> 페이지 보기 또는 방문 범주를 벗어나는 전환 이벤트는 eVar과 연결되지 않습니다. </li> 
     <li id="li_689FBC8B4DAC41B3B0166E6586DD1990"><b>일, 주, 월 또는 년과 같은 기간 기준.</b>지정된 기간 이상의 전환 이벤트는 eVar과 연결되지 않습니다. 만료 기간은 변수가 설정될 때 시작됩니다. eVar은 초(분, 시간, 일, 월 등)로 설정된 시간을 기반으로 하여 만료됩니다. 
      <ul id="ul_80C7E3182B6B4356B8A3CA920B81C6D5"> 
       <li id="li_F16F60319CCE406D9EDEFEC0A200BC4D">MINUTE=60초 </li> 
       <li id="li_45F47F3F5691415B84052B235DF3BB54">HOUR=3600초(60분) </li> 
       <li id="li_5288CE7D168E4C85B3D9BB67A44D32EC">DAY=86400초(24시간) </li> 
       <li id="li_60FC8BCD657745EE87B4E458CBA69583">WEEK=604800초(7일) </li> 
       <li id="li_7A05A66613C84F929F030310B9567CF5">MONTH=2678400초(31일) </li> 
       <li id="li_DCD3CABF59E34D5999B03E606B08AD85">QUARTER=8035200초(93일 - 3개월 31일) </li> 
       <li id="li_54351D2899454D39A8BA205910D2CCB1">YEAR=31536000초(365일) </li> 
      </ul> <p> </p> <p>방문이 월요일 오전 7시에 시작되고 eVar이 오전 7시 15분에 해당 방문 이내로 설정된 경우 만료가 아래와 같이 표시됩니다. </p> 
      <ul id="ul_72B311006BE6428698313D251C0940DB"> 
       <li id="li_50925D4A40AD4ACA88704A523138C5B9">일 만료: eVar이 화요일 오전 7시 15분에 만료됩니다. </li> 
       <li id="li_25846328766D4B4BAF407236C65C956C">주 만료: eVar이 다음 월요일 오전 7시 15분에 만료됩니다. </li> 
       <li id="li_82DB2D7F53304623A5E1241D75C7DF94">월 만료: eVar이 월요일 오전 7시 15분부터 31일 후에 만료됩니다. </li> 
      </ul> </li> 
     <li id="li_C132C5C5A5344B91BDF5EB6A1C717C37"><b>특정 전환 이벤트.</b> 특정 이벤트가 지정된 후 실행되는 다른 전환 이벤트가 eVar과 연결됩니다. </li> 
     <li id="li_5A782D743FB940649E6CB3E4BEA9B8B6"><b>절대 안 함.</b> 이 <span class="varname"> visitorID</span> cookie is intact, any amount of time can pass between eVar and event. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> 상태</span> </p> <p>(eVar만) </p> </td> 
   <td colname="col2"> <p>eVar 상태를 정의합니다. </p> <p><b></b> 비활성화됨</span>:eVar를 비활성화합니다. 전환 변수 목록에서 eVar를 제거합니다. </p> <p> <b></b> 하위 관계 없음</span>:하위 관계로 eVar를 분류할 수 없습니다. </p> <p> <b>Basic Subrelations</b>: </span>Lets you break down an eVar by any report with full subrelations (for example, Products or Campaign). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> 재설정</span> </p> </td> 
   <td colname="col2"> <p>eVar에서 모든 기존 값을 재설정합니다. </p> <p>eVar의 용도를 다시 지정할 때 이 설정을 사용하여 새 보고서에 이전 값을 혼합합니다. 재설정해도 내역 데이터는 지워지지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> 머천다이징</span> </p> <p>(eVar만) </p> </td> 
   <td colname="col2"> <p>머천다이징 변수는 다음 두 구문 중 하나를 따를 수 있습니다. </p> <p> <b>Products Syntax</b>:</span> Associates the eVar value to a product. 참고: [제품 구문]을 선택한 경우 [머천다이징 바인딩 이벤트] 섹션이 비활성화되므로 선택하여 편집할 수 있습니다. 이 구문에는 [바인딩 이벤트]를 적용할 수 없습니다. </p> </p> <p> <b>Conversion Variable Syntax</b>:</span> Associates the eVar with a product only if a Binding Event occurs. 이 경우 바인딩 이벤트처럼 동작하는 이벤트를 선택합니다. </p> <p>알맞게 JavaScript 코드를 업데이트하지 않고 이 설정을 변경하면 데이터가 손실됩니다. <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/var_merchandising.html" format="http" scope="external">머천다이징 변수</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> 머천다이징 바인딩 이벤트</span> </p> <p>(eVar만) </p> </td> 
   <td colname="col2"> <p>머천다이징이 <span class="uicontrol">전환 변수 구문</span>으로 설정된 경우, 선택한 이벤트는 현재 eVar 값을 제품에 바인딩합니다. </p> <p>바인딩 이벤트를 사용하려면 <span class="uicontrol">할당을 최근으로</span> 설정합니다. <span class="uicontrol">할당이 원래 값</span>인 경우 첫 번째 eVar 제품 바인딩은 eVar가 만료될 때까지 유지됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>