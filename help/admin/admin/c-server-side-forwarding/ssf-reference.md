---
description: 서버 측 전달 호출의 구성 변수, HTTP 헤더 및 데이터 신호에 대한 종합 목록 및 설명.
seo-description: 서버 측 전달 호출의 구성 변수, HTTP 헤더 및 데이터 신호에 대한 종합 목록 및 설명.
seo-title: 서버측 포워딩 데이터 및 코드 참조
title: 서버측 포워딩 데이터 및 코드 참조
uuid: 3 EB 3 EA 0 F-A 530-448 D-BBA 5-6408 B 2490 DC 8
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 서버측 포워딩 데이터 및 코드 참조

서버 측 전달 호출의 구성 변수, HTTP 헤더 및 데이터 신호에 대한 종합 목록 및 설명.

## 구성 변수 {#section_AD402B5EB9B24BF3B2039DA80FCA901E}

Parameters prefixed with `d_*` identify special, system-level key-value pairs used by our [data collection servers](https://marketing.adobe.com/resources/help/en_US/aam/c_compcollect.html) (DCS). [DCS API 호출에 대한 지원되는 속성](https://marketing.adobe.com/resources/help/en_US/aam/dcs-keys.html)을 참조하십시오.

| 매개 변수 | 설명 |
|--- |--- |
| d_rs | (Gets set with legacy/tracking-server-based server-side forwarding) <br>Set to the report suites passed in with the hit to Analytics. |
| d_dst_filter | (Gets set with report-suite-based server-side forwarding)  <br>Set to the report suite IDs passed in with the hit to Analytics. |
| d_dst | Analytics에 대한 요청에서 대상에 대한 컨텐츠가 클라이언트로 다시 전송될 것으로 예상하는 경우 d_dst=1<br>로 설정합니다. |
| d_mid | Analytics에 전달된 Experience Cloud ID입니다. |

## HTTP 헤더 {#section_0549705E76004F9585224AEF872066C0}

이 헤더는 HTTP 호출에서 데이터 및 응답 요청과 같은 정보를 포함하는 필드입니다.

<!-- Meike, missing link in table below: "See Understanding Calls to the Demdex Domain" -->

| HTTP 헤더 | 설명 |
|--- |--- |
| 호스트 | Analytics 호스트 구성 파일에 지정된 클라이언트의 특정 데이터 수집 호스트 이름으로 설정됩니다. 이 이름은   `host name .demdex.net` .  Demdex 도메인에 대한 호출 이해를 참조 하십시오 . |
| User-Agent | Analytics에 전달된 User-Agent 헤더로 설정합니다. |
| X-Original-User-Agent | Only set if an alternate user agent was specified by one of these headers: </br>`X-Device-User-Agent\ `  </br>`X-Original-User-Agent\`   </br>`X-OperaMini-Phone-UA\`   </br>`X-Skyfire-Phone\`    </br>`X-Bolt-Phone-UA\` |
| X-Forwarded-For | 요청한 클라이언트의 IP 주소로 설정합니다. Analytics는 이미 수신 `X-Forwarded-For` 헤더를 구문 분석하고 사용할 올바른 IP 주소를 결정했을 것입니다. |
| Accept-Language | Analytics에 전달된 `Accept-Language` 헤더로 설정합니다. |
| Referer | Analytics로 전달되거나 Analytics로 전달된 Referer 헤더에서 수집한 페이지 URL로 설정합니다. |

## 고객 정의 신호 {#section_8F8C39E87BDE48BAA59E25CB7E86215D}

Parameters prefixed with `c_` identify customer-defined variables. [DCS API 호출에 대한 지원되는 속성](https://marketing.adobe.com/resources/help/en_US/aam/dcs-keys.html)을 참조하십시오.

| 신호 | 설명 |
|--- |--- |
| c_browserWidth 및 c_browserHeight | 브라우저 창 너비와 높이. |
| c_campaign | s.campaign에 의해 설정됩니다 . |
| c_channel | s.channel에 의해 설정됩니다 . |
| c_clientDateTime | DD/MM/yyy HH 형식의 타임스탬프: MM: SS W TZ. TZ는 분 단위이며 Date.getTimezoneOffset 메소드의 반환과 일치합니다. |
| c_colorDepth | 16비트 또는 32비트 색상으로 지정됩니다. |
| c_connectionType | 연결 유형을 지정합니다. 옵션은 다음과 같습니다.<ul><li>모뎀</li><li>lan</li></ul> |
| c_contextData.* | 예:<ul><li>Appmeasurement: s. contextdata</li><li>[" category "] =" news ";</li><li>신호: c_contextData.category=news</li></ul> |
| c_cookiesEnabled | 쿠키를 사용할 수 있는지 여부를 지정합니다. 옵션은 다음과 같습니다. 예, 아니요, 알 수 없음 |
| c_currencyCode | 거래에 사용된 통화 유형입니다. |
| c_evar# | 사용자 지정 eVar |
| c_events | s.events에 의해 설정됩니다 . |
| c_hier# | 사용자 지정 계층 변수입니다. |
| c_javaEnabled | Java를 사용할 수 있는지 여부를 지정합니다. 옵션은 다음과 같습니다. 예, 아니요, 알 수 없음 |
| c_javaScriptVersion | 브라우저가 지원하는 JavaScript 파일 버전입니다. |
| c_latitude | 숫자 위도입니다. |
| c_linkClick | 옵션은 다음과 같습니다. 사용자 정의, 다운로드 종료 |
| c_linkCustomName | 링크에 제공된 사용자 지정 이름입니다(있을 경우). |
| c_linkDownloadURL | 다운로드 링크의 URL입니다. |
| c_linkExitURL | 종료 링크 URL입니다. |
| c_list# | 사용자 지정 목록 변수입니다. |
| c_longitude | 숫자 경도입니다. |
| c_mediaPlayerType | 미디어 스트림 추적 요청용입니다. 옵션은 다음과 같습니다.  기타, Primetime |
| c_pageName | 페이지 이름(설정된 경우)입니다. |
| c_pageURL | 브라우저의 주소 표시줄에 있는 페이지의 주소. |
| c_products | 제품 문자열(s.products에 의해 설정됨)입니다. |
| c_prop | 사용자 지정 Prop입니다. |
| c_purchaseID | 구매에 대한 고유 ID입니다. |
| c_referrer | 현재 페이지의 앞 페이지입니다. |
| c_screenResolution | 화면 너비와 높이(픽셀 단위)입니다. |
| c_server | 웹 서버 이름(s.server에 의해 설정됨)입니다. |
| c_state | 지역(s.state에 의해 설정됨)입니다. |
| c_timezone | 시간 오프셋(시간 단위)입니다. |
| c_transactionID | 거래의 고유 ID입니다. |
| c_zip | 우편 번호(s.zip에 의해 설정됨)입니다. |
