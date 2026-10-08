---
title: Analytics 구현을 위한 디버깅 도구
description: Analytics 디버거, 브라우저 개발자 도구 및 HTTP 디버깅 프록시를 사용하여 구현이 Adobe에 보내는 데이터를 검사합니다.
keywords: 패킷 분석기, 패킷 모니터, 패킷 스니퍼, 디버거, charles, NS_BINDING_ABORTED, sendBeacon
feature: Implementation Basics
exl-id: db077293-f72c-4933-8a30-f1e1963f332e
role: Admin, Developer, Leader
TQID: 'https://experienceleague.adobe.com/debgxI3FK1fp1Q02GY1-0H40z-L4G2HSmq11Tog97-Y'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: a421fb65-2c82-457a-921c-28c46b697a39
    internal-label: Analytics basics
subfeature_v2:
  - id: e992d880-33bc-4949-a648-aa7d410276cd
    internal-label: Validation
  - id: c24fe15a-643a-47bd-8278-5e027df49785
    internal-label: Implementation basics
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 319f78bb5f8c2449a7263e3f1c378c49656889a7
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 3%
---
# Analytics 구현을 위한 디버깅 도구

패킷 분석기 또는 패킷 스니퍼라고도 하는 디버깅 도구를 사용하여 구현에서 Adobe에 보내는 데이터를 검사할 수 있습니다. 요청이 성공적으로 실행되는지 확인하고, 이러한 요청에 포함된 변수 및 페이로드를 검사하고, 예기치 않은 구현 동작을 해결하는 데 도움이 될 수 있습니다.

>[!NOTE]
>
>이 페이지에 나열된 도구는 포괄적이지 않습니다. Adobe Analytics 고객이 유용하다고 느낀 도구를 나타냅니다. Adobe에서 제공하는 도구를 제외하고 Adobe은 이러한 제품을 지원하거나 문제를 해결하지 않습니다. 설치, 사용 및 지원 정보는 도구 게시자에게 문의하십시오.

## 디버깅 도구 선택

다음 카테고리는 검사할 내용을 기반으로 도구를 선택하는 데 도움이 됩니다.

| 도구 유형 | 유용한 경우 |
| --- | --- |
| **분석 및 태그 디버거** | Analytics 변수, 태그, 데이터 레이어 또는 컬렉션 요청을 사람이 읽을 수 있는 형식으로 해석하고 표시하기를 원합니다. |
| **브라우저 개발자 도구** | 웹 구현을 디버깅하고 있으며 별도의 디버깅 응용 프로그램을 설치하지 않고 직접 네트워크 요청을 검사하려고 합니다. |
| **HTTP(S) 디버깅 프록시** | 브라우저, 모바일 앱, WebViews, API 또는 기타 클라이언트의 HTTP 트래픽을 검사하거나 브라우저 개발자 도구 이상의 기능이 필요합니다. |

## Analytics 및 태그 디버거

Analytics 및 태그 디버거는 Analytics 기술을 인식하고 요청을 해석합니다. 이러한 도구를 사용하면 네트워크 요청을 수동으로 디코딩하지 않고도 Adobe Analytics 변수, Experience Platform Web SDK 페이로드, 태그 및 관련 구현 정보를 보다 쉽게 식별할 수 있습니다.

| 도구 | 가용성 | 유용한 대상: | 고려 사항 |
| --- | --- | --- | --- |
| **[Adobe Experience Platform Debugger](https://experienceleague.adobe.com/ko/docs/experience-platform/debugger/home)** | 브라우저 확장 | Adobe Analytics, 태그, 데이터 레이어 및 Experience Platform Web SDK을 포함한 Adobe Experience Platform 및 CX Enterprise 구현 디버깅 | Adobe 기술에 초점을 맞춘 Adobe 제공 도구 |
| **[옴니버그](https://omnibug.io)** | Chromium 기반 브라우저 및 Firefox | Adobe Analytics, Experience Platform Web SDK, Adobe 태그 및 기타 여러 분석 및 마케팅 공급업체의 요청 디코딩 | 여러 공급업체의 기술을 포함하는 구현에 유용함 |
| **[ObservePoint 디버거](https://www.observepoint.com/solutions/observepoint-debugger/)** | Chrome 및 Edge | Adobe Analytics 요청을 포함한 분석, 마케팅 및 측정 태그 검사 및 디코딩 | 브라우저 기반 디버거, ObservePoint 는 별도의 자동화된 구현 유효성 검사 제품도 제공합니다 |
| **[Adobe Experience Platform Assurance](https://experienceleague.adobe.com/ko/docs/experience-platform/assurance/home)** | CX Enterprise의 웹 애플리케이션 | Mobile SDK 구현에서 이벤트 검사 및 유효성을 검사하고, Edge Network에서 이벤트를 처리하는 방법 보기 | Adobe 제공 도구: 앱을 Assurance 세션에 연결하여 이벤트를 확인합니다. |

## 브라우저 개발자 도구

모든 최신 브라우저에는 네트워크 요청을 검사할 수 있는 개발자 도구가 포함되어 있으므로 웹 구현을 디버깅하는 데 별도의 도구가 필요하지 않은 경우가 많습니다. **F12** 또는 **Ctrl+Shift+I**(Windows 및 Linux) 또는 **Cmd+Option+I**(macOS)를 누른 다음 **네트워크** 탭을 선택합니다. Safari에서 먼저 Safari의 **고급** 설정에서 개발자 기능을 사용하도록 설정합니다.

## HTTP(S) 디버깅 프록시

HTTP 디버깅 프록시는 클라이언트와 서버 간의 HTTP 및 HTTPS 트래픽을 가로채웁니다. 이러한 기능은 브라우저 개발자 도구가 충분한 가시성을 제공하지 않거나 구현이 기존 웹 브라우저 외부에서 실행될 때 유용합니다.

HTTPS 검사는 일반적으로 디버깅 프록시가 제공하는 인증서를 신뢰하도록 클라이언트를 구성해야 합니다. 인증서를 설치하거나 암호화된 트래픽을 가로챌 때 조직의 보안 정책을 따르십시오.

| 도구 | 유용한 대상: |
| --- | --- |
| **[Charles](https://www.charlesproxy.com/)** | 브라우저, 애플리케이션, 모바일 장치 및 기타 HTTP(S) 트래픽 검사 |
| **[Fiddler Everywhere](https://www.telerik.com/fiddler/fiddler-everywhere)** | 애플리케이션 및 디바이스 간 HTTP 트래픽 캡처 및 검사 이전 Fiddler Classic 제품과 구별됩니다. |
| **[Proxyman](https://proxyman.com/)** | 브라우저, 애플리케이션 및 모바일 장치에서 HTTP(S) 트래픽 검사 및 수정 |
| **[HTTP Toolkit](https://httptoolkit.com/)** | 애플리케이션 및 API 디버깅을 위한 워크플로우를 사용하여 애플리케이션, API, 개발 환경 및 모바일 장치의 트래픽 검사 |
| **[mitmproxy](https://www.mitmproxy.org/)** | 명령줄 및 웹 인터페이스를 통한 스크립트 가능한 HTTP(S) 차단, 검사 및 수정. 명령줄 워크플로에 익숙한 사용자에게 가장 적합합니다. |

## Adobe Analytics 요청 찾기

AppMeasurement과 같이 Adobe Analytics으로 직접 데이터를 전송하는 구현의 경우 다음을 위해 네트워크 요청을 필터링합니다.

```text
/ss/
```

Adobe Analytics 컬렉션 요청에는 요청 URL 또는 페이로드에 Analytics 변수가 포함되어 있습니다. 원시 요청에서는 변수 이름이 아닌 쿼리 매개 변수 이름을 사용합니다. 예를 들어, eVar1은 `v1`(으)로 표시되고 prop1은 `c1`(으)로 표시됩니다. Analytics 디버거는 이 이름을 자동으로 디코딩합니다. 직접 디코딩하려면 Data Insertion API 설명서에서 [변수 참조](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/variable-reference)를 참조하십시오.

Analytics 데이터 수집 서버가 반환하는 HTTP 상태 코드는 데이터 삽입 API 설명서의 [HTTP 응답 코드](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/troubleshooting#http-response-codes)를 참조하십시오.

Adobe Experience Platform Web SDK을 사용하는 구현의 경우 다음을 위해 네트워크 요청을 필터링합니다.

```text
/ee/
```

요청을 선택하고 페이로드를 검사하여 Adobe Experience Platform Edge Network으로 전송된 데이터를 확인합니다. 웹 SDK은 Edge Network으로 데이터를 보낸 다음 Adobe Analytics 및 기타 구성된 서비스에 데이터를 전달할 수 있습니다. 클라이언트 요청 검사는 브라우저가 Edge Network에 보낸 내용을 확인합니다. 모든 다운스트림 서비스에서 데이터가 성공적으로 처리되었는지 확인하는 것은 아닙니다. Edge Network에서 이벤트를 처리하는 방법을 보려면 [Adobe Experience Platform Assurance](https://experienceleague.adobe.com/ko/docs/experience-platform/assurance/home)을(를) 사용하십시오.

## 중단된 요청

페이지가 탐색되면 브라우저는 아직 진행 중인 요청을 취소할 수 있습니다. Firefox에서는 이러한 요청에 `NS_BINDING_ABORTED` 레이블을 지정하고, Chrome 및 Edge에서는 이러한 요청에 `(canceled)` 레이블을 지정합니다. 탐색 후 요청이 계속 표시되도록 하려면 **로그 유지**(Chrome 및 Edge) 또는 **로그 유지**(Firefox)를 사용하도록 설정하십시오.

취소된 요청이 반드시 데이터가 손실되었음을 의미하지는 않습니다. 브라우저가 전체 요청을 보냈을 수 있으며 응답을 기다리는 중만 중지되었을 수 있습니다. 브라우저 개발자 도구는 일반적으로 차이를 표시할 수 없지만 HTTP 디버깅 프록시는 차이를 표시할 수 있습니다.

`navigator.sendBeacon()`(으)로 보낸 요청은 탐색 시 취소되지 않습니다. AppMeasurement은 종료 링크에 `sendBeacon`을(를) 사용하며 [`useBeacon`](/help/implement/vars/config-vars/usebeacon.md)이(가) 활성화될 때마다 사용합니다. 웹 SDK은 [`documentUnloading`](https://experienceleague.adobe.com/ko/docs/experience-platform/collection/js/commands/sendevent/documentunloading)&#x200B;(으)로 전송된 이벤트에 이 태그를 사용합니다. 링크 추적 요청이 자주 취소되는 경우 다음 옵션을 사용합니다.
