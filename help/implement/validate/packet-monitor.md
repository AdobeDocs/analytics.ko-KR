---
title: 패킷 분석기
description: 패킷 분석기를 사용하여 구현에서 Adobe 데이터 수집 서버로 보낸 데이터를 볼 수 있습니다.
keywords: 패킷 스니퍼, http 상태, 200, 302, charles
feature: Implementation Basics
exl-id: db077293-f72c-4933-8a30-f1e1963f332e
role: Admin, Developer, Leader
TQID: https://experienceleague.adobe.com/debgxI3FK1fp1Q02GY1-0H40z-L4G2HSmq11Tog97-Y
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 7d733a6375f6c6009563bc53f5a3ff090dbc48ed
workflow-type: tm+mt
source-wordcount: 679
ht-degree: 68%

---

# 패킷 분석기

패킷 분석기를 사용하여 구현에서 Adobe 데이터 수집 서버로 보낸 데이터를 볼 수 있습니다.

Adobe CX Enterprise Debugger와 마찬가지로 패킷 모니터는 이미지 요청에서 전달되는 데이터 매개 변수를 표시하지만 추가 기능도 제공합니다.

* 사용자 지정 링크 추적 이미지 요청 보기
* 하드 코딩된 이미지 요청이나 [!DNL Appmeasurement]와 같이 JavaScript 외의 구현 방법을 사용하여 이미지 요청 보기

Analytics 요청을 보려면 &quot;b/ss&quot;를 사용하여 발신 요청을 필터링하십시오.

요청이 Adobe의 [!DNL Analytics] 처리 서버에 전달되지 못하는 경우에도 디버거가 이미지 요청을 보고하는 드문 경우가 있습니다. 패킷 모니터를 사용하면 특정 이미지 요청이 성공적으로 실행되는지 100% 확인할 수 있습니다.

Adobe은 공식적인 패킷 모니터를 제공하지 않지만, 인터넷에는 다양한 종류의 모니터가 있습니다. 다음은 다른 사람들이 유용하다고 발견한 일부 패킷 모니터입니다.

>[!TIP]
>
>이러한 목록은 전체 목록이 아니라 자주 사용하는 모니터에 대한 정보입니다.

| Firefox | Internet Explorer | Chrome | 독립 실행형 프로그램 |
|---|---|---|---|
| [Observe Point](https://www.observepoint.com/product#plugin) (태그 뷰어) | [HttpWatch](https://www.httpwatch.com/) | [Observe Point](https://www.observepoint.com/product#plugin) (태그 뷰어) | [Charles](https://www.charlesproxy.com/) |
| [HttpFox](https://addons.thunderbird.net/ko-kr/firefox/addon/httpfox/) |  | [Chrome Developer Tools](https://code.google.com/chrome/devtools/docs/overview.html) | [Fiddler](https://www.telerik.com/fiddler) |
| [데이터 변조](https://addons.mozilla.org/ko-KR/firefox/addon/tamper-data-for-ff-quantum/) |  | [Firebug Lite](https://chromewebstore.google.com/detail/firebug-lite-for-google-c/ehemiojjcpldeipjhjkepfdaohajpbdo) | [Wireshark](https://www.wireshark.org/) |
| [HttpWatch](https://www.httpwatch.com/) |  |  |  |
| [Firebug](https://getfirebug.com/) |  |  |  |

>[!NOTE]
>
>Adobe는 이러한 패킷 모니터와 관련하여 발생하는 문제를 지원하거나 해결하지 않습니다. 지원이 필요하면 패킷 모니터 제공 사이트를 참조하십시오.

## 일반적인 HTTP 응답 상태 코드

AppMeasurement가 Adobe 데이터 수집 서버에 데이터를 보내면 서버는 응답 상태 코드로 응답합니다.

* **200 OK**: 데이터 수집 서버의 가장 일반적인 응답입니다. 이미지 요청을 성공적으로 수신했으며 투명한 이미지가 반환되었습니다.
* **302 발견됨**: 이 응답을 수신하는 두 가지 가능한 이유가 있습니다.
   * 방문자의 첫 번째 이미지 요청: 사용자가 사이트를 처음 방문하는 경우 리디렉션이 발생합니다. 이 리디렉션은 방문자 쿠키를 가져오는 것입니다. 데이터 수집에는 영향을 주지 않습니다.
   * Comscore와 Adobe 간의 통합: 조직에서 Comscore/Analytics 통합을 사용하는 경우 각 이미지 요청은 항상 302 응답을 표시합니다.
* **404 찾을 수 없음**: 이 응답은 이미지 요청을 찾을 수 없으며 데이터가 Adobe 데이터 수집 서버에 전송되지 않음을 의미합니다. 이 응답은 하드 코딩된 이미지 요청의 형식이 올바로 지정되지 않은 경우에도 가능합니다. Analytics를 구현한 개인 또는 팀과 함께 이 문제를 해결하십시오.

## 응답 코드의 NS_BINDING_ABORTED

이 메시지는 링크 추적 이미지 요청이 Adobe의 데이터 수집 서버에서 오는 응답을 기다리기 전에 브라우저를 다음 페이지로 진행할 수 있게 디자인되었기 때문에 발생합니다.

이미지 요청에 대한 Adobe의 응답은 페이지의 콘텐츠와 관계가 없는 1x1 투명 이미지입니다. Adobe의 패킷 모니터에 **[!UICONTROL 200 OK]** 응답이나 **[!UICONTROL NS_BINDING_ABORTED]** 응답이 있는 라인 항목이 표시되면 데이터가 서버에 도착한 것이므로, 더 이상 페이지를 대기시킬 필요가 없습니다.

플러그인으로 통합된 패킷 모니터에는 전체 응답이 거의 없습니다. 전체 응답이 수신되지 않았기 때문에 요청이 중단된 것으로 간주하는 경향이 있습니다. 또한 이러한 모니터는 중단된 요청인지 응답인지 여부를 구분하지 않습니다. 독립형 패킷 모니터에는 일반적으로 보다 자세한 메시지가 표시되며, 상태를 보다 정확하게 보고합니다. 예를 들어, 사용자는 *Charles*&#x200B;에서 &quot;전체 응답을 받기 전에 클라이언트에서 연결을 닫았습니다&quot;라는 메시지를 받을 수 있습니다. 즉, 데이터가 서버에 도달했지만 브라우저가 1x1 픽셀이 수신되기 전에 다음 페이지로 이동했습니다.

외부 패킷 모니터가 응답 대신 데이터 수집 요청의 취소를 보고한다면 심각한 문제일 수도 있습니다. Adobe [!DNL Customer Care]에서 문제 해결에 관한 도움말을 제공할 수 있습니다.
