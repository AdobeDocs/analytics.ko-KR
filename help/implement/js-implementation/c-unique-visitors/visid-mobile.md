---
description: 대부분의 모바일 장치는 브라우저 쿠키를 허용합니다. 하지만, 장치가 쿠키를 허용하지 않는 경우, 다른 방법을 사용하여 무선 장치를 고유하게 식별하게 됩니다.
keywords: Analytics 구현
seo-description: 대부분의 모바일 장치는 브라우저 쿠키를 허용합니다. 하지만, 장치가 쿠키를 허용하지 않는 경우, 다른 방법을 사용하여 무선 장치를 고유하게 식별하게 됩니다.
seo-title: 모바일 장치 식별
solution: Analytics
title: 모바일 장치 식별
topic: 개발자 및 구현
uuid: 22587 dd 1-cead -485 b-a 4 d 8-94 dfb 7 cd 9662
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# 모바일 장치 식별

대부분의 모바일 장치는 브라우저 쿠키를 허용합니다. 하지만, 장치가 쿠키를 허용하지 않는 경우, 다른 방법을 사용하여 무선 장치를 고유하게 식별하게 됩니다.

Adobe는 다수의 모바일 장치를 고유하게 식별하는 많은 HTTP [가입자 ID 헤더](../../../implement/js-implementation/c-unique-visitors/visid-mobile.md#section_60D6EAC0D16945A89DD5A7ADF3B8298D)를 확인해 왔습니다. 이러한 헤더에는 종종 장치 전화 번호(또는 번호에 우물 정자를 사용한 버전)나 다른 식별자가 포함됩니다. 현재 장치의 대부분에는 장치를 고유하게 식별하는 헤더가 하나 이상 있으며, 모든 Adobe 데이터 수집 서버는 방문자 ID 대신 자동으로 이러한 헤더를 사용합니다.

In a typical image request, a '1' in the path ( `/b/ss/rsid/1`) causes Adobe servers to return a gif image and to attempt to set a persistent [!UICONTROL visitor ID] cookie ( `AMCV_` or `s_vi`). 하지만, 장치가 HTTP 헤더를 기반으로 하는 모바일 장치로 인식되는 경우, '5'가 '1' 대신 전달되고, 이것은 wbmp 형식 이미지를 반환해야 하고, 인식된 무선 헤더(쿠키 아님) 목록을 사용하여 장치를 식별해야 함을 나타냅니다.

다음 표에는 경로에 이미지 반환 유형 값('1' 또는 '5')을 기반으로 사용된 ID 방법의 순서가 나열됩니다.

<table id="table_07B0E55D5DAA4552A5CBC6937D47A857"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 설정 </th> 
   <th colname="col2" class="entry"> ID 방법 순서 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <code> /1/</code> </td> 
   <td colname="col2"> <p>기본값: </p> 
    <ul id="ul_E37E9919658A492C92187BAA18D33AB6"> 
     <li id="li_1A9E39C7CFB24C68AA07C8E85D33A858">사용자 지정 방문자 ID </li> 
     <li id="li_0DC8D17828C848BEB614C6E47C090064">쿠키 </li> 
     <li id="li_52706792FAD14F459266E3A672F92EA1">가입자 ID 헤더 </li> 
     <li id="li_ECAD713D22314338BB5C92167DC0BB02"> IP 주소-사용자 에이전트-게이트웨이 IP 주소 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> /5/ /5.1/ /5.5/</code> </td> 
   <td colname="col2"> <p>장치가 무선 장치로 확인되었거나, <code>/5/</code>가 이미지 요청에서 수동으로 전송되었습니다. </p> 
    <ul id="ul_624BEDFA3E1243CF9B42081D8B8EFFFB"> 
     <li id="li_D65761D23B684DB59BC23E92C9098122">사용자 지정 방문자 ID </li> 
     <li id="li_ADBA806B74CA43EFA8612301E06106C6">가입자 ID 헤더 </li> 
     <li id="li_79DFD0DEAA1242C09A03E8134A40F799">쿠키 </li> 
     <li id="li_A462B9120FC6443480D62F37D456747E">IP 주소-사용자 에이전트-게이트웨이 IP 주소 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

수동 이미지 요청에서 '1' 또는 '5'를 전달할 수도 있지만, 이 코드는 상호 배타적이므로, 항상 '5'를 전달하면 쿠키가 지원될 때 쿠키가 사용되지 않습니다. 장치가 쿠키를 지원하는지 파악하고, 지원하는 경우 이미지에서 '5'가 아니라 '1'을 전달하는 자신만의 메커니즘을 통합할 수 있습니다. 이런 상황에서 정확도 개선은 쿠키를 지원하는 모바일 장치의 수로 제한됩니다.

## 구독자 ID 헤더 {#section_60D6EAC0D16945A89DD5A7ADF3B8298D}

구독자 ID 방식은 일반적으로 사용자 식별에 있어 쿠키보다 안정적입니다. 쿠키는 삭제 문제, 승인 문제, 게이트웨이 쿠키 관리 문제가 있기 때문입니다.

모바일 방문자가 사용하는 통신사에 대한 허용 목록에 추가되면 방문자 식별의 변경 사항이 개선됩니다. 통신사의 방문자 ID에 액세스하려면 통신사에 연락하여 도메인을 허용 목록에 추가하십시오. 통신사 허용 목록에 등록된 경우 액세스할 수 없었던 가입자 ID 헤더에도 액세스할 수 있습니다.

다음의 헤더 목록은 무선 장치를 식별하는 데 사용됩니다. 헤더 처리 알고리즘은 다음과 같습니다.

1. HTTP 헤더 키를 추출합니다("X-Up-Calling-Line-ID" 등의 헤더 이름).
1. 알파벳(A-Z 및 a-z)이 아닌 모든 문자를 잘라냅니다.
1. 헤더 키를 소문자로 변환합니다.
1. 다음 표의 헤더에 대해 키의 끝을 비교하여 일치하는 것을 찾습니다.

| 헤더 | 유형 | 예 |
|---|---|---|
| callinglineid | ID | X-Up-Calling-Line-ID: 8613802423312 |
| subno | ID | x-up-subno: swm_10448371100_vmag.mycingular.net |
| clientid | ID | ClientID: eGtUpsqEO19zVHmbOkgaPVI-@sprintpcs.com |
| uid | ID | x-jphone-uid: a2V4Uh21XQH9ECNN |
| clid | ID | X-Hts_clid: 595961714786 |
| deviceid | ID | rim-device-id: 200522ae |
| forwardedfor | ID 또는 IP 주소 | X-Forwarded-For: 127.0.0.1 |
| msisdn | ID 또는 IP 주소 | X-Wap-msisdn: 8032618185 |
| clientip | IP 주소 | Client-ip: 10.9.41.2 |
| wapipaddr | IP 주소 | X-WAPIPADDR: 10.48.213.162 |
| huaweinasip | IP 주소 | x-huawei-NASIP: 211.139.172.70 |
| userip | IP 주소 | UserIP: 70.214.81.241 |
| ipaddress | IP 주소 | X-Nokia-ipaddress: 212.97.227.125 |
| subscriberinfo | IP 주소 | X-SUBSCRIBER-INFO: IP=10.103.132.128 |

예를 들어 "callinglineid"는 "X-Up-Calling-Line-ID" 및 "nokia-callinglineid"와 일치합니다. 헤더에서 기대할 내용은 헤더 유형을 통해 알 수 있습니다. 헤더 우선 순위는 다음과 같습니다("callinglineid" 헤더가 있을 경우, "subno" 대신 "callinglineid"가 사용됨).

You can use [다이내믹 변수](../../../implement/js-implementation/c-variables/dynvars-overview.md#concept_B016789733A94070A9EAB209EEC05262)를 사용하여 헤더에서 특정 값을 추출할 수 있습니다.
