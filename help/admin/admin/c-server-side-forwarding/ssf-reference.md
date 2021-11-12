---
description: 서버 측 전달 호출의 구성 변수, HTTP 헤더 및 데이터 신호에 대한 종합 목록 및 설명.
title: 서버 측 전달 데이터 및 코드 참조
uuid: 3eb3ea0f-a530-448d-bba5-6408b2490dc8
exl-id: 6ab7bbb6-0709-427b-b9fa-a179dbe55fc9
source-git-commit: 4f29245a80e54f3fbc5a830075d066b31d23c628
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 92%

---

# 서버 측 전달 데이터 및 코드 참조

서버 측 전달 호출의 구성 변수, HTTP 헤더 및 데이터 신호에 대한 종합 목록 및 설명.

## 구성 변수 {#section_AD402B5EB9B24BF3B2039DA80FCA901E}

`d_*`라는 접두사가 있는 매개 변수는 DCS([데이터 수집 서버](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/system-components/components-data-collection.html?lang=ko-KR))에서 사용되는 특별한 시스템 수준의 키-값 쌍을 식별합니다. [DCS API 호출에 대한 지원되는 속성](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-keys.html?lang=ko-KR)을 참조하십시오.

| 매개 변수 | 설명 |
|--- |--- |
| `d_rs` | (기존/추적 서버 기반 서버 측 전달을 사용하여 세트 가져오기) <br>히트와 함께 Analytics에 전달된 보고서 세트로 설정합니다. |
| `d_dst_filter` | (보고서 세트 기반 서버 측 전달을 사용하여 세트 가져오기) <br>히트와 함께 Analytics에 전달된 보고서 세트 ID로 설정합니다. |
| `d_dst` | Analytics에 대한 요청에서 대상에 대한 컨텐츠가 클라이언트로 다시 전송될 것으로 예상하는 경우 `d_dst=1`로 설정합니다.<br> |
| `d_mid` | Analytics에 전달된 Experience Cloud ID입니다. |

## HTTP 헤더 {#section_0549705E76004F9585224AEF872066C0}

이 헤더는 HTTP 호출에서 데이터 및 응답 요청과 같은 정보를 포함하는 필드입니다.

| HTTP 헤더 | 설명 | Audience Manager에 의해 허용되는 h_key |
| --- | --- | --- |
| 호스트 | Analytics 호스트 구성 파일에 지정된 클라이언트의 특정 데이터 수집 호스트 이름으로 설정됩니다. 이 이름은   `host name .demdex.net`으로 나타납니다.  [Demdex 도메인에 대한 호출 이해](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html?lang=ko-KR)를 참조 하십시오. | `h_host` |
| User-Agent | Analytics에 전달된 User-Agent 헤더로 설정합니다. | `h_user-agent` |
| Accept-Language | Analytics에 전달된 `Accept-Language` 헤더로 설정합니다. | `h_accept-language` |
| Referer | Analytics로 전달되거나 Analytics로 전달된 `Referer` 헤더에서 수집한 페이지 URL로 설정합니다. | `h_referer` |
| 레퍼러 | Analytics로 전달되거나 Analytics로 전달된 `Referrer` 헤더에서 수집한 페이지 URL로 설정합니다. | `h_referrer` |

또한 `h_ip` DCS로 요청을 보내는 호스트의 IP에서 신호가 생성됩니다.

## 고객 정의 신호 {#section_8F8C39E87BDE48BAA59E25CB7E86215D}

`c_` 접두사가 있는 매개 변수는 고객 정의 변수를 식별합니다. [DCS API 호출에 대한 지원되는 속성](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-keys.html)을 참조하십시오.

| 신호 | 설명 |
| --- |--- |
| `c_browserWidth`  및 `c_browserHeight` | 브라우저 창 너비와 높이. |
| `c_campaign` | 설정 기준 `s.campaign`. |
| `c_channel` | 설정 기준 `s.channel`. |
| `c_clientDateTime` | 형식이 `dd/mm/yyy hh:mm:ss  W TZ` . `TZ`는 분 단위이며 `Date.getTimezoneOffset` 메소드의 반환과 일치합니다. |
| `c_colorDepth` | 16비트 또는 32비트 색상으로 지정됩니다. |
| `c_connectionType` | 연결 유형을 지정합니다. 옵션은 다음과 같습니다.<ul><li>modem</li><li>lan</li></ul> |
| `c_contextData.*` | 예:<ul><li>AppMeasurement: `s.contextData`</li><li>[&quot;category&quot;] = &quot;news&quot;;</li><li>신호: `c_contextData.category=news`</li></ul> |
| `c_cookiesEnabled` | 쿠키를 사용할 수 있는지 여부를 지정합니다. 옵션은 다음과 같습니다. yes, no, unknown |
| `c_currencyCode` | 거래에 사용된 통화 유형입니다. |
| `c_evar#` | 사용자 지정 eVar |
| `c_events` | 설정 기준 `s.events`. |
| `c_hier#` | 사용자 지정 계층 변수입니다. |
| `c_javaEnabled` | Java를 사용할 수 있는지 여부를 지정합니다. 옵션은 다음과 같습니다. yes, no, unknown |
| `c_javaScriptVersion` | 브라우저가 지원하는 JavaScript 파일 버전입니다. |
| `c_latitude` | 숫자 위도입니다. |
| `c_linkClick` | 옵션: custom, download exit |
| `c_linkCustomName` | 링크에 제공된 사용자 지정 이름입니다(있을 경우). |
| `c_linkDownloadURL` | 다운로드 링크의 URL입니다. |
| `c_linkExitURL` | 종료 링크 URL입니다. |
| `c_list#` | 사용자 지정 목록 변수입니다. |
| `c_longitude` | 숫자 경도입니다. |
| `c_mediaPlayerType` | 미디어 스트림 추적 요청용입니다. 옵션은 다음과 같습니다.  other, primetime |
| `c_pageName` | 페이지 이름(설정된 경우)입니다. |
| `c_pageURL` | 브라우저의 주소 표시줄에 있는 페이지의 주소입니다. |
| `c_products` | 제품 문자열(`s.products`에 의해 설정됨)입니다. |
| `c_prop` | 사용자 지정 Prop입니다. |
| `c_purchaseID` | 구매에 대한 고유 ID입니다. |
| `c_referrer` | 현재 페이지의 앞 페이지입니다. |
| `c_screenResolution` | 화면 너비와 높이(픽셀 단위)입니다. |
| `c_server` | 웹 서버 이름(`s.server`에 의해 설정됨)입니다. |
| `c_state` | 지역(설정 기준) `s.state`). |
| `c_timezone` | 시간 오프셋(시간 단위)입니다. |
| `c_transactionID` | 거래의 고유 ID입니다. |
| `c_zip` | 우편 번호(설정: `s.zip`). |
