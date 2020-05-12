---
description: Adobe에서는 쿠키를 사용하여 고유한 브라우저/장치를 추적합니다.
keywords: Analytics Implementation
subtopic: Visitors
title: 고유 방문자 수 식별
topic: Developer and implementation
uuid: ed4dee75-ecfb-4715-8122-461983c7dd8f
translation-type: ht
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# 고유 방문자 수 식별

Adobe에서는 쿠키를 사용하여 고유한 브라우저/장치를 추적합니다.

## Analytics 방문자 ID 순서 {#section_DE1DC9FC9B6D4388995B70E35B8BCDDF}

Adobe Analytics에서는 방문자를 식별하는 메커니즘을 몇 가지 제공합니다. 다음 표에는 Analytics에서 방문자를 식별할 수 있는 다양한 방법이 나열되어 있습니다(선호도 순).

| 사용된 순서 | 쿼리 매개 변수(컬렉션 방법) | 존재할 때 |
|---|---|---|
| 1 | vid (s.visitorID) | s.visitorID가 설정되어 있습니다. |
| 2 | aid (s_vi 쿠키) | 방문자는 방문자 ID 서비스를 배포하기 전에 기존 s_vi 쿠키가 있었거나 구성된 방문자 ID 유예 기간이 있습니다. |
| 3 | mid(Experience Cloud 방문자 ID 서비스에 의해 설정된 AMCV_ 쿠키) | 방문자의 브라우저가 쿠키를 승인합니다(자사). |
| 4 | fid(폴백 쿠키) | 방문자의 브라우저가 쿠키를 승인합니다(자사). |
| 5 | IP 주소, 사용자 에이전트, 게이트웨이 IP 주소 | 방문자의 브라우저가 쿠키를 승인하지 않습니다. |

많은 시나리오에서 2개나 3개의 서로 다른 ID가 같은 호출에 있는 경우를 볼 수도 있습니다. 하지만 Analytics에서는 해당 목록에 있는 첫 번째 ID를 공식 방문자 ID로 사용합니다. 예를 들어, 사용자 지정 방문자 ID(&quot;vid&quot; 쿼리 매개 변수에 포함됨)를 설정하는 경우, 이 ID는 동일한 히트에 있을 수 있는 다른 ID보다 먼저 사용됩니다.

>[!NOTE] 각각의 Analytics 방문자 ID는 Adobe 서버의 방문자 프로필과 연결됩니다. 방문자 프로필은 모든 방문자 ID 쿠키 만료와 관계없이 비활성 기간 13달 후 삭제됩니다.

## 사용자 지정 방문자 ID

사용자 지정 방법을 구현하여 s.visitorID 변수를 설정함으로써 방문자를 식별할 수 있습니다.

방문자를 식별하는 고유한 방법이 있으면 사이트에서 사용자 지정 방문자 ID를 사용할 수 있습니다. 사용자가 사용자 이름과 암호를 사용하여 웹 사이트에 로그인할 때 생성되는 ID가 그 예입니다.

사용자의 [!UICONTROL 방문자 ID]를 추출하고 관리할 수 있을 경우, 다음 방법을 사용하여 ID를 설정할 수 있습니다.

| 메서드 | 설명 |
|---|---|
| [s.visitorID](../implement/vars/config-vars/visitorid.md) 변수 | 브라우저에서 JavaScript를 사용하거나, 다른 AppMeasurement 라이브러리를 사용 중일 경우, 데이터 수집 변수에 방문자 ID를 설정할 수 있습니다. |
| 이미지 요청 시 쿼리 문자열 매개 변수 | 이 기능을 통해 [!UICONTROL 방문자 ID]를 하드 코딩된 이미지 요청에서 [!UICONTROL vid 쿼리 문자열] 매개 변수를 통해 Adobe로 전달할 수 있습니다. |
| 데이터 삽입 API | JavaScript를 허용하지 않는 무선 프로토콜을 사용하는 장치에서는 `<visitorid/>` XML 요소가 들어 있는 XML 게시물을 해당 서버로부터 Adobe 수집 서버로 보낼 수 있습니다. |
| URL 다시 쓰기 및 VISTA | 일부 배포 아키텍처에서는 쿠키를 설정할 수 없는 경우 세션 상태를 유지할 수 있도록 URL 다시 쓰기를 지원합니다. 이와 같은 경우, Adobe 엔지니어링 서비스에서는 페이지의 URL에서 세션 값을 찾는 [!DNL VISTA] 규칙을 구현한 다음 형식을 지정하여 [!UICONTROL visid] 값에 삽입할 수 있습니다. |
>[!CAUTION]
>**사용자 지정 방문자 ID는 세분화/고유해야 함&#x200B;**: 사용자 지정 방문자 ID가 잘못 구현되면 데이터가 올바르지 않고 보고 성능이 저하될 수 있습니다. 사용자 지정 방문자 ID가 고유하지 않거나 세분화되지 않거나 문자열 &quot;NULL&quot; 또는 &quot;0&quot;과 같은 일반적인 기본값으로 잘못 설정된 경우 여러 방문자의 히트가 Adobe Analytics에서 단일 방문자로 표시됩니다. 이 경우 방문자 수가 너무 적고 세그먼트가 해당 방문자에 대해 제대로 작동하지 않는 올바르지 않은 데이터가 발생합니다. 세분화되지 않은 사용자 지정 방문자 ID로 인해 데이터가 Analytics 보고 클러스터의 여러 노드에 제대로 전파되지 않습니다. 이 경우 한 노드가 오버로드되어 보고서 요청을 적시에 처리할 수 없습니다. 결과적으로 보고서 세트에 대한 모든 보고가 실패합니다.<br>Analytics에서 종종 균형이 맞지 않는 데이터 몇 달치를 한 번에 처리하기도 하므로 잘못 구현된 사용자 지정 방문자 ID가 보고 성능에 곧바로 영향을 주지 않을 수 있습니다. 하지만 시간이 지나면서 Analytics에서 영향을 받는 보고서 세트에 대한 처리를 비활성화해야 할 정도로 잘못 구현된 사용자 지정 방문자 ID 값이 문제가 될 수 있습니다.</br><br>구현자는 단일 사용자 지정 방문자 ID 값이 보고서 세트 트래픽의 1% 이상을 처리할 수 없다는 지침을 따라야 합니다. 1% 지침은 대부분의 보고서 세트에 충분하지만, 보고 성능에 영향을 줄 수 있는 실제 제한은 매우 큰 보고서 세트의 경우 1%보다 작을 수 있습니다.</br>

## Analytics 방문자 ID

사용자가 사이트를 방문하면, Adobe 웹 서버에서는 브라우저에 대한 HTTP 응답에 영구적 쿠키를 포함하여 영구적 쿠키를 설정합니다. 이 쿠키는 지정된 데이터 수집 도메인에서 설정됩니다.

Adobe 데이터 수집 서버로 요청이 전송되면 헤더에 방문자 ID 쿠키(`s_vi`)가 있는지 확인이 이루어집니다. 이 쿠키가 요청에 있으면 방문자 식별에 사용됩니다. 쿠키가 요청에 없으면 서버가 고유한 방문자 ID를 생성하고 이것을 HTTP 응답 헤더의 쿠키로 설정하여 다시 요청과 함께 전송합니다. 쿠키는 브라우저에 저장되었다가 다음에 사이트를 방문할 때 데이터 수집 서버로 전송되어 방문 중에 방문자를 식별할 수 있게 합니다.

### 타사 쿠키 및 CNAME 레코드 {#section_61BA46E131004BB2B75929C1E1C93139}

Apple Safari와 같은 일부 브라우저는 현재 웹 사이트의 도메인과 일치하지 않는 도메인의 HTTP 헤더에 설정된 쿠키를 더 이상 보관하지 않습니다(타사 컨텍스트에 사용된 쿠키이거나 타사 쿠키). 예를 들어 `mysite.com`을 방문 중이고 데이터 수집 서버가 `mysite.omtrdc.net`인 경우 브라우저가 `mysite.omtrdc.net`의 HTTP 헤더에서 반환되는 쿠키를 거부할 수 있습니다.

이를 방지하기 위해 많은 고객들이 [자사 쿠키 구현](https://docs.adobe.com/content/help/ko-KR/core-services/interface/ec-cookies/cookies-first-party.html)의 일부로서 데이터 수집 서버에 대한 CNAME 레코드를 구현했습니다. CNAME 레코드가 고객 도메인을 데이터 수집 서버로 호스트 이름을 매핑하도록 구성된 경우(예: `metrics.mysite.com`을 `mysite.omtrdc.net`으로 매핑) 데이터 수집 도메인이 웹 사이트 도메인과 일치하므로 방문자 ID 쿠키가 저장됩니다. 이는 방문자 ID 쿠키가 저장될 가능성을 높이긴 하지만 CNAME 레코드를 구성하고 데이터 수집 서버에 대한 SSL 인증서를 유지해야 하므로 약간의 오버헤드를 유발합니다.

### 모바일 장치의 쿠키 {#section_7D05AE259E024F73A95C48BD1E419851}

쿠키를 사용하여 모바일 장치를 추적하는 경우 몇 가지 설정을 사용하여 측정 방식을 수정할 수 있습니다. 쿠키의 기본 수명은 5년이지만 CL 쿼리 매개 변수(`s.cookieLifetime`)를 사용하여 이 기본값을 바꿀 수 있습니다. cname 구현을 위해 쿠키 위치를 설정하려면 CDP 쿼리 문자열 `s.cookieDomainPeriods`를 사용하십시오. 값이 지정되지 않은 경우 기본값은 2입니다. 기본 위치는 domain.com입니다. CNAME을 사용하지 않는 구현의 경우 방문자 ID 쿠키 위치는 207.net 도메인입니다.

## ID 서비스

ID 서비스는 레거시 Analytics 방문자 ID 메커니즘을 대체하며, 하트비트 비디오 측정, Target용 Analytics 및 향후 Experience Cloud 핵심 서비스 및 통합에 필요합니다.

이 서비스에 대한 제품 설명서가 필요하면 [Identity Service](https://docs.adobe.com/content/help/ko-KR/id-service/using/home.html)를 참조하십시오.

## 모바일 장치 식별

대부분의 모바일 장치는 브라우저 쿠키를 허용합니다. 하지만, 장치가 쿠키를 허용하지 않는 경우, 다른 방법을 사용하여 무선 장치를 고유하게 식별하게 됩니다.

Adobe는 다수의 모바일 장치를 고유하게 식별하는 많은 HTTP 가입자 ID 헤더를 확인해 왔습니다. 이러한 헤더에는 종종 장치 전화 번호(또는 번호에 우물 정자를 사용한 버전)나 다른 식별자가 포함됩니다. 현재 장치의 대부분에는 장치를 고유하게 식별하는 헤더가 하나 이상 있으며, 모든 Adobe 데이터 수집 서버는 방문자 ID 대신 자동으로 이러한 헤더를 사용합니다.

전형적인 이미지 요청에서 경로(`/b/ss/rsid/1`)의 &#39;1&#39;은 Adobe 서버가 gif 이미지를 반환하고 영구 [!UICONTROL 방문자 ID] 쿠키(`AMCV_` 또는 `s_vi`)의 설정을 시도하도록 합니다. 하지만, 장치가 HTTP 헤더를 기반으로 하는 모바일 장치로 인식되는 경우, &#39;5&#39;가 &#39;1&#39; 대신 전달되고, 이것은 wbmp 형식 이미지를 반환해야 하고, 인식된 무선 헤더(쿠키 아님) 목록을 사용하여 장치를 식별해야 함을 나타냅니다.

다음 표에는 경로에 이미지 반환 유형 값(&#39;1&#39; 또는 &#39;5&#39;)을 기반으로 사용된 ID 방법의 순서가 나열됩니다.

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
   <td colname="col2"> <p>장치가 무선 장치로 확인되었거나, <code> /5/</code>가 이미지 요청에서 수동으로 전송되었습니다. </p> 
    <ul id="ul_624BEDFA3E1243CF9B42081D8B8EFFFB"> 
     <li id="li_D65761D23B684DB59BC23E92C9098122">사용자 지정 방문자 ID </li> 
     <li id="li_ADBA806B74CA43EFA8612301E06106C6">가입자 ID 헤더 </li> 
     <li id="li_79DFD0DEAA1242C09A03E8134A40F799">쿠키 </li> 
     <li id="li_A462B9120FC6443480D62F37D456747E">IP 주소-사용자 에이전트-게이트웨이 IP 주소 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

수동 이미지 요청에서 &#39;1&#39; 또는 &#39;5&#39;를 전달할 수도 있지만, 이 코드는 상호 배타적이므로, 항상 &#39;5&#39;를 전달하면 쿠키가 지원될 때 쿠키가 사용되지 않습니다. 장치가 쿠키를 지원하는지 파악하고, 지원하는 경우 이미지에서 &#39;5&#39;가 아니라 &#39;1&#39;을 전달하는 자신만의 메커니즘을 통합할 수 있습니다. 이런 상황에서 정확도 개선은 쿠키를 지원하는 모바일 장치의 수로 제한됩니다.

### 구독자 ID 헤더 {#section_60D6EAC0D16945A89DD5A7ADF3B8298D}

구독자 ID 방식은 일반적으로 사용자 식별에 있어 쿠키보다 안정적입니다. 쿠키는 삭제 문제, 승인 문제, 게이트웨이 쿠키 관리 문제가 있기 때문입니다.

모바일 방문자가 사용하는 통신사에 대한 허용 목록에 추가되면 방문자 식별의 변경 사항이 개선됩니다. 통신사의 방문자 ID에 액세스하려면 통신사에 연락하여 도메인을 허용 목록에 추가하십시오. 통신사 허용 목록에 등록된 경우 액세스할 수 없었던 가입자 ID 헤더에도 액세스할 수 있습니다.

다음의 헤더 목록은 무선 장치를 식별하는 데 사용됩니다. 헤더 처리 알고리즘은 다음과 같습니다.

1. HTTP 헤더 키를 추출합니다(&quot;X-Up-Calling-Line-ID&quot; 등의 헤더 이름).
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

예를 들어 &quot;callinglineid&quot;는 &quot;X-Up-Calling-Line-ID&quot; 및 &quot;nokia-callinglineid&quot;와 일치합니다. 헤더에서 기대할 내용은 헤더 유형을 통해 알 수 있습니다. 헤더 우선 순위는 다음과 같습니다(&quot;callinglineid&quot; 헤더가 있을 경우, &quot;subno&quot; 대신 &quot;callinglineid&quot;가 사용됨).

 [다이내믹 변수](../implement/vars/page-vars/dynamic-variables.md)를 사용하여 헤더에서 특정 값을 추출할 수 있습니다.

## 대체 ID 방법

다른 방문자 ID 방법이 실패할 경우, Adobe에서는 대체 쿠키를 설정하거나 IP 주소와 사용자 에이전트를 결합하여 방문자를 식별합니다.

### 방문자 식별 대비책 {#section_2BA15E4FA6034C3EBF43859406343EB6}

2013년 1월에 발표된 JavaScript 1.x 및 JavaScript H.25.3용 AppMeasurement에는 Adobe의 데이터 수집 서버에서 설정한 쿠키(`s_vi`라고 함)를 차단하는 브라우저를 사용하는 방문자를 위한 새로운 방문자 식별 대비책이 포함되어 있습니다. 이전에는 쿠키를 설정할 수 없을 경우, 데이터를 수집하는 동안 IP 주소와 사용자 에이전트 문자열의 조합을 사용하여 방문자를 식별했습니다.

이 업데이트를 사용하면 표준 `s_vi` 쿠키를 사용할 수 없을 경우, 무작위로 생성된 고유 ID를 사용하는 대체 쿠키가 웹 사이트의 도메인에 만들어집니다. `s_fid`라는 이 쿠키는 2년 동안 사용할 수 있으며 앞으로 식별 대비책으로 사용됩니다. 기본 쿠키(`AMCV_` 또는 `s_vi`)를 설정할 수 없는 상황에서는 이 변경 사항으로 인해 방문 및 방문자 수의 정확도가 높아집니다.

총 방문 횟수에는 `s_vi` 쿠키나 대비책을 사용하여 식별된 모든 사용자가 포함됩니다.

### IP 주소, 사용자 에이전트, 게이트웨이 IP 주소 {#section_104819D74C594ECE879144FCC5DEF4BF}

라는 사용자 지정 코드에서 변수를 찾습니다. `AMCV_` 또는 `s_vi` 및 `s_fid` 쿠키를 설정할 수 없는 경우에는 IP 주소와 사용자 에이전트의 조합을 사용하여 방문자를 식별합니다.
