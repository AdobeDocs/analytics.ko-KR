---
description: HTTP 요청 및 응답 헤더는 AppMeasurement에서 모으는 데이터 외에 추가로 데이터를 모으려고 할 때 사용됩니다. 이 섹션에서는 데이터 수집 중 사용되는 헤더에 대해 설명합니다.
keywords: Analytics 구현
seo-description: HTTP 요청 및 응답 헤더는 AppMeasurement에서 모으는 데이터 외에 추가로 데이터를 모으려고 할 때 사용됩니다. 이 섹션에서는 데이터 수집 중 사용되는 헤더에 대해 설명합니다.
seo-title: 데이터 수집 HTTP 헤더
solution: Analytics
title: 데이터 수집 HTTP 헤더
topic: 개발자 및 구현
uuid: 3325 E 13 C-B 300-46 E 4-A 592-3 A 83 ED 59718 B
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 데이터 수집 HTTP 헤더

HTTP 요청 및 응답 헤더는 AppMeasurement에서 모으는 데이터 외에 추가로 데이터를 모으려고 할 때 사용됩니다. 이 섹션에서는 데이터 수집 중 사용되는 헤더에 대해 설명합니다.

## HTTP 요청 헤더 {#section_C1DE3416CCC241A898155C915A01A0FC}

<table id="table_84D1F4B54ABE4423A2EBE840C49D3876"> 
 <tbody> 
  <tr> 
   <td> <b>헤더</b> </td> 
   <td> <b>사용</b> </td> 
  </tr> 
  <tr> 
   <td> Cookie </td> 
   <td> <p>이전에 Adobe의 데이터 수집 서버에서 만든 읽기 쿠키. </p> <p> 2014년에, Adobe 서버는 Adobe에서 설정한 것을 제외하고 서버 호출이 있는 모든 쿠키를 버립니다. Adobe 쿠키의 전체 목록은 <a href="https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/" format="https" scope="external">Experience Cloud에 사용된 쿠키</a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td> User-Agent </td> 
   <td> 브라우저, 운영 체제 및 모바일 장치 감지에 사용됨 </td> 
  </tr> 
  <tr> 
   <td> X-Device-User-Agent </td> 
   <td> OperaMini와 같은 일부 브라우저에 대해 올바른 브라우저, 운영 체제 및 모바일 장치 감지를 위해 User-Agent의 대체 헤더로 사용됨 </td> 
  </tr> 
  <tr> 
   <td> X-Original-User-Agent </td> 
   <td> OperaMini와 같은 일부 브라우저에 대해 올바른 브라우저, 운영 체제 및 모바일 장치 감지를 위해 User-Agent의 대체 헤더로 사용됨 </td> 
  </tr> 
  <tr> 
   <td> X-OperaMini-Phone-UA </td> 
   <td> OperaMini와 같은 일부 브라우저에 대해 올바른 브라우저, 운영 체제 및 모바일 장치 감지를 위해 User-Agent의 대체 헤더로 사용됨 </td> 
  </tr> 
  <tr> 
   <td> X-Skyfire-Phone </td> 
   <td> OperaMini와 같은 일부 브라우저에 대해 올바른 브라우저, 운영 체제 및 모바일 장치 감지를 위해 User-Agent의 대체 헤더로 사용됨 </td> 
  </tr> 
  <tr> 
   <td> X-Bolt-Phone-UA </td> 
   <td> OperaMini와 같은 일부 브라우저에 대해 올바른 브라우저, 운영 체제 및 모바일 장치 감지를 위해 User-Agent의 대체 헤더로 사용됨 </td> 
  </tr> 
  <tr> 
   <td> UA-OS </td> 
   <td> 대체 헤더가 운영 체제를 식별할 때 사용됨 </td> 
  </tr> 
  <tr> 
   <td> UA-Pixels </td> 
   <td> 클라이언트 화면의 화면 해상도에 대한 대체 소스로 사용됨 </td> 
  </tr> 
  <tr> 
   <td> UA-Color </td> 
   <td> 클라이언트 화면의 색상 깊이에 대한 대체 소스로 사용됨 </td> 
  </tr> 
  <tr> 
   <td> X-moz </td> 
   <td> 데이터 수집 요청이 웹 페이지의 사전 반입의 일부로서 수행되었음을 감지 </td> 
  </tr> 
  <tr> 
   <td> X-Purpose </td> 
   <td> 브라우저가 웹 페이지 미디어를 보여주고 있을 때 데이터 수집 요청이 수행되었음을 감지 </td> 
  </tr> 
  <tr> 
   <td> Accept </td> 
   <td> GIF나 WBMP 이미지를 다시 보내야 할 것인지를 알 수 있도록, 브라우저가 지원하는 이미지 형식을 식별하는 데 사용됨 </td> 
  </tr> 
  <tr> 
   <td> Referrer </td> 
   <td> 데이터 수집 요청이 쿼리 문자열에서 전달되지 않았거나 쿼리 문자열에 있는 값과 다를 경우, 데이터 수집 요청을 수행한 페이지 URL에 대한 정보를 가져오기 위한 대비책으로 사용됨 </td> 
  </tr> 
  <tr> 
   <td> X-Forwarded-For </td> 
   <td> 데이터 수집 요청을 수행한 클라이언트의 올바른 IP 주소를 찾는 데 사용되며, IP 주소는 지리적 구역, 모바일 통신사 및 기타 보고서를 생성하는 데 사용됨 </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>동적 변수를 사용하는 구현에는 위에 나열되지 않은 다른 HTTP 요청 헤더에서 읽는 옵션이 있습니다.

## HTTP 응답 헤더 {#section_A9C7035198C84037A21A8033CC408F0E}

| **헤더** | **사용** |
|---|---|
| Access-Control-Allow-Origin | 다른 서버들에 대한 스타일 데이터 수집 요청을 공유하는 원래 리소스 공유에 대한 지원을 활성화하는 데 사용됨 |
| Expires | 브라우저 캐싱 제어 |
| Last-Modified | 브라우저 캐싱 제어 |
| Cache-Control | 브라우저 캐싱 제어 |
| Pragma | 브라우저 캐싱 제어 |
| ETag | 브라우저 캐싱 제어 |
| Vary | 브라우저 캐싱 제어 |
| P3P | 데이터 수집 요청을 위한 기본 또는 사용자 지정 P3P 정책 제공 |
| Status | 컨텐츠 요청이 없는 경우 "SUCCESS" 또는 "FAILURE" 상태를 포함함. 요청이 컨텐츠를 반환하지 않도록 지정할 때만 사용됨. |
| Reason | 컨텐츠 요청이 없는 실패 상태에 대한 이유를 포함합니다. 요청이 컨텐츠를 반환하지 않도록 지정할 때만 사용됨. |
| Location | 클라이언트가 데이터 수집 요청을 다른 URL로 보내도록 리디렉션하는 데 사용됨. 일례로, 방문자 ID 쿠키를 설정하는 기능을 감지하는 Adobe의 쿠키 핸드셰이크가 있음. |
| Content-Type | 다시 클라이언트로 보내지는 컨텐츠 유형 지정(GIF, 텍스트, Javascript 등) |
| Content-Length | 다시 클라이언트로 보내지는 컨텐츠 크기 지정 |

>[!NOTE]
>
>내부 상태 모니터링에 대한 응답에서 다른 HTTP 헤더를 설정할 수 있습니다. 이러한 헤더 중 일부는 브라우저로 반환될 수 있지만, 브라우저가 이 헤더를 받을 필요는 없습니다.
