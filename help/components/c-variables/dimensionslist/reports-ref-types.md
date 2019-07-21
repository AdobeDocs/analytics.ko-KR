---
description: 방문할 때마다 방문자의 참조 사이트를 추적 및 기록하면 방문자가 사이트를 어떻게 발견해서 방문했는지 알 수 있습니다.
seo-description: 방문할 때마다 방문자의 참조 사이트를 추적 및 기록하면 방문자가 사이트를 어떻게 발견해서 방문했는지 알 수 있습니다.
seo-title: 레퍼러 유형
solution: Analytics
title: 레퍼러 유형
topic: 보고서
uuid: 7 f 63 d 327-D 223-4537-A 722-4780 AAE 05 C 2 B
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 참조 유형

방문할 때마다 방문자의 참조 사이트를 추적 및 기록하면 방문자가 사이트를 어떻게 발견해서 방문했는지 알 수 있습니다.

아래 목록은 다양한 유형의 레퍼러를 정의합니다.

**다른 웹 사이트**: 레퍼러는 방문자가 다른 웹 사이트(사이트의 일부로 정의되지 않은) 페이지에 있는 링크를 클릭하고 사용자 웹 사이트에 도달할 때 기록됩니다.

**검색 엔진**: 검색 엔진 레퍼러는 방문자가 검색 엔진을 사용하여 사이트에 액세스할 때 기록됩니다. 참조 값은 Adobe에서 검색 엔진으로 간주되어야 하며 검색 엔진으로 간주되지 않는 하위 도메인이 될 수 없습니다(예: [!DNL mail.yahoo.com]은 이메일에 사용되므로 검색 엔진이 아님).

**[!UICONTROL 소셜 네트워크]**: 참조 값은 Adobe에서 소셜 네트워크로 간주되어야 합니다. [소셜 네트워크 목록](https://helpx.adobe.com/analytics/kb/list-social-networks.html)을 참조하십시오.

**이메일**: 참조 도메인은 방문자가 프로토콜이 [!DNL imap://] 들어 있는 이메일 메시지 링크를 클릭하거나 사이트에 도달하면 이메일 참조 [!DNL mail://] 도메인으로 간주됩니다. 예를 들어 [!DNL https://mail.yahoo.com]에서 오는 모든 것은 프로토콜이 [!DNL https://]://이기 때문에 이메일 레퍼러로 계산되지 않습니다. Outlook의 이메일은 입력/책갈피 표시 행에 보고되며 도메인이 알려진 검색 엔진인 HTTP 프로토콜을 가진 레퍼러는 검색 엔진 행에 보고됩니다.

**입력/책갈피 표시 레퍼러는 방문자가 사용자 사이트의 URL을 브라우저에 직접 입력할 때 또는 책갈피를 선택하여 사이트에 액세스하는 경우 기록됩니다.** 모바일 장치는 방문의 첫 번째 히트에 참조가 없는 경우 *`typed/bookmarked`* 를 참조 유형으로 보고합니다.

**[!UICONTROL 사이트 내부]**: 이러한 항목은 내부 URL 필터에서 태그가 지정된 항목입니다. These items are not counted as *`referrer instances`* but can be seen when reporting on other metrics.

## 인터페이스별 레퍼러 유형 {#section_4D8CE5E111DD48FBBDCF9B5A1F16E92E}

<table id="table_EC7423532C7E44DE97B7FC0321585A2B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> Marketing Reports &amp; Analytics (SiteCatalyst) </th> 
   <th colname="col3" class="entry"> Ad hoc analytics </th> 
   <th colname="col4" class="entry"> Data Warehouse </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 보고된 레퍼러 유형 </td> 
   <td colname="col2"> 
    <ul id="ul_EFC8E81EC6DF4CC2AC0E290244FD5859"> 
     <li id="li_686FCAEB04054B9F8A7D2434E8C49F04">기타 웹 사이트 </li> 
     <li id="li_C232868230AA4A54958B524F3D8FDA35"> 검색 엔진 </li> 
     <li id="li_A89BFD0468F74ED7822F64BE4A7332AE"> 소셜 </li> 
     <li id="li_C824E6F7F6E748DD827A95B105ADBADD"> 입력/책갈피 표시 </li> 
    </ul> <p> 이 보고서에는 사전 정의된 지표인 인스턴스와 고유 방문자, 이 두 개만 표시됩니다. </p> </td> 
   <td colname="col3"> 
    <ul id="ul_FD81EB3C1BD949A39C5A9E9688D25271"> 
     <li id="li_6099E7E03F3843D484808258A332BBE9">기타 웹 사이트 </li> 
     <li id="li_5AABC02DA7964D578BF8404DA819245D"> 검색 엔진 </li> 
     <li id="li_B18907AC7FA1429A893B57634EB7DC6F"> 소셜 </li> 
     <li id="li_7674B67897994E1FA99BCD9B604BCB6E"> 입력/책갈피 표시 </li> 
    </ul> </td> 
   <td colname="col4"> 
    <ul id="ul_C37ADBEC31D04295BF5CDEA25DB5191A"> 
     <li id="li_81A642C96C674669BA00B2DACA534B8A">기타 웹 사이트 </li> 
     <li id="li_29B9DA9F2AAD46A69886D34D5E6E43D4"> 검색 엔진 </li> 
     <li id="li_E381EEF111F248F99EE39600D616B7C2"> 소셜 </li> 
     <li id="li_596377F4D3C248BEA5191EE2985A2B13"> 입력/책갈피 표시 </li> 
     <li id="li_A7A72D3D6B9A4CCFB43EDA77ABFDEDBC"> 사용자 사이트 내 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 내용 {#section_B83A3571D64E4E7792712FAF740D7955}

* 레퍼러, 레퍼러 유형 및 참조 도메인은 방문의 첫 번째 히트에서, 또는 레퍼러가 외부인 방문 동안(예: 방문자가 사이트를 떠나고, 검색 엔진을 사용한 다음 첫 번째 방문이 만료되기 전에 사이트로 돌아오는 경우) 설정됩니다. 이 값들은 동시에 설정되며, 방문 전체에서 지속됩니다.
* 이 보고서에 모든 레퍼러 유형이 나열되는 것은 아닙니다. 이것은 사이트 전체 방문이 이 보고서의 방문과 일치하지 않음을 의미합니다.

## 보고서 내역 {#section_6C0FCEA9DAF04D97BA056E153B7E4628}

| 날짜 | 변경 |
|---|---|
| 2014/1/16 | Data Warehouse를 업데이트하여 Marketing Reports &amp; Analytics에서 사용하는 논리와 일치시켰습니다. 이 날짜 전에는 레퍼러 유형이 방문 전체에서 지속되지 않았습니다. |

